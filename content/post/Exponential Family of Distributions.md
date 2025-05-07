---
draft: false
title: "Explonential Family of Distributions"
categories: ["Notes", "Statistics"]
---

# Exponential Family of Distributions

The exponential family of distributions is a powerful and widely used class of probability distributions in statistics and machine learning. The exponential family provides a unified framework for many common probability distributions like the normal, binomial, Poisson, and gamma distributions.

## Exponential Family General Form

A probability distribution belongs to the exponential family if its probability density function (for continuous distributions) or probability mass function (for discrete distributions) can be written as:

where:

$$
p(x∣θ)=h(x)exp(η(θ) ^⊤ T(x)−A(θ))
$$

x is the random variable.

$\theta$ is the parameter (or vector of parameters) of the distribution.

$h(x)$ is a base measure, which does not depend on θ.

$\eta(\theta)$ is called the natural parameter.

$T(x)$ is the sufficient statistic.

$A(\theta)$ is the log-partition function (or cumulant function), ensuring that the distribution is normalized (i.e., it integrates to 1 over the sample space).

## What’s Special About the Exponential Family?

- **Sufficient Statistics**: For exponential family distributions, the function T(x) gives a sufficient statistic for θ. This means that knowing T(x) provides all the information about θ contained in the data.

- **Conjugacy**: Many exponential family distributions have conjugate priors in Bayesian statistics. This means the posterior distribution (after observing data) belongs to the same family as the prior, simplifying Bayesian updating.

- **Moment Properties**: The log-partition function A(θ) has important properties. The first derivative of A(θ) gives the expected value of the sufficient statistic, while the second derivative gives the variance.

## Normal Distribution

The probability density function (PDF) of the normal distribution is:

$$
p(x|\mu, \sigma^2) = \frac{1}{\sqrt{2 \pi \sigma^2}} \exp\left( -\frac{(x - \mu)^2}{2 \sigma^2} \right)
$$

To show that this belongs to the exponential family, we need to express it in the canonical form:

$$
p(x|\theta) = h(x) \exp\left( \eta(\theta) \cdot T(x) - A(\theta) \right)
$$

We rewrite the normal distribution PDF in a more revealing way:

$$
-\frac{(x - \mu)^2}{2 \sigma^2} = -\frac{x^2 - 2x\mu + \mu^2}{2 \sigma^2} \\
 = -\frac{x^2}{2 \sigma^2} + \frac{x\mu}{\sigma^2} - \frac{\mu^2}{2 \sigma^2}
$$

$$
p(x|\mu, \sigma^2) = \frac{1}{\sqrt{2 \pi \sigma^2}} \exp\left( -\frac{x^2}{2 \sigma^2} + \frac{x\mu}{\sigma^2} - \frac{\mu^2}{2 \sigma^2} \right)
$$

$$
p(x|\mu, \sigma^2) = \left( \frac{1}{\sqrt{2 \pi \sigma^2}} \exp \left( -\frac{\mu^2}{2 \sigma^2} \right) \right) \exp \left( \frac{x\mu}{\sigma^2} - \frac{x^2}{2 \sigma^2} \right)
$$

So, the normal distribution is in the exponential family with:

$$
\begin{align*}
h(x) &= \frac{1}{\sqrt{2 \pi \sigma^2}} \exp \left( -\frac{x^2}{2 \sigma^2} \right) \\
\eta(\theta) &= \left( \frac{\mu}{\sigma^2}, -\frac{1}{2 \sigma^2} \right) \\
T(x) &= \left( x, x^2 \right) \\
A(\theta) &= \frac{\mu^2}{2 \sigma^2} + \frac{1}{2} \log (2 \pi \sigma^2)
\end{align*}
$$

> The exponential family forms the basis for generalized linear models, which extend linear regression to handle response variables with non-normal distributions.

To find the mean and variance of the estimates of the parameters μ and σ² of the normal distribution using the log-partition function, we use the properties of the exponential family distribution.

For a univariate normal distribution, the natural parameters are:

$$
\begin{align*}
& \eta(\theta) = \begin{pmatrix} \frac{\mu}{\sigma^2} \\ -\frac{1}{2\sigma^2} \end{pmatrix} \\
&  \eta_1 = \frac{\mu}{\sigma^2} \\
& \eta_2 = -\frac{1}{2\sigma^2} \\
& \text{The log-partition function A(θ) for the normal distribution is:} \\
&  A(\theta) = \frac{\mu^2}{2 \sigma^2} + \frac{1}{2} \log(2 \pi \sigma^2) \\
& \text{Substituting } \(\mu\) and \(\sigma^2\) \text{ in terms of }\(\eta_1\) \text{ and }\(\eta_2\):\\
&\mu = \eta_1 \sigma^2 \\
 &\sigma^2 = -\frac{1}{2 \eta_2} \\
 &\text{Thus:} \\
A(\theta) & = \frac{(\eta_1 \sigma^2)^2}{2 \sigma^2} + \frac{1}{2} \log\left(2 \pi \sigma^2\right) \\
&= \frac{\eta_1^2 \sigma^2}{2} + \frac{1}{2} \log\left(2 \pi \left(-\frac{1}{2 \eta_2}\right)\right) \\
&= \frac{\eta_1^2 \left(-\frac{1}{2 \eta_2}\right)}{2} + \frac{1}{2} \left(\log(2 \pi) - \log(-\eta_2)\right) \\
&= -\frac{\eta_1^2}{4 \eta_2} - \frac{1}{2} \log(-\eta_2) + \text{constant}
\end{align*}
$$

## Mean of the Parameters

To find the mean of the estimates of $\mu$ and $\sigma2$, we use the first derivatives of $A(\theta)$.

- Mean of $\mu$:

  The first derivative of A(θ) with respect to η1 gives the mean of the sufficient statistic x:

$$
  \frac{\partial A(\theta)}{\partial \eta_1} = \mu
$$

- Mean of σ2:

  The first derivative of A(θ) with respect to η2 gives the mean of the sufficient statistic x2:

  Since the mean of $x^2$ is $mu^2 + \sigma^2$, and by subtracting $mu^2$, the mean of $\sigma^2$ is directly:

$$
  \frac{\partial A(\theta)}{\partial \eta_2} = \frac{\mu^2 + \sigma^2}{2} \\
  \mathbb{E}[\hat{\sigma}^2] = \text{Var}(x) = \sigma^2
$$

## Variance of the Parameters

To find the variance, we use the second derivatives of $A(\theta)$.

$$
\begin{align*}
\text{Var}(\hat\mu) = -\frac{\partial^2 A(\theta)}{\partial \eta_1^2} = \frac{1}{2 \eta_2} \\ \\
\text{Since} \(\eta_2 = -\frac{1}{2 \sigma^2}\), \text{ this can be rewritten as: } \\  \\
 \text{Var}(\hat\mu) = \sigma^2
\end{align*}
$$

Variance of $\mu$: The variance of the sufficient statistic $x$ is given by the negative of the second derivative of $A(\theta)$ with respect to $\eta_1$:

Variance of $\sigma^2$: The variance of $\sigma^2$ is related to the second derivative of $A(\theta)$ with respect to $\eta_2$:

The final estimates of the mean and variance of the statistics are:

$$
\begin{align*}
\mathbb{E}[\hat\mu] &= \mu \\
\text{Var}(\hat\mu) &= \sigma^2 \\
\mathbb{E}[\hat\sigma^2] &= \sigma^2 \\
\text{Var}(\hat\sigma^2) &= 2 \left(\frac{\mu^2}{\sigma^2} + \sigma^2\right) \\
\end{align*}
$$

## Appendix

$$
\begin{align*}
\mathbb{E}[x^2] & = \mathbb{E}[(x - \mu + \mu)^2] \\
& = \mathbb{E}[(x - \mu)^2 + 2(x - \mu)\mu + \mu^2] \\
& = \mathbb{E}[(x - \mu)^2] + \mathbb{E}[2(x - \mu)\mu] + \mathbb{E}[\mu^2] \\
& = \mathbb{E}[(x - \mu)^2] + 2\mu \cdot 0 + \mu^2 \\
& = \mathbb{E}[(x - \mu)^2] + \mu^2 \\
& = \text{Var}(x) + \mu^2 \newline
& = \sigma^2 + \mu^2
\end{align*}
$$
