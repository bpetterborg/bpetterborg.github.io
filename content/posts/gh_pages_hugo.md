+++
draft = false
date = 2021-03-25T18:53:44-04:00
title = "Host Hugo w/ Github Pages"
slug = ""
series = ["Hugo","Github Pages"]
authors = ["Ben Petterborg"]
+++

Table of Contents
=================
1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
3. [Prepare your environment](#prepare-your-environment)
4. [Building your site](#building-your-site)

## Introduction
I had a bit of difficulty setting up Hugo to work with Github Pages,
so I decided to document how I was able to make it work.

## Getting Started
This guide assumes you already have a Hugo site. If you do not,
you can learn how to [here](https://gohugo.io/getting-started/quick-start/).

You will also need a Github Pages repo setup, these are pretty simple,
and you can use [this](https://guides.github.com/features/pages/) guide.

Both of these are pretty simple to setup, but if you have any questions,
ask Google first, but if that doesn't work, leave a comment below and I'll be happy to help.

## Prepare your environment
After you've created your site repo, delete the contents. Once that's done,
head to wherever you wish to keep it on your local machine and clone it.

Once you're done, `cd` to it and create an empty file named `.nojekyll`

``` Bash
touch .nojekyll
```

After that, go ahead and generate your site with Hugo. If you've already made your site and want to
migrate to Github Pages, just copy the contents over to the new repo.

Now, we'll need to edit the `config.toml` to configure the site to be compatible with Github Pages.

``` Bash
vim config.toml
```

Add the following line, under the top set of variables
``` TOML
publishDir = "docs"
```

Go to your Repo>Settings>Github Pages> and set `Source` directory to `/docs`

## Building your site

Go to the folder where you have your site and run `hugo`.

Now that your site has been built, add all, commit, and push to Github.
