# Templates
These are my $\LaTeX$ templates that I use for homework or anything else (apart from my resume, which is [here](https://github.com/ravibrock/resume)). To use, copy them into your project's directory and source the main file for each package. Additional directions are below:

## Homework
To use this, source `homework.sty` and it will source all the other packages. To add an image to the title page, use `\logo{image.png}` in your document's source code.

### Submodule setup
I use this as a git submodule so that it's easy to sync with the central repo. To do this, I run `git submodule add https://github.com/ravibrock/latex-templates` and put the following snippet in my document's preamble:
```tex
\usepackage{import}
\usepackage{silence}\WarningFilter{latex}{You have requested package}
\import{latex-templates/math}{homework.sty}
```
This imports the packages, since `\usepackage` doesn't work well with folders, and silences the requested package warning thrown by `import` since it's unhelpful and nothing is broken.
