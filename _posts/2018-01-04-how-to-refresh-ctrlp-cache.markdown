---
layout: post
title: "How to Refresh CtrlP Cache"
date: "2018-01-04 10:45:19 -0500"
categories: vim 
---

I really enjoy using [`ctrlp.vim`](https://github.com/ctrlpvim/ctrlp.vim) for fuzzy finding files in vim. Makes navigation really easy.

By default, `ctrlp` caches your directories upon first use for faster finding later on. That typically works great until you add or delete files, and your cache is no longer valid.

Fortunately, you can quickly purge your cache in ctrlp by clicking <kbd>F5</kbd> once ctrlp is open.

I must have missed this line in the documentation. 
