# tic.bookdown

<!-- badges: start -->
[![Travis build status](https://travis-ci.org/ropenscilabs/tic.bookdown.svg?branch=master)](https://travis-ci.org/ropenscilabs/tic.bookdown)
[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/ropenscilabs/tic.bookdown?branch=master&svg=true)](https://ci.appveyor.com/project/ropenscilabs/tic-package)
<!-- badges: end -->

This is a minimal example of a book based on R Markdown and **bookdown** (https://github.com/rstudio/bookdown), built and deployed by _tic_. 
_tic_ is an R package for CI-agnostic workflow definitions for various R projects. 
See its [documentation](https://ropenscilabs.github.io/tic/) for more information.

## Comparing to a conventional setup

Only a few files are added or changed to enable integration with _tic_:

- [`tic.R`](tic.R): This file describes the CI workflow.
- [`.travis.yml`](.travis.yml): This file translates between CI stages of Travis CI and _tic_ stages.
- [`.Rbuildignore`](.Rbuildignore): The files listed above are not part of a built R package and must be excluded.

## Set up an operational fork of this repository

If you want to experiment with _travis_ and _tic_ in this repo, you can fork it.

1. Use `usethis::create_from_github()` to automatically create a fork of this repo.
    If you use RStudio, a new RStudio project will open. 
    You may need to set up your SSH credentials first. See [this guide](http://happygitwithr.com/ssh-keys.html) if you're having problems. 
    (It's definitely worth getting this function running as it saves you so much time in the future!) 
    Alternatively, fork this repo on Github and then create a new R Project within RStudio (File -> New Project -> Version Control -> Github). 
1. Run `tic::use_tic()` to set up all requirements needed for the CI integration of your package.

## Accessing the rendered book

The rendered version of the book lives in the `gh-pages` branch (which will be automatically created if missing) and is served via _Github Pages_ using the following URL scheme: `https://<username>.github.io/<repo-name>`.
