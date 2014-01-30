---
layout: post
title: 'Tutorial: How to use Git to deploy and update a website Pt. 1'
date: '2012-06-11T17:55:06-07:00'
tags: 
tumblr_url: http://blog.lovellfelix.com/post/24913411212/tutorial-how-to-use-git-to-deploy-and-update-a-website
---
The HTML source for web site lives in a Git repository on a local workstation. This page describes how I set things up so that I can make changes live by running just “git push web”.
The one-line summary: push into a remote repository that has a detached work tree, and a post-receive hook that runs “git checkout -f”.
The local repository
It doesn’t really matter how the local repository is set up, but for the sake of argument, let’s suppose you’re starting one from scratch.
$ mkdir website && cd website$ git initInitialized empty Git repository in /home/projects/website/.git/$ echo ''Hello, world!'' > index.html$ git add index.html$ git commit -q -m "The humble beginnings of my web site."
The remote repository
I assume that the web site will live on a server to which you have ssh access, and that things are set up so that you can ssh to it without having to type a password.

On the server, we create a new repository to mirror the local one.
$ mkdir website.git && cd website.git$ git init --bare --sharedInitialized empty Git repository in /home/project/website.git/
Then we define (and enable) a post-receive hook that checks out the latest tree into the web server’s DocumentRoot (this directory must exist; Git will not create it for you):
$ mkdir /var/www/www.example.org$ cat > hooks/post-receive#!/bin/shGIT_WORK_TREE=/var/www/www.example.org git checkout -f$ chmod +x hooks/post-receive
Back on the workstation, we define a name for the remote mirror, and then mirror to it, creating a new “master" branch there.
$ git remote add web ssh://user@server.example.org/home/project/website.git$ git push web master
