---
layout: post
title: 'Tutorial: How to use Git to deploy and update a website Pt. 1'
date: '2012-06-11T17:55:06-07:00'
tags:

author:
  name: Lovell Felix
  twitter: lovellfelix
  gplus: 102676824509364241023
  bio: Geek, Google Fanboy, Tech News Junkie, Entrepreneur - Drinker of tea :)
  image: https://lh3.googleusercontent.com/-Ubq3pEfgeLk/AAAAAAAAAAI/AAAAAAAAOvs/nGutWDQ5OGc/s120-c/photo.jpg.png

tumblr_url: http://blog.lovellfelix.com/post/24913411212/tutorial-how-to-use-git-to-deploy-and-update-a-website

---

<b>The Problem:</b>

<blockquote> I routinely push the changes I made on my website to a remote server that stores my git repositories, and host the website. It's somewhat redundant, because after I push the updates I made using git I use an FTP client to upload the same files to the same server o.0. Yes! There must be a way to automate this process, and <b>kill two birds with one stone</b>. </blockquote>

<h3>Solution?</h3>

- Push changes to Git remote server, and update website with one command.

-- push into a remote repository that has a detached work tree, and a post-receive hook that runs “git checkout -f”

This tutorial outlines the steps I took to make changes live by running just <b>“git push web”</b>.


<b>The local repository</b>


It doesn’t really matter how the local repository is set up, but for the sake of argument, let’s suppose you’re starting one from scratch.

{% highlight bash linenos%}
mkdir website && cd website
echo ''Hello, world!'' > index.html
git add index.html
git commit -q -m "The humble beginnings of my web site."

{% endhighlight %}

<b>The remote repository</b>
I assume that the web site will live on a server to which you have ssh access, and that things are set up so that you can ssh to it without having to type a password.

On the server, we create a new repository to mirror the local one.

{% highlight scss %}
mkdir website.git && cd website.git

git init --bare --shared

//Initialized empty Git repository in /home/project/website.git/
{% endhighlight %}

Then we define (and enable) a post-receive hook that checks out the latest tree into the web server’s DocumentRoot (this directory must exist; Git will not create it for you):

{% highlight scss %}
mkdir /var/www/www.example.org
cat > hooks/post-receive
#!/bin/sh
GIT_WORK_TREE=/var/www/www.example.org g
it checkout -f
chmod +x hooks/post-receive
{% endhighlight %}

Back on the workstation, we define a name for the remote mirror, and then mirror to it, creating a new “master" branch there.

{% highlight scss %}
git remote add web ssh://user@server.example.org/home/project/website.git
git push web master
{% endhighlight %}