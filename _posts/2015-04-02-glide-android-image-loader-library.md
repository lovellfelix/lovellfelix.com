---
layout: post
title: 'Glide: Android Image loader library'
date: '2015-04-01T23:31:00-07:00'
tags:

author:
  name: Lovell Felix
  twitter: lovellfelix
  gplus: 102676824509364241023
  bio: Geek, Google Fanboy, Tech News Junkie, Entrepreneur - Drinker of tea :)
  image: https://lh3.googleusercontent.com/-Ubq3pEfgeLk/AAAAAAAAAAI/AAAAAAAAOvs/nGutWDQ5OGc/s120-c/photo.jpg.png
---

The past few weeks the [Android community](https://plus.google.com/communities/105153134372062985968) been ranting and raving over [Glide](https://github.com/bumptech/glide), the new image loader kid on the block (well newish). It actually been around for almost a year. It was introduced in Google I/O 2014. I tried it last July, but the performance wasn’t significantly different to [Picasso](http://square.github.io/picasso/) and the community was small, so I decided to continue using [Picasso](http://square.github.io/picasso/) in all my projects. Yeah I know, I chose a product based on popularity :P Is that a bad thing? 

So why did I decide to do the old switcheroo? I came across a blog post on [The Cheese Factory](http://inthecheesefactory.com/blog/get-to-know-glide-recommended-by-google/en) with some performance benchmark, and it clearly illustrated how ridiculously fastER and bettER at memory usage [Glide](https://github.com/bumptech/glide) was to [Picasso](http://square.github.io/picasso/). <!-- more -->


![credit - The Cheese Factory](/images/posts/glide_usage.png)

Ok great! Statistics looks awesome, now the lets look into the key factor. USABILITY!!! How easy is it to use? I’m the type that don’t really like putting in too much extra effort trying to figure out how to use a library. In my opinion, if it’s hard to implement it’s not a library.  Ooops maybe I should that that back... Volley you’re awesome! 

The good news if you’re familiar with [Picasso](http://square.github.io/picasso/) you’re in Good hands. They’re very similar, and easy to implement with one liners.
{% highlight Java %}

//Picasso 

dependencies {
    compile 'com.squareup.picasso:picasso:2.5.1'
}

Picasso.with(context)
    .load("https://lovellfelix.com/images/logo.png")
    .into(imgView);
{% endhighlight %}

{% highlight Java %}

//Glide

dependencies {
    compile 'com.github.bumptech.glide:glide:3.5.2'
    compile 'com.android.support:support-v4:22.0.0
} 

Glide.with(context)
    .load("https://lovellfelix.com/images/logo.png")
    .into(imgView);
{% endhighlight %}

See they’re are very similar, but [Glide](https://github.com/bumptech/glide) is a little bit more flexible, but that’s another blog post. 

Based on the performance improvement I’ve seen after switching over to [Glide](https://github.com/bumptech/glide) it definitely was worth it, and No it’s not like switching mobile network providers.

> No Tricks all Treats! I promise ;)

Until next time, Happy Gliding. 

