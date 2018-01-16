---
layout: post
title: "Running rails dev server in the background"
date: "2018-01-16 15:08:48 -0500"
categories: rails
---

When I am working on UI in a rails app, I typically don't care to read the information in a rails debugger.

Running rails in the background is as easy as:

{% highlight shell %}
rails s -d
{% endhighlight %}

Quitting the process is slightly tricker than the good ol fashion cmd-c

{% highlight shell %}
kill -9 $(cat tmp/pids/server.pid)
{% endhighlight %}
