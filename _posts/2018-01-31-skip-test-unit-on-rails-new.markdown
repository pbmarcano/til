---
layout: post
title: "Skip test_unit on `rails new`"
date: "2018-01-31 23:34:59 -0500"
categories: rails
---

While starting a new rails app, I noticed that I could simply skip installing Test::Unit from the start. This left the initial application ready for Rspec to be installed and configured.

```shell
rails new my_app --skip-test
```

Pretty simple. Kicking myself for removing it manually each time I decided to use Rspec.
