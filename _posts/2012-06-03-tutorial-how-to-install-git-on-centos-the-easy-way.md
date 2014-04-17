---
layout: post
title: 'Tutorial: How to install Git on CentOS the easy way.'
date: '2012-06-03T23:31:00-07:00'
tags: 
tumblr_url: http://blog.lovellfelix.com/post/24385308070/tutorial-how-to-install-git-on-centos-the-easy-way

author:
  name: Lovell Felix
  twitter: lovellfelix
  gplus: 102676824509364241023
  bio: Geek, Google Fanboy, Tech News Junkie, Entrepreneur - Drinker of tea :)
  image: https://lh3.googleusercontent.com/-Ubq3pEfgeLk/AAAAAAAAAAI/AAAAAAAAOvs/nGutWDQ5OGc/s120-c/photo.jpg.png
---

What is git? 

git -  is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. 


Git is easy to learn and has a tiny footprint with lightning fast performance.
It outclasses SCM tools like Subversion, CVS, Perforce, and ClearCase with features like cheap local branching, convenientstaging areas, and multiple workflows.  
Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency. 


Git is easy to learn and has a tiny footprint with lightning fast performance. It outclasses SCM tools like Subversion, CVS, Perforce, and ClearCase with features like cheap local branching, convenientstaging areas, and multiple workflows.


Installing git -

{% highlight scss %}
//First we need to add the EPEL Repository to CentOS.

//Install EPEL Repository On 32-bit CentOS Linux 5.5:

rpm -Uvh http://dl.fedoraproject.org/pub/epel/5/i386/epel-release-5-4.noarch.rpm

//Install EPEL Repository On 64-bit CentOS Linux 5.5:

rpm -Uvh http://dl.fedoraproject.org/pub/epel/5/x86_64/epel-release-5-4.noarch.rpm

//Once everything goes right run -

yum update

yum install git git-daemon

{% endhighlight %}

And that’s it! 
