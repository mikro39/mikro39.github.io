---
title: "12 3 2022 Changing Themes"
date: 2022-12-13T23:37:15-07:00
draft: false
tags: ["Blog","Work-Log"]
---

## Introduction
It is 23:37, do you know where your kids are?

So a few changes as i am customizing this thing. Changed from the default theme - Sorry Hugo folks, it is nice, but hard to customize.

## Setup
For this project, i am using my M1 Macbook Pro with Visual Studio Code. I am deploying this site to GitHub Pages, and have a rudementary pipeline in place that builds using Hugo, the site and publishes to a branch that is published to the GitHub Page.

The URL comes from GoDaddy where i have it reserved, and using DNS at GoDaddy.

## Changing themes in Hugo
To start, adding a theme is super easy. In Terminal, navigate to the root directory and run a script like the following:

`git submodule add https://github.com/vimux/binario themes/binario`

This will create a submodule that allows you to change the layout.

To create a new page:
`hugo new post/12-3-2022-Changing-Themes.md`

Link to the theme:
[binario theme](https://themes.gohugo.io/themes/binario/)

Link to Markdown [cheat sheet](https://www.markdownguide.org/cheat-sheet/)
