---
title: "12 3 2022 Changing Themes"
date: 2022-12-13T23:37:15-07:00
draft: false
tags: ["Blog","Work-Log"]
---

## Introduction
It is 23:37, do you know where your kids are?

So there are a few changes as I am customizing this thing. Changed from the default theme - Sorry Hugo folks, it is nice, but hard to customize. The new theme is switching from ananke to binario. But I am getting ahead of myself. Let me start by explaining it from the beginning.

## Setup
For this project, I am using my M1 Macbook Pro with Visual Studio Code as the coding platform. This will change depending on what work machine i am working on - I have a VM on a self hosted server (Windows 10), a Desktop PC, Razer Blade 15 laptop, and a phone that could be used for .md file edits. I am deploying this site to GitHub Pages via github actions and github environments, and have a rudementary pipeline in place that builds the site's static pages using Hugo(Go lang) and then publishes to a branch that is published to the GitHub Page.

The URL comes from GoDaddy where I have it reserved, and the basic CNAME and A Records pointed to github DNS.

The goal of this is to allow offline edits that can be synced, with a clear language to do so. With Markdown (.md) you can do this via a simple text editor found on many devices. I'm sure with a kindle and a web browser I could update this site.

## Changing themes in Hugo
To start, adding a theme is super easy. In Terminal, navigate to the root directory and run a git submodule like the following:

`git submodule add https://github.com/vimux/binario themes/binario`

This will create a submodule that allows the template to be updated as it changes or is secured. I chose a template for simplicity sake, as the repo is for project notes and blog posts, and build my own would just use a lot of time that could be used on other, more personally relevant pages.

Once it is in, Hugo is pretty slick. Running a command like `hugo` will build the static site. `hugo server` will build the site and then host it on local host. It also allows the creation of site pages that are formatted for the template by adding `hugo new XXX`
To create this post, i rant the following:
`hugo new post/Changing-Themes.md`

This went through and created the page, and formatted it for editing.

After changing the theme, the first post required some edits to clarify formatting to the new template, but for the most part, it is all in markdown, that the site then interpretes - which is the simplicity I was looking for.

Link to the theme:
[binario theme](https://themes.gohugo.io/themes/binario/)

## Special note on Markdown
I am also using this cheat sheet, which I may make as a post here just so that we can all have a cheat sheet. :)

Link to Markdown [cheat sheet](https://www.markdownguide.org/cheat-sheet/)
