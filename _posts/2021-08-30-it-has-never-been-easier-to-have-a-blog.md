---
toc: true
toc_label: "Contents"
title: It has never been easier to have a blog with Github Pages
tags: [blog, jekyll, github pages, markdown, vercel, multi-language]
excerpt: With jekyll and github pages you just have to worry about the content
lang: en
ref: easy-blog
---

It's been 7 years since [I migrated the blog from Blogger to Github Pages + Jekyll](https://juan.pallares.me/moving-to-jekyll/){:target="\_blank"}. Back at that time, I was totally new to Git. I used a Windows machine to build the blog and I remember [it was a nightmare to install Ruby and make it work properly](https://juan.pallares.me/jekyll-windows/){:target="\_blank"}. Also, I forked the theme I used and I never updated it. Anyway, I managed to maintain the blog active. Enough old stories, now it's extremely easy to have a blog like this one.

## Github pages in Github

You can have a [site up and running in 5 steps](https://pages.github.com/). It has to be public and by default the domain is `yourusername.github.io`. You can configure your own custom domain. Having a [Jekyll blog has more steps](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll){:target="\_blank"} but it's also pretty easy. Summary:

- Easy setup
- Public repo
- Short amount of themes
- Ability to set you own custom domain

### Github not accessible

A Spanish internet provider, Movistar, had a bug that make Github unreachable. This is the main provider in Spain so suddenly the blog was down for a lot of people.
I decided to deploy the blog somewhere else, that means, use Github as repo but deploy the jekyll build process output to another provider. I went for [Vercel](https://vercel.com/), the same place I deploy the [Net Salary Calculator](https://tusueldoneto.pallares.me){:target="\_blank"}.

Here is when I discovered how outdated and how custom was my good old jekyll blog. I took the chance to rebuild the blog from scratch. At the end it was just creating a new jekyll blog and then moving there my posts and pages.

## Github pages + Vercel + Minimal Mistakes theme

Vercel has a template for Jekyll that works out of the box so you just have to pick your repo from the menu and leave the other options as default. It will be deployed in a minute. Good thing about using Vercel? I have a more generic Jekyll version so I can use my favourite Jekyll theme, [minimal mistakes](https://github.com/mmistakes/minimal-mistakes). [It comes now as a gem](https://github.com/mmistakes/minimal-mistakes#gem-based-method) so I won't have problems updating. I made some custom changes to the [layouts provided so my posts can be multilanguage](https://juan.pallares.me/configure-jekyll-multi-language-without-plugin/) and I can override the layouts to keep this functionality. I just had to create the `_layouts` folder and inside set the files I want to override.

Main advantages, same as Github plus:
- Repo can be made private
- You can set any Jekyll theme you want

Have a look at [the source code](https://github.com/jpallares/PallaresBlog), you could replace the `_posts` files with your own ones, configure the `_config.yml` with your data and have your own blog in minutes.