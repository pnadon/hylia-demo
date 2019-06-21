---
layout: layouts/post.njk
title: 'Hylia, a tool for easily generating and deploying a static website'
metaTitle: hylia-tutorial
date: 2019-06-21T04:42:21.601Z
tags:
  - inside
  - website
---
## Introduction
This tutorial will help you with setting up your own website / blog, using Hylia. While other services allow you to make
your own website, they are either paywalled, riddled with ads, or limited in functionality. Using a static site
generator such as Hylia (or equivalent) will give you full control over what goes on your website.

## Requirements

This tutorial requires that you have completed the setup tutorial, or that you at least have a GitHub account and text editor.

## Definitions

According to the official site, Hylia is a _Eleventy starter kit with Netlify CMS preconfigured_. Let's break down what
that means:

- Eleventy is a _static site generator_. This means you can quickly and easily type up content, and then run Eleventy to convert it into a website. A _static site_ is a site that does not retain information, meaning you cannot make user accounts or other dynamic content. If you wish to change the website (such as add a blog post), you must code it in yourself and then run _Eleventy_ to re-build the site. This sounds harder than it is, because _Eleventy_ ensures the process is easy!
- Netlify is a service that lets you deploy a GitHub repository as a website. This means you as a developer push your website's code to your repository, Eleventy builds it, and then Netlify distributes it for the world to see.
- Netlify CMS is a _content manager_, which essentially makes adding a new post or extra content to your site extremely easy.

Combined, these technologies form the basis of Hylia, so as you can see Hylia gives you the best of both worlds; an
easily-accessible and free way to build a website, and control over the most minute details of your site when you need
it.

## Getting started
If you'd like a video tutorial, [this](https://www.youtube.com/watch?v=0hM_0BH-Y_A&feature=youtu.be) is a very good one.

1. Go on the [Hylia website](https://hylia.website/) and click the _deploying Hylia to Netlify_ button.
2. You will be asked for your GitHub credentials, which you will need to enter to make a new repository
3. You will be prompted to name your repository. The kebab-style naming is typical for GitHub repositories (eg my-website-name).
4. Netlify will begin building the site, once it is done you can click the randomly-generated url, and see that your website is up and running!

## Identity

To enable some features we must first enable _Identity_ by going to your website's page on Netlify, clicking the
_Settings_ tab, then _Identity_ in the left-hand list, and clicking the blue _Enable_ button.

Afterwards scroll all the way down and click on "Enable Git Gateway"

Lastly, click the _Identity_ tab at the top, click on "Invite Users", and enter your own email.

Check your email for the invite link, and set up a password for your admin account.

## Content Manager

Now if you go on your site, and visit the `/admin` page (eg [https://awesome-jang-410844.netlify.com/admin](https://awesome-jang-410844.netlify.com/admin)),
you will see an interface for posting and managing your site. From this point on I advise playing around. Check the following links to know how to
configure your site, and how to use Markdown if you arent familiar.

- [GitHub-flavored Markdown](https://help.github.com/en/articles/basic-writing-and-formatting-syntax)
- [Hylia](https://github.com/andybelldesign/hylia)

## Cloning and updating your website locally

While the content manager offers many features, if you wish to have full control over the look and content of your
website, you can clone your Github repository to your compute, and open up the project in your favorite text editor.

### Clone the repository
Using GitHub Desktop, clone your repository to a folder on your computer **that you will remember** (organization is key!),
and then click on the "Open in Visual Studio Code" button, if you chose VSCode as your preferred editor.

### Modifying the website
From here, you can see the entire makeup of your website. Things such as your website's theme, posts, etc. are all accessible and customizeable here.

If you wish to test and build your website locally, you can do so by installing the `eleventy` CLI tool from *npm*, the node package manager.
If you already installed NodeJS, then you have npm, and can install *eleventy* by entering `npm install -g @11ty/eleventy`.

See [this link](https://www.11ty.io/) for documentation on how to use *eleventy*.

### Push your changes
Once you have made your changes, commit and push your changes using the GitHub Desktop application, to update your
actual website.

## BONUS! Dark Theme
The default theme for Hylia is nice, but wouldnt it be sweet if it you changed it into a Dark-Mode style theme? See if 
you can clone the project to your local machine, and then mess around with the theme to customize it the way you want!
