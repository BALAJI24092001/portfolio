---
draft: false
title: "Calculus"
categories: ["Notes"]
---

<!-- tags: ["MATH"] -->

## Function

### Function of single variable

A relation f from a set $A$ to a set $B$ is said to be a function if every element of set $A$ has one and only one image in set $B$. In other words, a function $f$ is a relation such that no two pairs in the relation have the same first element.

The notation $f : X \rightarrow Y$ means that $f$ is a function from $X$ to $Y$ . $X$ is called the domain of $f$, and $Y$ is called the co-domain of $f$.

Given an element $x \in X$, there is a unique element $y$ in $Y$ that is related to $x$. The unique element $y$ to which $f$ relates $x$ is denoted by $f(x)$ and is called $f$ of $x$, or the value of $f$ at $x$, or the image of $x$ under $f$.

The set of all values of $f(x)$ taken together is called the range of $f$ or the image of $X$ under $f$. Symbolically:

range of $f = \{y \in Y | y = f(x) \text{ for some } x ∈ X\}$

| Function      | Domain         | Range               |
| ------------- | -------------- | ------------------- |
| $y = x + 2$   | $\mathbb{R}$   | $\mathbb{R}$        |
| $y = 3x² - 7$ | $\mathbb{R}$   | $\{y: y ≥ -7\}$     |
| $y = sin x$   | $\mathbb{R}$   | $\{y: -1 ≤ y ≤ 1\}$ |
| $y = 2^x$     | $\mathbb{R}$   | $\{y: y > 0\}$      |
| $y = 1/x$     | $\{x: x ≠ 0\}$ | $\{y: y ≠ 0\}$      |
| $y = log₂ x$  | $\{x: x > 0\}$ | $\mathbb{R}$        |

### Types of Functions

1. **One-One (Injective) Function**<br>
   A function $f : X \rightarrow Y$ is defined to be one-one (or injective) if the images of distinct elements of $X$ under $f$ are distinct, i.e., for any $x1, x2 \in X$, if $f(x1) = f(x2)$, then it implies that $x1 = x2$.

2. **Onto (Surjective) Function**<br>
   A function $f : X \rightarrow Y$ is said to be onto (or surjective) if every element of $Y$ is the image of some element of $X$ under $f$, i.e., for every $y \in Y$ , there exists an element $x \in X$ such that $f(x) = y$.

3. **One-One and Onto (Bijective) Function**<br>
   A function $f : X \rightarrow Y$ is said to be one-one and onto (or bijective) if it is both one-one and onto.

### Special functions

- <u>**Explicit Functions**</u> <br>
  Explicit functions are functions where the dependent variable (usually denoted as $y$) is expressed explicitly in terms of the independent variable (usually denoted as $x$), such as $y = f(x)$. <br>
  _**Example**_ : $y = f(x) = 2x + 3$

- <u>**Implicit Functions**</u> <br>
  Implicit functions are functions where the relationship between the dependent and independent variables is defined implicitly, often by an equation involving both variables, like $x^2 + y^2 = 1$.

- <u>**Composite Functions**</u> <br>
  Composite functions are formed by combining two or more functions, creating a new function. For example, if $f(x)$ and $g(x)$ are functions, the composite function $h(x) = f(g(x))$ or $h(x) = g(f(x))$ <br>
  Let $f(x) = 2x$ and $g(x) = x^2$. Then the composite function is $h(x) = f(g(x)) = 2x^2$.

- <u>**Polynomial Functions**</u> <br>
  Polynomial functions are algebraic functions of the form <br>
  $f(x) = a_nx^n + a_{n−1}x_{n−1} + . . . + a_1x + a_0$, where ai are constants, and n is a non-negative integer.<br>
  _**Example**_: $f(x) = 3x^3 − 2x^2 + 5x − 1$ is a polynomial function in `x` with degree 3.<br>

  > Note: A polynomial function of degree ’0’ is called a constant polynomial function (or) simply constant function.

- <u>**Rational Functions**</u> <br>
  Rational functions are functions of the form $f(x) = \frac{p(x)}{q(x)}$ , where $p(x)$ and $q(x)$ are both
  polynomial functions. <br> _**Example**_: $f(x) = \frac{2x^2−3x+1}{x^2+4x+4}$

- <u>**Algebraic Functions**</u> <br>
  Algebraic functions are functions that can be defined by algebraic equations involving polynomial, rational, and root functions.<br>
  _**Example**_: $f(x) = \sqrt{3x^3 − 2x^2 + 5x − 1}$ <br>
  If a relation arises due to performing a finite number of fundamental operations additions, subtraction, multiplication, division, root extraction etc. on polynomial functions then such a relation is also called an Algebraic function.

  1.  All polynomial functions are algebraic but not the converse.
  2.  A function that is not algebraic is called transcendental function.

- <u>**Logarithmic Functions**</u><br>
  Logarithmic functions are functions of the form $f(x) = logb(x)$, where $b$ is the base of the logarithm.<br>
  _**Example**_: $f(x) = log_{10}(x)$

- <u>**Even Functions**</u><br>
  Even functions are symmetric about the y-axis, and odd functions are symmetric aboutthe origin. For even functions, $f(−x) = f(x)$, and for odd functions, $f(−x) = −f(x)$. <br>
  _**Example**_: Even Function: $f(x) = x^2$ (Symmetric about the y-axis)

- <u>**Odd Function:**</u><br>
  $f(x) = x^3$ (Symmetric about the origin)

- <u>**Exponential Functions**</u><br>
  Exponential functions are functions of the form $f(x) = a^x$, where $a$ is a positive constant.
  _**Example**_: $f(x) = 2^x$

- <u>**Modulus Functions**</u><br>
  Modulus functions, often denoted as $f(x) = |x|$, return the absolute value of $x$, making it always non-negative.
  _**Example**_: $f(x) = |x|$

- <u>**Signum (Sign) Functions**</u><br>
  The signum (sign) function is defined as $f(x) = \text{sgn}(x)$, where: <br>
  Example:

  $$
  \text{sgn}(x) =
  \begin{cases}
  -1 & \text{if } x < 0 \\
  0 & \text{if } x = 0 \\
  1 & \text{if } x > 0
  \end{cases}
  $$

### Composition of Functions

- Let $f : A \rightarrow B$ and $g : B \rightarrow C$ be two functions. Then, the composition of $f$ and $g$, denoted by $g \circ f$, is defined as the function $g \circ f : A \rightarrow C$ given by

  $$
  (g \circ f)(x) = g(f(x))\text{, for all }x \in A
  $$

- If $f : A \rightarrow B$ and $g : B \rightarrow C$ are one-one, then $g \circ f : A \rightarrow C$ is also one-one.

- If $f : A \rightarrow B$ and $g : B \rightarrow C$ are onto, then $g \circ f : A \rightarrow C$ is also onto.
- Let $f : A \rightarrow B$ and $g : B \rightarrow C$ be the given functions such that $g \circ f$ is one-one. Then $f$ is one-one.
- Let $f : A \rightarrow B$ and $g : B \rightarrow C$ be the given functions such that $g \circ f$ is onto. Then $g$ is onto.

### Invertible Function

- A function $f : X \rightarrow Y$ is defined to be invertible if there exists a function $g : Y \rightarrow X$ such that $g \circ f = I_X$ and $f \circ g = I_Y$ . The function $g$ is called the inverse of f and is denoted by $f^{−1}$.
- A function $f : X \rightarrow Y$ is invertible if and only if f is a bijective function.
- If $f : X \rightarrow Y$ , $g : Y \rightarrow Z$, and $h : Z \rightarrow S$ are functions, then $h \circ (g \circ f) = (h \circ g) \circ f$.
- Let $f : X \rightarrow Y$ and $g : Y \rightarrow Z$ be two invertible functions. Then $g \circ f$ is also invertible with $(g \circ f)^{−1} = f^{−1} \circ g^{−1}$.

## Limits

> Limits describe how a function behaves near a point, instead of at that point. This simple yet powerful idea is the basis of all of calculus.

In calculus, the concept of a limit is fundamental to understanding the behavior of functions as they approach specific points. A limit represents the value that a function approaches as its input (independent variable) gets arbitrarily close to a certain value. We denote the limit of a function f(x) as x approaches a limit point c as follows:

$$
\lim_{x \rightarrow c} f(x) = L
$$

This means that as x gets very close to c, the values of f(x) get arbitrarily close to L.

The function $f$ is said to tend to the limit $\ell$ as $x \rightarrow a$, if for a given positive real number $\epsilon > 0$ we can find a real number $\delta > 0$ such that

$$
|f(x) - \ell| < \epsilon \quad \text{whenever} \quad 0 < |x - a| < \delta
$$

Symbolically we write

$$
\lim_{x \to a} f(x) = \ell
$$

$\textbf{Left Hand and Right Hand Limits}$

Let $x < a$ and $x \rightarrow a$ from the left hand side.

If

$$
|f(x) - \ell_1| < \epsilon, \quad a - \delta < x < a \quad \text{or} \quad \lim_{x \to a^-} f(x) = \ell_1
$$

then $\ell_1$ is called the left hand limit.

Let $x > a$ and $x \rightarrow a$ from the right hand side.

If

$$
|f(x) - \ell_2| < \epsilon, \quad a < x < a + \delta \quad \text{or} \quad \lim_{x \to a^+} f(x) = \ell_2
$$

then $\ell_2$ is called the right hand limit.

<b>If $\ell_1 = \ell_2$ then $\lim_{x \to a} f(x)$ exists. If the limit exists then it is unique.</b>

### Basic Limit Rules

There are several basic rules that help us evaluate limits:

1. The Limit of a Constant:
   $$
   \lim_{x \rightarrow c} k = k
   $$
   where k is a constant.
2. The Limit of a Sum or Difference:

   $$
   \lim_{x\rightarrow c} [f(x) ± g(x)] = \lim_{x \rightarrow c}    f(x) \pm \lim_{x \rightarrow c} g(x)
   $$

3. The Limit of a Product:

   $$
   \lim_{x \to c} [f(x) . g(x)] = \lim_{x \to c}f(x) · \lim_{x \to c}  g(x)
   $$

4. The Limit of a Quotient:

   $$
   \lim_{{x \to c}} \frac{f(x)}{g(x)} = \frac{\lim_{{x \to c}} f(x)}{\lim_{{x \to c}} g(x)}, \text{ if } \lim_{{x \to c}} g(x) \neq 0
   $$

### Trigonometry Functions

1. $\quad \lim_{{x \to 0}} \sin x = 0$

2. $\quad \lim_{{x \to 0}} \cos x = 1$

3. $\quad \lim_{{x \to 0}} \frac{\tan x}{x} = 1$

4. $\quad \lim_{{x \to 0}} \frac{\sin x}{x} = 1$

5. $\quad \lim_{{x \to 0}} \frac{\sin^{-1} x}{x} = 1$

6. $\quad \lim_{{x \to 0}} \frac{\tan^{-1} x}{x} = 1$

7. $\quad \lim_{{x \to \infty}} \frac{\sin x}{x} = 0$

8. $\quad \lim_{{x \to 0}} \left(\cos x + a \sin b x\right)^{\frac{1}{x}} = e^{ab}$

9. $\quad \lim_{{x \to 0}} \left(\frac{1 - \cos (ax)}{x}\right) = \frac{a^2}{2}$

### 1 power infinity

1. $\quad \lim_{{x \to 0}} \left(1 + x\right)^{\frac{1}{x}} = e$

2. $\quad \lim_{{x \to 0}} \left(1 + ax\right)^{\frac{1}{x}} = e^a$

3. $\quad \lim_{{x \to \infty}} \left(1 + \frac{1}{x}\right)^x = e$

4. $\quad \lim_{{x \to \infty}} \left(1 + \frac{a}{x}\right)^x = e^a$

### Log and Exponential Functions

1. $\quad \lim_{{x \to 0}} e^x = 1$

2. $\quad \lim_{{x \to 0}} \frac{e^x - 1}{x} = 1$

3. $\quad \lim_{{x \to 0}} \frac{e^{mx} - 1}{mx} = m$

4. $\quad \lim_{{x \to 0}} \frac{a^x - 1}{x} = \log_e a$

5. $\quad \lim_{{x \to 0}} \frac{\log(1 + x)}{x} = 1$

6. $\quad \lim_{{x \to a}} \frac{x^n - a^n}{x - a} = na^{n-1}$

7. $\quad \lim_{{x \to a}} \left( \frac{a^x + b^x}{2} \right)^{\frac{1}{x}} = \sqrt{ab}$

### L'Hospital's Rule

We apply L'Hospital's Rule to the limit if we get the limit in the following forms (Indeterminate forms):

$$
\frac{0}{0}, \frac{\infty}{\infty}, 0 \cdot \infty, \infty - \infty, 0^0, 1^{\infty}, \infty^0
$$

Try to convert all indeterminate forms into $\frac{0}{0}$ or $\frac{\infty}{\infty}$, then only you can apply L'Hospital's Rule.

If $\lim_{x \to a} \frac{f(x)}{g(x)}$ is of the form $\frac{0}{0}$ or $\frac{\infty}{\infty}$, then:

$$
\lim_{{x \to a}} \frac{f(x)}{g(x)} = \frac{f'(x)}{g'(x)}
$$

Note:

If $\lim_{{x \to a}} f(x)$ exists, then it is unique.
If $f(x)$ is a polynomial function, then $\lim_{{x \to a}} f(x) = f(a)$.

## Continuity

1. **Continuity of a function at a point:** <br>
   A function $f(x)$ is said to be continuous at `a` if it satisfies the following conditions

   - $f(a)$ is defined
   - $\lim_{x \to a} f(x)$ exists i.e $\lim_{x \to a^{−}} f(x) = lim_{x \to a^{+}} f(x)$
   - $\lim_{x \to a^{+}} f(x) = f(a)$

2. **Left continuous (or) continuity from the left at a point:** <br>
   A function $f(x)$ is said to be continuous from the left (or) left continuous at $x = a$ if

   - $f(a)$ is defined
   - $\lim_{x \to a^{-}} f(x) = f(a)$

3. **Right continuous (or) continuity from the right at a point:** <br>
   A function $f(x)$ is said to be continuous from the right (or) right continuous at $x = a$ if

   - $f(a)$ is defined
   - $\lim_{x \to a^{+}} f(x) = f(a)$

4. **Continuity of a function in an open interval:** <br>
   A function $f(x)$ is said to be continuous in an open interval $(a, b)$ if $f(x)$ is continuous $\forall x \in (a, b)$ (or) $\lim_{x \to c} f(x) = f(c) \forall c \in (a, b)$
5. **Continuity of a function on closed interval:** <br>
   A function $f(x)$ is said to be continuous on closed interval $[a, b]$if

   - $f(x)$ is continuous $\forall x ∈ (a, b)$
   - $\lim_{x \to a^{+}} f(x) = f(a)$
   - $\lim_{x \to b^{-}} f(x) = f(b)$

**Important Points:**<br>

1. If $f(x)$ and $g(x)$ are two continuous functions then $\quad f(x) + g(x),\quad f(x) − g(x),\quad f(x).g(x)$ and $\quad \frac{f(x)}{g(x)} (:: g(x) \neq 0)$ are also continuous.
2. Polynomial function, exponential function, sine and cosine functions, and modulus function are continuous everywhere.
3. Logarithmic functions are continuous in $(0, \infty)$
4. Let the functions f and g be continuous at a point $x = x_0$ then,
   - $cf$, $f \pm g$ and $f.g$ are continuous at $x = x_0$, where $c$ is any constant.
   - $\frac{f}{g}$ is continuous at $x = x_0$, if $g(x_0) \neq 0$
5. If $f$ is continuous at $x = x_0$ and $g$ is continuous at $f(x_0)$ then the composite function $g(f(g))$ is continuous at $x = x_0$.
6. If f is continuous at an interior point $c$ of a closed interval $[a, b]$ and $f(c) \neq 0$, then there exists a neighbourhood of $c$, throughout which $f(x)$ has the same sign as $f(c)$.
7. If $f$ is continuous in a closed interval $[a, b]$ then it is bounded there and attains its bounds at least once in $[a, b]$.
8. If $f$ is continuous in a closed interval $[a, b]$, and if $f(a)$ and $f(b)$ are of opposite signs, then there exists at least one point $c \in [a, b]$ such that $f(c) = 0$.
9. If $f$ is continuous in a closed interval $[a, b]$ and $f(a) \neq f(b)$ then it assumes every value between $f(a)$ and $f(b)$.

## Differentiability

$f(x)$ is said to be differentiable at the point $x = a$ if the derivative $f‘(a)$ exists at every point in its domain. It is given by

$$
\lim_{h \to 0} \frac{f(a+h)−f(a)}{h}
$$

**Important Note:**<br>

1. If the derivative of $f(x)$ exists at $x = a$ then the function $f(x)$ is said to be differentiable function at $x = a$.
2. $f^l(a)$ exists at $x = a \iff Lf^l(a) = Rf^l(a)$.
3. If $f(x)$ and $g(x)$ are two differentiable functions then $f(x)+g(x)$, $f(x)−g(x)$, $f(x).g(x)$, $\frac{f(x)}{g(x)}$ .. $g(x) \neq 0$ are also differentiable.
4. Polynomial functions, exponential functions, sine and cosine functions are differentiable every where.
5. Every differentiable function is continuous but a continuous function need not be differentiable.

**Derivability of a function in an open interval:**<br>
A function $f(x)$ is said to be derivable (or) differentiable in an open interval $(a, b)$ if $f^l(c)$ exists $\forall c \in (a, b)$.

**Derivability of a function on closed interval:**<br>
A function $f(x)$ is said to be derivable (or) differentiable on closed interval $[a, b]$ i. if $f^l(c)$ exists $\forall c \in (a, b)$

1. $Rf^l(a)$ exists
2. $Lf^l(b)$ exists.

## Taylor Series

Let $f(x)$ be a function which is differentiable at $x = a$. Then we can write $f(x)$ as the following power series, called the Taylor series of $f(x)$ at $x = a$:

$$
f(x) = f(a) + f'(a) \frac{(x - a)}{1!} + f''(a) \frac{(x - a)^2}{2!} + f'''(a) \frac{(x - a)^3}{3!} + \cdots
$$

### Maclaurin Series

If the Taylor Series is centred at 0, then the series is known as the Maclaurin series. It means that, if $a = 0$ in the Taylor series, then we get:

$$
f(x) = f(0) + f'(0) \frac{x}{1!} + f''(0) \frac{x^2}{2!} + f'''(0) \frac{x^3}{3!} + \cdots
$$

This is known as the Maclaurin series.

### Standards Expansions

1. $(1 - x)^{-1} = 1 + x + x^2 + x^3 + \cdots \quad \text{for } |x| < 1$
2. $(1 + x)^{-1} = 1 - x + x^2 - x^3 + \cdots \quad \text{for } |x| < 1$
3. $(1 - x)^{-2} = 1 + 2x + 3x^2 + 4x^3 + \cdots \quad \text{for } |x| < 1$
4. $(1 + x)^{-2} = 1 - 2x + 3x^2 - 4x^3 + \cdots \quad \text{for } |x| < 1$
5. $(1 - x)^{-3} = 1 + 3x + 6x^2 + 10x^3 + \cdots \quad \text{for } |x| < 1$
6. $\quad (1 + x)^{-3} = 1 - 3x + 6x^2 - 10x^3 + \ldots \quad [-1 < x < 1]$
7. $\quad (1 + x)^n = 1 + nx + \frac{n(n-1)}{2!}x^2 + \frac{n(n-1)(n-2)}{3!}x^3 + \ldots \quad [-1 < x < 1]$
8. $\quad (1 - x)^{-n} = 1 + nx + \frac{n(n+1)}{2!}x^2 + \frac{n(n+1)(n+2)}{3!}x^3 + \ldots \quad [-1 < x < 1]$
9. $\quad e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \ldots \quad [-\infty < x < \infty]$
10. $\quad e^{-x} = 1 - x + \frac{x^2}{2!} - \frac{x^3}{3!} + \ldots \quad [-\infty < x < \infty]$
11. $\quad \sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \ldots \quad [-\infty < x < \infty]$
12. $\quad \sinh x = x + \frac{x^3}{3!} + \frac{x^5}{5!} + \frac{x^7}{7!} + \ldots \quad [-\infty < x < \infty]$

13. $$
    \quad \sin^{-1} x = x + \frac{1}{2} \frac{x^3}{3} + \frac{1 \cdot 3}{2 \cdot 4} \frac{x^5}{5} + \frac{1 \cdot 3 \cdot 5}{2 \cdot 4 \cdot 6} \frac{x^7}{7} + \ldots \quad [-1 < x < 1]
    $$

14. $\quad \cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \ldots \quad [-\infty < x < \infty]$
15. $\quad \cosh x = 1 + \frac{x^2}{2!} + \frac{x^4}{4!} + \frac{x^6}{6!} + \ldots \quad [-\infty < x < \infty]$
16. $\quad \cos^{-1} x = \frac{\pi}{2} - \sin^{-1} x = \frac{\pi}{2} - \left( x + \frac{1}{2} \frac{x^3}{3} + \frac{1 \cdot 3}{2 \cdot 4} \frac{x^5}{5} + \ldots \right) \quad [-1 < x < 1]$
17. $\quad \tan x = x + \frac{x^3}{3} + \frac{2x^5}{15} + \ldots \quad \left[ -\frac{\pi}{2} < x < \frac{\pi}{2} \right]$
18. $\quad \tanh x = x - \frac{x^3}{3} + \frac{2x^5}{15} - \ldots \quad \left[ -\frac{\pi}{2} < x < \frac{\pi}{2} \right]$

19. $$
    \quad \tan^{-1} x =
        \begin{cases}
        x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \ldots & \text{for } -1 < x < 1 \newline
        \frac{\pi}{2} - \frac{1}{x} + \frac{1}{3x^3} - \frac{1}{5x^5} + \ldots & \text{for } x \geq 1 \newline
        -\frac{\pi}{2} + \frac{1}{x} - \frac{1}{3x^3} + \frac{1}{5x^5} - \ldots & \text{for } x < -1
        \end{cases}
        \quad \left[-1 < x < 1\right]
    $$

20. $\quad \cot x = \frac{1}{x} - \frac{x}{3} - \frac{x^3}{45} + \ldots \quad \left[0 < x < \pi\right]$
21. $\quad \coth x = \frac{1}{x} + \frac{x}{3} - \frac{x^3}{45} + \ldots \quad \left[0 < |x| < \pi\right]$

22. $$
    \quad \cot^{-1} x = \frac{\pi}{2} - \tan^{-1} x =
        \begin{cases}
        \frac{\pi}{2} - \left(x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \ldots\right) & \text{for } -1 < x < 1 \newline
        \frac{1}{x} - \frac{1}{3x^3} + \frac{1}{5x^5} - \ldots & \text{for } x \geq 1 \newline
        \pi + \frac{1}{x} - \frac{1}{3x^3} + \frac{1}{5x^5} - \ldots & \text{for } x < -1 \newline
        \end{cases}
        \quad \left[-1 < x < 1\right]
    $$

23. $\quad \sec x = 1 + \frac{x^2}{2} + \frac{5x^4}{24} + \ldots \quad \left[-\frac{\pi}{2} < x < \frac{\pi}{2}\right]$

24. $\quad \csc x = \frac{1}{x} + \frac{x}{6} + \frac{7x^3}{360} + \ldots \quad \left[0 < x < \pi\right]$
25. $\quad \ln(1 + x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \ldots \quad \left[-1 < x < 1\right]$

## DIFFERENTIAL CALCULUS

### Differentiation

Differentiation is the process of finding the derivative of a function. The derivative represents the rate of change of the function's value with respect to a change in its input value.

#### The Derivative

If $f(x)$ is a function, its derivative, denoted as $f'(x)$ or $\frac{df}{dx}$, is defined as:

$$
 f'(x) = \lim_{{h \to 0}} \frac{f(x+h) - f(x)}{h}
$$

> Note: The derivative represents the slope of the tangent line to the graph of the function at a given point.

#### Basic Rules of Differentiation

- **Power Rule**:

  $$
  \frac{d}{dx} [x^n] = nx^{n-1}
  $$

- **Constant Rule**:

  $$
  \frac{d}{dx} c = 0
  $$

  where c is a constant.

- **Sum Rule**:

  $$
  \frac{d}{dx} [f(x) + g(x)] = f'(x) + g'(x)
  $$

- **Difference Rule**:

  $$
  \frac{d}{dx} [f(x) - g(x)] = f'(x) - g'(x)
  $$

- **Product Rule**:

  $$
  \frac{d}{dx} [f(x) \cdot g(x)] = f'(x) \cdot g(x) + f(x) \cdot g'(x)
  $$

- **Quotient Rule**:

  $$
  \frac{d}{dx} \left[\frac{f(x)}{g(x)}\right] = \frac{f'(x) \cdot g(x) - f(x) \cdot g'(x)}{[g(x)]^2}
  $$

- **Chain Rule**:
  $$
  \frac{d}{dx} [f(g(x))] = f'(g(x)) \cdot g'(x)
  $$

#### Higher-Order Derivatives

- **Second Derivative**: The derivative of the derivative, denoted as $f''(x)$ or $\frac{d^2f}{dx^2}$.
- **nth Derivative**: The derivative taken n times, denoted as $f^{(n)}(x)$ or $\frac{d^nf}{dx^n}$.

**Critical Points and Inflection Points** <br>

- **Critical Points**: Points where $f'(x) = 0$ or $f'(x)$ is undefined. Used to determine local maxima and minima.
- **Inflection Points**: Points where the concavity of the function changes, identified by $f''(x) = 0$.

#### Mean Value Theorem for Derivatives

The Mean Value Theorem for Derivatives states that if a function $f$ is continuous on the closed interval $[a, b]$ and differentiable on the open interval $(a, b)$, then there exists at least one point $c$ in $(a, b)$ such that the instantaneous rate of change (derivative) at $c$ is equal to the average rate of change over $[a, b]$. Mathematically, it is expressed as:

$$
f'(c) = \frac{f(b) - f(a)}{b - a}
$$

**Conditions:**

1. **Continuity**: $f$ must be continuous on the closed interval $[a, b]$.
2. **Differentiability**: $f$ must be differentiable on the open interval $(a, b)$.

**Interpretation:**

The theorem essentially states that there is at least one point $c$ where the tangent to the curve is parallel to the secant line connecting $(a, f(a))$ and $(b, f(b))$.

##### Rolle's Theorem

Rolle's Theorem is a special case of the Mean Value Theorem. It states that if a function $f$ satisfies the following three conditions on a closed interval $[a, b]$:

1. $f$ is continuous on the closed interval $[a, b]$.
2. $f$ is differentiable on the open interval $(a, b)$.
3. $f(a) = f(b)$.

Then, there exists at least one point $c$ in the open interval $(a, b)$ such that:

$$
 f'(c) = 0
$$

In simpler terms, if a function starts and ends at the same value on a certain interval and meets the continuity and differentiability conditions, there is at least one point in that interval where the derivative (slope of the tangent) is zero. This means the function has a horizontal tangent line at some point in the interval.

##### Lagrange's Mean Value Theorem (MVT)

The Mean Value Theorem (MVT) generalizes Rolle's Theorem. It states that if a function $f$ satisfies the following conditions on a closed interval $[a, b]$:

1. $f$ is continuous on the closed interval $[a, b]$.
2. $f$ is differentiable on the open interval $(a, b)$.

Then, there exists at least one point $c$ in the open interval $(a, b)$ such that:

$$
 f'(c) = \frac{f(b) - f(a)}{b - a}
$$

This means that there is at least one point in the interval where the instantaneous rate of change (the derivative) is equal to the average rate of change over the interval. In other words, the slope of the tangent at some point is equal to the slope of the secant line connecting the endpoints $(a, f(a))$ and $(b, f(b))$.

**Formulas Recap** <br>

- **Rolle's Theorem:** If $f(a) = f(b)$, then $f'(c) = 0$.
- **Lagrange's Mean Value Theorem:** $f'(c) = \frac{f(b) - f(a)}{b - a}$.

#### Mean Value Theorem for Integrals

The Mean Value Theorem for Integrals states that if $f$ is continuous on the closed interval $[a, b]$, then there exists at least one point $c$ in $(a, b)$ such that the value of the function at $c$ is equal to the average value of the function over $[a, b]$. Mathematically, it is expressed as:

$$
f(c) = \frac{1}{b - a} \int_a^b f(x) \, dx
$$

**Conditions:**

1. **Continuity**: $f$ must be continuous on the closed interval $[a, b]$.

**Interpretation:**

The theorem states that there is at least one point $c$ where the function's value is equal to its average value over the interval.

**Example:**

Consider the function $f(x) = x^2$ on the interval $[1, 3]$.

1. **Check conditions**:

   - $f(x) = x^2$ is continuous on $[1, 3]$.

2. **Apply the Mean Value Theorem for Integrals**:

   $$
   \frac{1}{3 - 1} \int_1^3 x^2 \, dx = \frac{1}{2} \left[ \frac{x^3}{3} \right]_1^3 = \frac{1}{2} \left( \frac{27}{3} - \frac{1}{3} \right) = \frac{1}{2} (9 - \frac{1}{3}) = \frac{1}{2} \times \frac{26}{3} = \frac{13}{3}
   $$

   So, there exists a point $c$ in $(1, 3)$ such that $f(c) = \frac{13}{3}$.

- **Mean Value Theorem for Derivatives**: Guarantees that there is at least one point where the derivative (slope of the tangent) equals the average rate of change over an interval.
- **Mean Value Theorem for Integrals**: Guarantees that there is at least one point where the function's value equals its average value over an interval.

#### Implicit Differentiation

Implicit differentiation is a technique used in calculus to find the derivative of a function when it is not explicitly given in the form $y = f(x)$. Instead, both variables $x$ and $y$ are given in a relation, often in the form $F(x, y) = 0$. The goal is to differentiate this relation with respect to $x$ to find $\frac{dy}{dx}$.

1. **Implicit Function**: An implicit function is one where $y$ is not isolated on one side of the equation. For example, in the equation $x^2 + y^2 = 1$, $y$ is defined implicitly in terms of $x$.

2. **Differentiation Process**:

   - Treat $y$ as a function of $x$, even though it is not explicitly written as $y = f(x)$.
   - Differentiate both sides of the equation with respect to $x$. Remember to apply the chain rule when differentiating terms involving $y$, because $y$ is a function of $x$.

3. **Chain Rule**: The chain rule is used when differentiating a composite function. When you differentiate $y$ with respect to $x$, you get $\frac{dy}{dx}$. For example, if you differentiate $y^2$ with respect to $x$, you apply the chain rule:
   $$
   \frac{d}{dx}(y^2) = 2y \cdot \frac{dy}{dx}
   $$

**Example:**<br>

Let's find $\frac{dy}{dx}$ for the equation $x^2 + y^2 = 1$:

1. **Start with the equation**:

   $$
   x^2 + y^2 = 1
   $$

2. **Differentiate both sides with respect to $x$**:

   $$
   \frac{d}{dx}(x^2) + \frac{d}{dx}(y^2) = \frac{d}{dx}(1)
   $$

3. **Apply the differentiation**:

   - The derivative of $x^2$ with respect to $x$ is $2x$.
   - The derivative of $y^2$ with respect to $x$ is $2y \cdot \frac{dy}{dx}$ (using the chain rule).
   - The derivative of a constant (1) with respect to $x$ is 0.

   So, we get:

   $$
   2x + 2y \cdot \frac{dy}{dx} = 0
   $$

4. **Solve for $\frac{dy}{dx}$**:
   - Isolate $\frac{dy}{dx}$ on one side of the equation:
     $$
     2y \cdot \frac{dy}{dx} = -2x
     $$
   - Divide both sides by $2y$ (assuming $y \neq 0$):
     $$
     \frac{dy}{dx} = -\frac{x}{y}
     $$

So, the derivative $\frac{dy}{dx}$ for the given implicit function $x^2 + y^2 = 1$ is:

$$
\frac{dy}{dx} = -\frac{x}{y}
$$

Implicit differentiation allows us to find the derivative of a variable that is defined implicitly by a relation involving another variable. By differentiating both sides of the relation with respect to $x$ and applying the chain rule, we can solve for $\frac{dy}{dx}$ even when $y$ is not isolated on one side of the equation. This technique is particularly useful in cases where it is difficult or impossible to explicitly solve for $y$ in terms of $x$.
Used when a function is not explicitly solved for one variable.

#### Logarithmic Differentiation

Logarithmic differentiation is a technique used in calculus to differentiate functions that are products, quotients, or powers of other functions. This method leverages the properties of logarithms to simplify the differentiation process, especially when dealing with complex expressions.

1. **Logarithm Properties**: The key properties of logarithms that make logarithmic differentiation useful are:

   - $\log(ab) = \log(a) + \log(b)$
   - $\log\left(\frac{a}{b}\right) = \log(a) - \log(b)$
   - $\log(a^b) = b \log(a)$

2. **Steps for Logarithmic Differentiation**:
   - **Step 1**: Take the natural logarithm $\ln$ of both sides of the function $y = f(x)$. This step transforms the function into a form that is easier to differentiate.
   - **Step 2**: Use the properties of logarithms to simplify the expression.
   - **Step 3**: Differentiate both sides of the equation with respect to $x$. Remember to apply the chain rule when differentiating the logarithm of $y$ (since $y$ is a function of $x$).
   - **Step 4**: Solve for $\frac{dy}{dx}$ by isolating it on one side of the equation.

**Example:** <br>

Let's differentiate the function $y = x^x$ using logarithmic differentiation.

1. **Start with the function**:

   $$
   y = x^x
   $$

2. **Take the natural logarithm of both sides**:

   $$
   \ln(y) = \ln(x^x)
   $$

3. **Simplify using logarithm properties**:

   $$
   \ln(y) = x \ln(x)
   $$

4. **Differentiate both sides with respect to $x$**:

   - For the left side, use the chain rule:
     $$
     \frac{d}{dx}[\ln(y)] = \frac{1}{y} \cdot \frac{dy}{dx}
     $$
   - For the right side, apply the product rule (since $x \ln(x)$ is a product of $x$ and $\ln(x)$):
     $$
     \frac{d}{dx}[x \ln(x)] = \ln(x) + x \cdot \frac{1}{x} = \ln(x) + 1
     $$

   So, we get:

   $$
   \frac{1}{y} \cdot \frac{dy}{dx} = \ln(x) + 1
   $$

5. **Solve for $\frac{dy}{dx}$**:
   - Multiply both sides by $y$:
     $$
     \frac{dy}{dx} = y (\ln(x) + 1)
     $$
   - Recall that $y = x^x$:
     $$
     \frac{dy}{dx} = x^x (\ln(x) + 1)
     $$

So, the derivative $\frac{dy}{dx}$ for the function $y = x^x$ is:

$$
\frac{dy}{dx} = x^x (\ln(x) + 1)
$$

Logarithmic differentiation is a powerful technique for differentiating functions that involve products, quotients, or powers. By taking the natural logarithm of the function, we can simplify the differentiation process using the properties of logarithms. This method is particularly useful for complex expressions where traditional differentiation rules would be cumbersome.

#### Derivatives of Some Important Functions

1.  $\frac{d}{dx} (x^n) = n \cdot x^{n-1}\quad\quad$
    $\frac{d}{dx} \left( \frac{1}{x^n} \right) = \frac{-n}{x^{n+1}}\quad\quad$
    $\frac{d}{dx} (\sqrt{x}) = \frac{1}{2\sqrt{x}} ;\quad x \neq 0$

2.  $\frac{d}{dx} [ax^n + b] = an \cdot x^{n-1}$

3.  $\frac{d}{dx} [ax + b]^n = n \cdot a (ax + b)^{n-1}$

4.  $\frac{d}{dx} [e^{ax}] = a \cdot e^{ax}$

5.  $\frac{d}{dx} [\log x] = \frac{1}{x} ; \quad\quad x > 0$

6.  $\frac{d}{dx} [a^x] = a^x \log a; \quad\quad a > 0$

7.  $\frac{d}{dx} [\sin x] = \cos x\quad\quad$
    $\frac{d}{dx} [\cos x] = -\sin x\quad\quad$
    $\frac{d}{dx} [\tan x] = \sec^2 x\quad\quad$ <br>

    $\frac{d}{dx} [\cot x] = -\csc^2 x\quad\quad$
    $\frac{d}{dx} [\sec x] = \sec x \cdot \tan x\quad\quad$
    $\frac{d}{dx} [\csc x] = -\csc x \cdot \cot x\quad\quad$

**Inverse Rule**

If $y = f(x)$ and its inverse $x = f^{-1}(y)$ is also defined, then $\frac{dy}{dx} = \frac{1}{\frac{dx}{dy}}$

### Maxima and Minima

- **Local Maximum/Minimum**: A point $(x_0, y_0)$ where the function reaches its highest or lowest value in a small surrounding neighborhood.

- **Global Maximum/Minimum**: A point $(x_0, y_0)$ where the function reaches its highest or lowest value over its entire domain.

#### Functions of one variable

**Local or relative maximum** <br>
A function $f(x)$ is said to have a Maximum at $x = c$ if there exists $\delta > 0$ such that $|x − c| <  \delta \Rightarrow f(x) \leq f(c)$.

**Local or relative minimum** <br>
A function $f(x)$ is said to have a minimum at $x = c$ if there exists $\delta > 0$ such that $|x − c| < \delta \Rightarrow f(x) \geq f(c)$.

**Stationary points** <br>
The values of $x$ for which $f(x) = 0$ are called stationary points or turning points.

**Stationary values** <br>
A function $f(x)$ is said to be stationary at $x = a$ if $f^′(a) = 0$ and $f(a)$ is a stationary value.

**Extreme point** <br>
The point at which the function has a maximum or a minimum is called an extreme point.

**Extreme values** <br>
The values of the function at extreme points are called extreme values (Extrema).

**Point of inflection** <br>
The point at which a curve crosses its tangents is called the point of inflection.
The function $f(x)$ has neither maximum nor minimum at the point of inflection.

**Note:**

1. A necessary condition for a function to have an extreme value at $x = a$ is $f'(a) = 0$.
2. $f'(a) = 0$ is only a necessary condition but not a sufficient condition for $f(a)$ to be an extreme value of $f(x)$.
3. Every extreme point is a stationary point but every stationary point need not be an extreme point.

**Rule to find maxima and minima:**<br>

Let $f(x)$ be the given function

**Step 1:** Find $f'(x)$

**Step 2:** Equate $f'(x)$ to zero to obtain the stationary points.

**Step 3:** Find $f''(x)$ at each stationary point.

- If $f''(x_0) > 0$ then $f(x)$ has a minimum at $x = x_0$
- If $f''(x_0) < 0$ then $f(x)$ has a maximum at $x = x_0$
- If $f''(x_0) = 0$ then $f(x)$ may (or) may not have extremum.

In this case, check for maxima and minima using the changes in sign of $f(x)$ as given below.

1. For $x < x_0$ if $f'(x) < 0$ and $x > x_0$ if $f'(x) > 0$ then $f(x_0)$ is a minimum value of $f(x)$.
2. For $x < x_0$ if $f'(x) > 0$ and $x > x_0$ if $f'(x) < 0$ then $f(x_0)$ is a maximum value of $f(x)$.
3. For $x < x_0$ and $x > x_0$ if $f'(x) > 0$ (or) $f'(x) < 0$ then $f(x_0)$ is not an extremum.

#### Functions of two variables:

1. **Function and Partial Derivatives**: Let $f(x, y)$ be the function. Compute the first-order partial derivatives $f_x$ and $f_y$:

$$
f_x = \frac{\partial f}{\partial x}, \quad f_y = \frac{\partial f}{\partial y}
$$

2. **Critical Points**: Solve the system of equations $f_x = 0$ and $f_y = 0$ to find the critical points $(x_0, y_0)$.

3. **Second-Order Partial Derivatives**: Compute the second-order partial derivatives:

$$
f_{xx} = \frac{\partial^2 f}{\partial x^2}, \quad f_{yy} = \frac{\partial^2 f}{\partial y^2}, \quad f_{xy} = \frac{\partial^2 f}{\partial x \partial y}
$$

4. **Hessian Determinant**: Calculate the Hessian determinant $H$ at each critical point:

$$
H = f_{xx}(x_0, y_0) f_{yy}(x_0, y_0) - [f_{xy}(x_0, y_0)]^2
$$

5. **Classification of Critical Points**:
   - If $H > 0$ and $f_{xx} > 0$, $(x_0, y_0)$ is a local minimum.
   - If $H > 0$ and $f_{xx} < 0$, $(x_0, y_0)$ is a local maximum.
   - If $H < 0$, $(x_0, y_0)$ is a saddle point (neither a maximum nor a minimum).
   - If $H = 0$, the test is inconclusive.

**Example**<br>
Let's go through an example to illustrate these steps:

Consider the function:

$$
f(x, y) = x^2 + y^2 - 4x - 6y + 13
$$

1. **First-Order Partial Derivatives**:

$$
f_x = 2x - 4, \quad f_y = 2y - 6
$$

2. **Critical Points**:
   Set $f_x = 0$ and $f_y = 0$:

$$
2x - 4 = 0 \implies x = 2
$$

$$
2y - 6 = 0 \implies y = 3
$$

So, the critical point is $(2, 3)$.

3. **Second-Order Partial Derivatives**:

$$
f_{xx} = 2, \quad f_{yy} = 2, \quad f_{xy} = 0
$$

4. **Hessian Determinant**:

$$
H = (2)(2) - (0)^2 = 4
$$

5. **Classification**:
   Since $H > 0$ and $f_{xx} = 2 > 0$, $(2, 3)$ is a local minimum.

To verify if it's a global minimum, we need to check the behavior of the function over its entire domain, but generally speaking, quadratic functions like this tend to have their local minima as global minima.

#### Absolute or Global maximum/minimum:

The absolute maximum/minimum values of the function $f(x)$ in the closed interval $[a, b]$ are given by

1. **Absolute maximum value**

   - $\max (f(a), f(b), \text{all local maximum values of } f)$
   - greatest value of $f(x)$ in $[a, b]$.

2. **Absolute minimum value**
   - $\min (f(a), f(b), \text{all local minimum values of } f)$
   - least value of $f(x)$ in $[a, b]$.

### Partial Derivatives

In calculus, a **partial derivative** of a function of multiple variables is its derivative with respect to one of those variables, with the other variables held constant. This is different from an ordinary derivative, where the function depends on a single variable.

Partial derivatives are crucial in multivariable calculus because they help us understand how a function changes as each of its variables changes. They are widely used in various fields such as physics, engineering, economics, and machine learning.

Let $f(x, y)$ be a function of two variables $x$ and $y$. The partial derivatives of $f$ with respect to $x$ and $y$ are denoted by $f_x$ and $f_y$, respectively, and are defined as:

$$
 f_x = \frac{\partial f}{\partial x} = \lim_{\Delta x \to 0} \frac{f(x + \Delta x, y) - f(x, y)}{\Delta x}
$$

$$
 f_y = \frac{\partial f}{\partial y} = \lim_{\Delta y \to 0} \frac{f(x, y + \Delta y) - f(x, y)}{\Delta y}
$$

In simple terms, $f_x$ measures the rate of change of $f$ with respect to $x$ while keeping $y$ constant, and $f_y$ measures the rate of change of $f$ with respect to $y$ while keeping $x$ constant.

**Notation** <br>

- $f_x$ or $\frac{\partial f}{\partial x}$: Partial derivative with respect to $x$.
- $f_y$ or $\frac{\partial f}{\partial y}$: Partial derivative with respect to $y$.

**Example** <br>

Consider the function $f(x, y) = x^2y + 3xy + y^3$.

1. **Partial Derivative with Respect to $x$**:

   $$
    f_x = \frac{\partial}{\partial x} (x^2y + 3xy + y^3)
   $$

   $$
    f_x = 2xy + 3y
   $$

2. **Partial Derivative with Respect to $y$**:
   $$
    f_y = \frac{\partial}{\partial y} (x^2y + 3xy + y^3)
   $$
   $$
    f_y = x^2 + 3x + 3y^2
   $$

> Partial derivatives give us the slope of the tangent line to the curve obtained by intersecting the surface $z = f(x, y)$ with a plane parallel to the respective coordinate plane.

#### Higher-Order Partial Derivatives

Just like ordinary derivatives, we can take higher-order partial derivatives. For a function $f(x, y)$, the second-order partial derivatives are:

- $f_{xx} = \frac{\partial^2 f}{\partial x^2}$: Second partial derivative with respect to $x$.
- $f_{yy} = \frac{\partial^2 f}{\partial y^2}$: Second partial derivative with respect to $y$.
- $f_{xy} = \frac{\partial^2 f}{\partial y \partial x}$ or $f_{yx} = \frac{\partial^2 f}{\partial x \partial y}$: Mixed partial derivatives.

#### Clairaut's Theorem

As mentioned earlier, for functions with continuous second-order partial derivatives, the mixed partial derivatives are equal:

$$
 f_{xy} = f_{yx}
$$

#### Applications

Partial derivatives are used in numerous applications, including:

1. **Gradient**: The gradient of a function $f(x, y)$ is a vector that points in the direction of the steepest ascent. It is denoted by $\nabla f$ and is given by:

   $$
    \nabla f = \left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right)
   $$

2. **Tangent Planes**: The equation of the tangent plane to the surface $z = f(x, y)$ at the point $(x_0, y_0, z_0)$ is:

   $$
    z - z_0 = f_x(x_0, y_0)(x - x_0) + f_y(x_0, y_0)(y - y_0)
   $$

3. **Optimization**: In optimization problems, partial derivatives are used to find local maxima, minima, and saddle points of functions with several variables.

#### Example Problems

1. **Find the Partial Derivatives**:
   For the function $g(x, y) = \sin(x) \cos(y)$:

   $$
   g_x = \frac{\partial g}{\partial x} = \cos(x) \cos(y)
   $$

   $$
   g_y = \frac{\partial g}{\partial y} = -\sin(x) \sin(y)
   $$

2. **Compute the Gradient**:
   For $h(x, y) = x^2 + y^2$:
   $$
   \nabla h = \left( \frac{\partial h}{\partial x}, \frac{\partial h}{\partial y} \right) = (2x, 2y)
   $$

#### Visual Representation

Let's visualize partial derivatives with a simple 3D surface. Suppose we have a surface $z = f(x, y)$, and we slice it with planes parallel to the $x$- and $y$-axes:

- **Slice Parallel to $yz$-Plane**: Fix $x = x_0$. The curve is $z = f(x_0, y)$. The slope of this curve at $y = y_0$ is $f_y(x_0, y_0)$.
- **Slice Parallel to $xz$-Plane**: Fix $y = y_0$. The curve is $z = f(x, y_0)$. The slope of this curve at $x = x_0$ is $f_x(x_0, y_0)$.

In summary, partial derivatives help us understand how functions of multiple variables change with respect to each variable independently. They are the cornerstone of multivariable calculus.

## INTEGRATION

### Indefinite Integrals

If $f(x)$ and $g(x)$ are two functions of $x$ such that $g'(x) = f(x)$, then the integral of $f(x)$ is $g(x)$. Further, $g(x)$ is called the antiderivative of $f(x)$.

The process of computing an integral of a function is called Integration and the function to be integrated is called integrand.

An integral of a function is not unique. If $g(x)$ is any one integral of $f(x)$, then $g(x) + C$ is also its integral, where $C$ is any constant termed as constant of integration.

#### Standard Formulae

1.

$$
\int x^n \, dx = \frac{x^{n+1}}{n+1} + c \quad (n \ne -1)
$$

2.

$$
\int (ax + b)^n \, dx = \frac{(ax + b)^{n+1}}{(n+1)a} + c \quad (n \ne -1)
$$

3.

$$
\int \frac{1}{x} \, dx = \log x + c
$$

4.

$$
\int \frac{1}{ax + b} \, dx = \frac{\log (ax + b)}{a} + c
$$

5.

$$
\int a^x \, dx = \frac{a^x}{\log a} + c
$$

6.

$$
\int e^x \, dx = e^x + c
$$

7.

$$
\int \sin x \, dx = -\cos x + c
$$

8.

$$
\int \cos x \, dx = \sin x + c
$$

9.

$$
\int e^{ax} \, dx = \frac{e^{ax}}{a} + c
$$

10.

$$
\int \sec^2 x \, dx = \tan x + c
$$

11.

$$
\int \csc^2 x \, dx = -\cot x + c
$$

12.

$$
\int \sec x \tan x \, dx = \sec x + c
$$

13.

$$
\int \csc x \cot x \, dx = -\csc x + c
$$

14.

$$
\int \tan x \, dx = \log (\sec x) + c
$$

15.

$$
\int \cot x \, dx = \log (\sin x) + c
$$

16.

$$
\int \sec x \, dx = \log (\sec x + \tan x) + c
$$

17.

$$
\int \csc x \, dx = \log (\csc x + \cot x) + c
$$

18.

$$
\int \frac{1}{1-x^2} \, dx = \sin^{-1} x + c \quad \text{or} \quad -\cos^{-1} x + c
$$

19.

$$
\int \frac{1}{1+x^2} \, dx = \tan^{-1} x + c \quad \text{or} \quad -\cot^{-1} x + c
$$

20.

$$
\int \frac{1}{\sqrt{1-x^2}} \, dx = \sec^{-1} x + c \quad \text{or} \quad -\csc^{-1} x + c
$$

21.

$$
\int \sinh x \, dx = \cosh x + c
$$

22.

$$
\int \cosh x \, dx = \sinh x + c
$$

23.

$$
\int \tanh x \, dx = \log (\cosh x) + c
$$

24.

$$
\int \coth x \, dx = \log (\sinh x) + c
$$

25.

$$
\int \text{sech} x \, dx = \tan^{-1} (\sinh x) + c
$$

26.

$$
\int \text{csch} x \, dx = \log (\tanh (\frac{x}{2})) + c
$$

27.

$$
\int f(g(x))g'(x) \, dx = \int f(u) \, du = F(g(x)) + c
$$

28.

$$
\int \frac{f'(x)}{f(x)} \, dx = \log |f(x)| + c
$$

29.

$$
\int \frac{f'(x)}{[f(x)]^n} \, dx = \frac{[f(x)]^{1-n}}{1-n} + c
$$

30.

$$
\int \frac{dx}{\sqrt{a^2 - x^2}} = \sin^{-1} \frac{x}{a} + c
$$

31.

$$
\int \frac{dx}{\sqrt{a^2 + x^2}} = \sinh^{-1} \frac{x}{a} + c \quad \text{or} \quad \log \left| x + \sqrt{a^2 + x^2} \right| + c
$$

32.

$$
\int \frac{dx}{\sqrt{x^2 - a^2}} = \cosh^{-1} \frac{x}{a} + c \quad \text{or} \quad \log \left| x + \sqrt{x^2 + a^2} \right| + c
$$

33.

$$
\int \frac{1}{x^2 + a^2} dx = \frac{1}{a} \tan^{-1} \left( \frac{x}{a} \right) + c
$$

34.

$$
\int \frac{1}{x^2 - a^2} dx = \frac{1}{2a} \log \left| \frac{x - a}{x + a} \right| + c
$$

35.

$$
\int \frac{1}{a^2 - x^2} dx = \frac{1}{2a} \log \left| \frac{a + x}{a - x} \right| + c
$$

36.

$$
\int \sqrt{a^2 - x^2} dx = \frac{x \sqrt{a^2 + x^2}}{2} + \frac{a^2}{2} \sin^{-1} \frac{x}{a} + c
$$

37.

$$
\int \sqrt{a^2 + x^2} dx = \frac{x \sqrt{a^2 + x^2}}{2} + \frac{a^2}{2} \sinh^{-1} \frac{x}{a} + c
$$

38.

$$
\int \sqrt{x^2 - a^2} dx = \frac{x \sqrt{x^2 - a^2}}{2} - \frac{a^2}{2} \cosh^{-1} \frac{x}{a} + c
$$

39.

$$
\int \log x \, dx = x (\log x - 1) = x \log \left( \frac{x}{e} \right) + c
$$

40.

$$
\int e^x [f(x) + f'(x)] dx = e^x f(x) + c
$$

### Definite Integrals

The difference in the values of an integral of a function $f(x)$ for two assigned values say $a, b$ of the independent variable $x$, is called the Definite Integral of $f(x)$ over the interval $[a, b]$ and is denoted by $\int_{a}^{b} f(x)dx$.

The number ‘$a$’ is called the lower limit and the number ‘$b$’ is the upper limit of integration.

If $f(x)$ is a function of $x$ continuous in $[a, b]$, then

$$
 \int_{a}^{b} f(x)dx = g(b) - g(a)
$$

where $g(x)$ is a function such that

$$
 \frac{d}{dx} g(x) = f(x).
$$

#### Properties

1. If $f(x)$ is a continuous function of $x$ over $[a, b]$, and $c$ belongs to $[a, b]$, then <br>
   $\int_{a}^{b} f(x)dx = \int_{a}^{c} f(x)dx + \int_{c}^{b} f(x)dx.$

2. If $f(x)$ is a continuous function of $x$ over $[a, b]$, then<br>
   $\int_{a}^{b} Kf(x)dx = K \int_{a}^{b} f(x)dx.$

3. If $f(x)$ is a continuous function of $x$ over $[a, b]$, then<br>
   $\int_a^b f(x)dx = -\int_b^a f(x)dx.$

4. If $f(x)$ is continuous in some neighbourhood of $a$, then<br>
   $\int_a^a f(x)dx = 0.$

5. If $f(x)$ and $g(x)$ are continuous in $[a, b]$, then<br>
   $\int_a^b [f(x) + g(x)]dx = \int_a^b f(x)dx + \int_a^b g(x)dx.$

6. $\int_a^b f(x)dx = \int_a^b f(z)dz = \int_a^b f(t)dt.$

7. $\int_0^a f(x)dx = \int_0^a f(a - x)dx.$

8. $\int_{-a}^a f(x)dx = 0, \text{ if } f(x) \text{ is odd}.$

9. $\int_{-a}^a f(x)dx = 2 \int_0^a f(x)dx \text{ if } f(x) \text{ is even}.$

10. $\int_0^{2a} f(x)dx = 2 \int_0^a f(x)dx, \text{ if } f(2a - x) = f(x) = 0 \text{ if } f(2a - x) = -f(x)$

11. $\int_0^{na} f(x)dx = n \int_0^a f(x)dx, \text{ if } f(a + x) = f(x)$
