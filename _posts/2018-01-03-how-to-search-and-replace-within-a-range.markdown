---
layout: post
title: "How to search and replace within a range in vim"
date: "2018-01-03 15:29:16 -0500"
categories: vim
---

A quick "search and replace in vim" google search will likely result in vim command looking something like this:

{% highlight vim %}
%s/foo/bar/g
{% endhighlight %}

While useful, you may have a big file and want to restrict where you find and replace. The `%` operator can be omitted to search a single line, or be replaced with a range of lines, like so:

{% highlight vim %}
" Singe line
s/foo/bar/g 

" Range
1,5s/foo/bar/g
{% endhighlight %}
