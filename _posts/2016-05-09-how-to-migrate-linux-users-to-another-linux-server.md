---
layout: post
title: 'Notes: Migrate Linux users to another Linux server'
date: '2015-04-01T23:31:00-07:00'
tags:

author:
  name: Lovell Felix
  twitter: lovellfelix
  gplus: 102676824509364241023
  bio: Geek, Google Fanboy, Tech News Junkie, Entrepreneur - Drinker of tea :)
  image: https://lh3.googleusercontent.com/-Ubq3pEfgeLk/AAAAAAAAAAI/AAAAAAAAOvs/nGutWDQ5OGc/s120-c/photo.jpg.png
---

<div class="alert-message alert-message-danger">
  <h4>The Problem</h4>
  <p>I have a Debian 5.0.4 virtual machine that's no longer supported and my shop is pretty much a CentOS ecosystem. The server is primary use for sFTP with over 250 user accounts.</p>
</div>

**The PLAN:** Migrate from Debain 5 to CentOS7, and avoid manually recreating user accounts or generating new passwords. Sounds easy right? Actually, it was and wasn't as time consuming as I anticipated or took a lot effort to get all the user accounts including the host directory over to the new server.

I outlined the steps in gist below:

{% gist 9b7181b218ab02b4314e7ccd0194bbe2 %}

FYI: Linux is awesome! :D
