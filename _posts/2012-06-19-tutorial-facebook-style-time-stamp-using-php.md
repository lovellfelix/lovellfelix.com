---
layout: post
title: 'Tutorial: Facebook Style time stamp using PHP'
date: '2012-06-19T17:52:00-07:00'
tags:

author:
  name: Lovell Felix
  twitter: lovellfelix
  gplus: 102676824509364241023
  bio: Geek, Google Fanboy, Tech News Junkie, Entrepreneur - Drinker of tea :)
  image: https://lh3.googleusercontent.com/-Ubq3pEfgeLk/AAAAAAAAAAI/AAAAAAAAOvs/nGutWDQ5OGc/s120-c/photo.jpg.png

tumblr_url: http://blog.lovellfelix.com/post/25463607324/tutorial-facebook-style-time-stamp-using-php
---
The function returns the difference between two Dates as a human string for use in the browser. For instance, the values returned are seconds ago, 50 minutes ago, 7 hours ago, a day ago, weeks ago, years ago, and so on.

Syntax
$time = strtotime(YYYY-MM-DD HH:MM:SS)

Example

{% highlight scss %}

$time = strtotime(''2010/09/10 10:00:00'') => "- 3 days ago"

//The default time units are:

$tokens = array ( 31536000 => ''year'', 2592000 => ''month'', 604800 => ''week'', 86400 => ''day'', 3600 => ''hour'', 60 => ''minute'', 1 => ''second'' ); 

//The text will be automatically de-pluralized if, say there is only 1 year.

foreach ($tokens as $unit => $text) {
if ($time < $unit) continue; $numberOfUnits = floor($time / $unit);
return $numberOfUnits.'' ''.$text.(($numberOfUnits>1)?''s'':'''');
}

{% endhighlight %}

The complete project can be download from my Github Repository
