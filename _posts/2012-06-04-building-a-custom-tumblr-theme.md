---
layout: post
title: Building a custom tumblr. theme
date: '2012-06-04T21:42:00-07:00'
tags: 
tumblr_url: http://blog.lovellfelix.com/post/24447493615/building-a-custom-tumblr-theme

author:
  name: Lovell Felix
  twitter: lovellfelix
  gplus: 102676824509364241023
  bio: Geek, Google Fanboy, Tech News Junkie, Entrepreneur - Drinker of tea :)
  image: https://lh3.googleusercontent.com/-Ubq3pEfgeLk/AAAAAAAAAAI/AAAAAAAAOvs/nGutWDQ5OGc/s120-c/photo.jpg.png

---

To start, click the name of your blog at the top of the Dashboard, click the ”Customize appearance” button on the right side of the page. Click the ”Edit HTML” button under the theme thumbnail to access your current theme’s HTML code.
Tumblr has two types of special operators used to render content in your HTML.
Variables are used to insert dynamic data like your blog’s title or description:
<!-- more -->
Html Head
As always in Html, there are several pieces of information you are going to want to include within the head of your html document, and Tumblr does not let us down. It provides us with several variables that can be deployed with great ease.

{% highlight bash %}
{Title} – The html safe title of your blog
{Meta Description} – An html safe description of your blog for use within the meta tag
{Favicon} – A dynamically generated favicon url from your portrait photo
{RSS} – The url to the RSS feed of your tumbleblog

===========

<html>
    <head>
<title>{Title}</title>
	<link rel="shortcut icon" href="{Favicon}">
	rss+xml" href="{RSS}">
	<meta name="description" content="{MetaDescription}" />
    </head>
    <body>
        ...
    </body>
</html>
{% endhighlight %}

Blocks are either used to render a block of HTML for a set of data (like your posts), or to conditionally render a block of HTML like a “Previous Page” link):

{% highlight bash %}
<html>
    <body>
        <ol id="posts">
            {block:Posts}
                <li> ... </li>
            {/block:Posts}
        </ol>
    </body>
</html>
{% endhighlight %}

Display Posts:

Now that we have set up the easy stuff with some basic variables, it’s time to get stuck into the more dynamic posts which are rendered with the help of both blocks and variables. The posts block is placed in the area that all our different types of posts will be displayed.

Within our posts block, we can start to branch out into our many different kinds of posts. Each of these are shown below.

{% highlight bash %}
{block:Text}{/block:Text} – Displays Text posts
{block:Photo}{/block:Photo} – Displays Photo posts
{block:Photoset}{/block:Photoset} – Displays Photoset posts
{block:Quote}{/block:Quote} – Displays Quote posts
{block:Link}{/block:Link} - Displays Link posts
{block:Chat}{/block:Chat} – Displays Chat posts
{block:Audio}{/block:Audio} – Displays Audio posts
{block:Video}{/block:Video} – Displays Video posts
{block:Answer}{/block:Answer} – Displays answer posts
{% endhighlight %}


Each different type of post has several different types of variables and further blocks that are relevant only to that type of post, but there are several variables that are likely to be used in ever post such as the link, and tags.

{% highlight bash %}
{Permalink} – The exact url for a single post
{ShortURL} – The sharing friendly short url for a single post
{PostID} – The unique numeric post ID for a single post

{block:Posts}
...
	{block:Text}
	<div>
		{block:Title}
		<h2><a href="{Permalink}">{Title}</a></h2>
		{/block:Title}
		<div>
		{Body}
		</div>
	</div>
	{/block:Text}
...
{/block:Posts}

{% endhighlight %}

The different type of variables can be found on tumblr. documents page here, and you can fork or download theme to this blog on github
