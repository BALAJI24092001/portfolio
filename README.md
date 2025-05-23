## Building Portfolio

Install `HUGO` using chocolatey in windows

```
choco install hugo
pip install hugo
```

Build the website using the below command

```
hugo new site <website name>
cd <website name>
```

Select a HUGO theme and get the theme inside the project.

```
git clone https://github.com/adityatelange/hugo-PaperMod themes/PaperMod --depth=1
```

Add a new post using the below command.

```
hugo new content content/posts/my-first-post.md
```

Get a localhost to run your website on your local system using the below command.

```
hugo server
hugo server -D # for draft posts to show in the localhost
```

NOTE: Add the two files in the layouts/partials/ to render latex in markdown posts.

<!-- TODO: Learn how hugo environment is structured. -->
