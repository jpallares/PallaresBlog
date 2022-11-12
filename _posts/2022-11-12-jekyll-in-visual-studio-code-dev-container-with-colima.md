---
toc: true
toc_label: 'Contents'
title: Use Jekyll with Visual Studio Code Dev Containers and Colima
tags: [jekyll, vscode, container, docker, blog, setup]
excerpt: Forget about configuration and go straight to write posts
header:
  teaser: /images/vs-code-dev-container-colima.png
lang: en
ref: vscodedevcontainer
---

## Intro

Configuring the dev environment can be difficult. [One example is this blog](https://juan.pallares.me/configure-jekyll-multi-language-without-plugin/), it requires ruby, some """amazing""" rubygems, etc. configuring it in MacOS is hard, in Windows is directly a nightmare. Recently, I tried to write a post from a new laptop, the moment I saw I could not build the jekyll site I desisted. I pushed to a branch and built in another machine. Then I learned about [Visual Studio Code Dev Containers](https://code.visualstudio.com/docs/devcontainers/containers).

## Automate Dev Container creation 🤖

So can I configure a container and build my blog directly there? Can I forget about configuring Jekyll in each machine I want to blog from? Yes you can!

<iframe src="https://giphy.com/embed/SWuKsQEzr42m1X0pec" width="480" height="480" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

Ok cool, but how do I configure the container? that will be hard! well, I have good news, there are predefined examples and the Jekyll one works out of the box. [Check the documentation](https://code.visualstudio.com/docs/devcontainers/create-dev-container#_automate-dev-container-creation), you just need to:

- Open Command Palette (`F1`)
- Select `Dev Containers: Add Dev Container Configuration Files`
- Look for the `Jekyll` one

## I don't have Docker Desktop :whale:

One of the requirements to run VS Code Dev Containers is having Docker Desktop. If you don't have it and you are using a Mac, I got you covered, meet [Colima](https://github.com/abiosoft/colima).

Steps to install:

- Uninstall previous Docker Desktop App and related files. If you used brew to install, you can use: `brew uninstall --cask docker`
- Then run `brew install colima`
- Install dependencies `brew install docker docker-compose`
- Finally run it `colima start`

And that's it, VS Code Dev Containers will works flawlessly. Be aware Colima by default uses 2 CPUs, 2GiB memory and 60GiB storage but this can be configured.

### Known issues

Once you get into the container there is no git anymore => To solve it, run `git status`. It will suggest a command like `git config --global --add safe.directory /path/to/repo`. Run it and git will be back.

## Conclusion

I'll keep an any for more automated containers, they can be super helpful when the environment configuration is complex. Are you planning to use it for any of your projects?
