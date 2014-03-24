---
layout: post
title: Using Git to deploy and update a website Pt. 2
date: '2012-10-01T17:00:12-07:00'
tags: 
tumblr_url: http://blog.lovellfelix.com/post/32691308177/using-git-to-deploy-and-update-a-website-pt-2
---
Previously I wrote Tutorial: How to use Git to deploy and update a website Pt. 1 I was able to automatically
push my updates seamlessly from my local machine to my git server, and web server.

It worked great, and reduced my deployment time significantly. Now I want to take it a step further. I want to push two
different branches to different locations on my remote server.
There are two branches on my local machine Master, and Beta.

With this twist I should be able to push the Master branch to http://example.com, and the Beta branch to
http://beta.example.com.Let’s start by creating the Beta Branch from your existing directory on the local machine.git branch
checkout -b betaAfter that, SSH to the GIT Server, and navigate to the Git repository folder,
example: /home/project/website.git/Then we define (and enable) a post-receive hook that checks out the Master and Beta branch
into the respectable web server’s DocumentRoot.

{% highlight scss %}
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
