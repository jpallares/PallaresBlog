---
toc: true
toc_label: 'Contents'
title: Book - The Art of Unit Testing, 2nd Edition - Roy Osherove
tags: [books, unit testing, integration testing, unit of work, stub, fake, mock]
excerpt: It's never too late to realize about mistakes I've been doing while testing
lang: en
ref: artofunittesting
---

## Intro

## Dev container

## Predefined Jekyll one

## Colima

Preface
As you may know - in light of Docker Desktop licensing costs, we have to switch to alternatives. It is not a deal for Linux or Windows users (because of WSL). macOS users are less fortunate.

I am aware of two most popular Docker Desktop alternative setups on macOS:

Podman + podman-compose
Colima
Tried both and found Colima the most user-friendly solution. Most importantly, it works well with docker-compose out of the box.

Find a short migration guide below.

Switching from Docker Desktop to Colima on macOS
This is a short guide how to ditch Docker Desktop on macOS

Uninstall Docker Desktop
First, you need to remove Docker Desktop App and related files.

Follow this guide
Be aware: This will destroy Docker containers, images, volumes, and other Docker related data local to the machine.

Unfortunately, it did not work for me entirely, so here is a list of files and directories to remove manually:

sudo rm -Rf /Applications/Docker.app
sudo rm -f /usr/local/bin/docker
sudo rm -f /usr/local/bin/docker-machine
sudo rm -f /usr/local/bin/com.docker.cli
sudo rm -f /usr/local/bin/docker-compose
sudo rm -f /usr/local/bin/docker-compose-v1
sudo rm -f /usr/local/bin/docker-credential-desktop
sudo rm -f /usr/local/bin/docker-credential-ecr-login
sudo rm -f /usr/local/bin/docker-credential-osxkeychain
sudo rm -f /usr/local/bin/hub-tool
sudo rm -f /usr/local/bin/hyperkit
sudo rm -f /usr/local/bin/kubectl.docker
sudo rm -f /usr/local/bin/vpnkit
sudo rm -Rf ~/.docker
sudo rm -Rf ~/Library/Containers/com.docker.docker
sudo rm -Rf ~/Library/Application\ Support/Docker\ Desktop
sudo rm -Rf ~/Library/Group\ Containers/group.com.docker
sudo rm -f ~/Library/HTTPStorages/com.docker.docker.binarycookies
sudo rm -f /Library/PrivilegedHelperTools/com.docker.vmnetd
sudo rm -f /Library/LaunchDaemons/com.docker.vmnetd.plist
sudo rm -Rf ~/Library/Logs/Docker\ Desktop
sudo rm -Rf /usr/local/lib/docker
sudo rm -f ~/Library/Preferences/com.docker.docker.plist
sudo rm -Rf ~/Library/Saved\ Application\ State/com.electron.docker-frontend.savedState
sudo rm -f ~/Library/Preferences/com.electron.docker-frontend.plist
sudo rm -f /var/run/docker.sock
If you installed docker with brew install --cask docker
run:

brew uninstall --cask docker
Install Colima and dependencies
brew install colima
brew install docker
brew install docker-compose
Here, besides the Colima, we are installing Docker client and Docker Compose binary (we removed them when uninstalled Docker Desktop).

Configure and start Colima
Here I am providing example with custom configured parameters (be default Colima starts with 2 CPUs, 2GiB memory and 60GiB storage.)

The below command will create a Virtual Machine(VM) with Docker runtime.
Note: Disk size cannot be changed after the VM is created.

colima start --cpu 2 --memory 4 --disk 30
More about customising VM here.

That's it! 🎉 🎉 🎉 You have a working Docker setup.

Try to spin up your services defined in docker-compose.yml:

docker-compose up
Issues? Check troubleshooting section below 👇

