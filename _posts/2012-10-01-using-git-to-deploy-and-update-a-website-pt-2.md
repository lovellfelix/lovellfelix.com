---
layout: post
title: Using Git to deploy and update a website Pt. 2
date: '2012-10-01T17:00:12-07:00'
tags:

author:
  name: Lovell Felix
  twitter: lovellfelix
  gplus: 102676824509364241023
  bio: Geek, Google Fanboy, Tech News Junkie, Entrepreneur - Drinker of tea :)
  image: https://lh3.googleusercontent.com/-Ubq3pEfgeLk/AAAAAAAAAAI/AAAAAAAAOvs/nGutWDQ5OGc/s120-c/photo.jpg.png

tumblr_url: http://blog.lovellfelix.com/post/32691308177/using-git-to-deploy-and-update-a-website-pt-2
---

Previously I wrote <a href="/blog/tutorial-how-to-use-git-to-deploy-and-update-a-website/">Tutorial: How to use Git to deploy and update a website Pt. 1</a>, I was able to simultaneous push my changes seamlessly from my local machine to my git server, and web server.

It worked great, and reduced my deployment time significantly. Now I am taking it a step further. I want to push two different branches to different locations on my remote server.
There are two branches on my local machine <b>Master</b>, and <b>Beta</b>.<!-- more -->

With this twist, I will be able to push the <b>Master branch</b> to <u>http://example.com</u>, and the <b>Beta branch</b> to <u>http://beta.example.com</u>. Let’s start by creating the <b>Beta Branch</b> from your existing directory on the local machine.

<b>git branch checkout -b beta</b>

After that, SSH to the GIT Server, and navigate to the Git repository folder, example: <b>/home/project/website.git/</b>. 

Then create a post-receive hook that checks out the <b>Master</b> and <b> Beta branch</b> into the respectable web server’s <b>DocumentRoot</b>.

{% highlight bash %}
vi hooks/post-receivecat >
#!/bin/bashwhile read oldrev newrev refdo  branch=`echo $ref | cut -d/ -f3`
if [ "master" == "$branch" ];
then    git --work-tree=/path/under/root/dir/live-site/ checkout -f $branch    
echo ''Changes pushed live.''  
fi  
if [ "dev" == "$branch" ];
then    
git --work-tree=/path/under/root/dir/dev-site/ checkout -f $branch    
echo ''Changes pushed to dev.''  
fi done
{% endhighlight %}

And that’s it! Easy as pie. 0.o  
