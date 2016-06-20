---
layout: post
title: 'Notes: Migrate Linux users to another server'
date: '2016-05-09T23:31:00-07:00'
tags: 

author:
  name: Lovell Felix
  twitter: lovellfelix
  gplus: 102676824509364241023
  bio: Geek, Google Fanboy, Tech News Junkie, Entrepreneur - Drinker of tea :)
  image: https://lh3.googleusercontent.com/-Ubq3pEfgeLk/AAAAAAAAAAI/AAAAAAAAOvs/nGutWDQ5OGc/s120-c/photo.jpg.png
---


FYI: Linux is awesome! :D

<div class="alert-message alert-message-danger">
  <h4>The Problem</h4>
<p>Debian 5.0.4 VM that's way past its end of life. The server is used primary for sFTP. It has over 100 user accounts. So Yeah! Updating 100 user accounts credentials will time consuming. Also, my shop is pretty much a CentOS Shop.</p>
</div>

I'm moving from Debain 5 to CentOS7 sounds easy right? Actually, it was a pretty easy and it didn't take much effort to get all the user accounts including the host directory over to the new server.

{% gist 9b7181b218ab02b4314e7ccd0194bbe2 %}


