---
layout: post
title: "How to minify a css or js file in vim"
date: "2018-01-26 18:32:03 -0500"
categories: vim
---

I wanted a quick and easy way to minify a CSS file for this site, without adding any fancy build tools like webpack, using a quick command.

The ideal workflow was:

- Open a regular CSS file.
- Minify the current file.
- Save over the file.

After some digging and a node library, I came up with this.

1. Install Minify via NPM
``` shell
npm install -g minify
```
2. Open css file in vim
``` shell
vim style.css
```
3. Now that you are in vim, create a new line at the top of the file using <kbd>Shift</kbd> + <kbd>O</kbd>
4. Read in the existing file, parse it through minify and paste it in place.
``` vim
:r !minify %
```
5. Move down a line to the uncompressed css and delete the rest of the file using <kbd>d</kbd> + <kbd>G</kbd>

If you are looking to minify lots of files for an app there are clearly better options, but if you just want to shrink the size of a single file on a static site this is my new favorite.
