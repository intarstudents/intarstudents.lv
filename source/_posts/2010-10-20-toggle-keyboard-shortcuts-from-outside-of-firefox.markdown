---
comments: true
date: 2010-10-20 16:10:08
layout: post
slug: toggle-keyboard-shortcuts-from-outside-of-firefox
title: Toggle keyboard shortcuts from outside of Firefox!
wordpress_id: 189
categories:
- Default
tags:
- Firefox
- httpd.js
- httpk3y
- keyboard shortcuts
- Prism
- server
---

First of all little background why I thought this was a good idea. For most of my time I'm working as web developer and have two monitor workstation. So easiest way is to write code in one monitor and "review" it as web page on other one (inside web browser). But that makes a lot of work to navigate between them. _Click there, click here_. And even if you use `Ctrl + Tab` it's more than two keyboard shortcut away from reloading that page.

And I know that out there is [XRefresh](http://xrefresh.binaryage.com/), but not every time when code has been edited there is need for refresh, because it might just be a little change (like added comment, that will not appear in page anyways) or I just don't feel like reloading.

So in scene comes [httpK3y](http://github.com/intarstudents/httpK3y) - small server inside Firefox/Prism add-on, that you can control via [HTTP](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol). It has simple [API](http://github.com/intarstudents/httpK3y/blob/master/README.md) and is easy to configure. Works cross platform (Windows, Linux, Mac OS X) and only dependencies are [Firefox](http://www.mozilla.com/en-US/) (3.6 and up) or [Prism](http://prism.mozillalabs.com/) (1.0 and up).

You can read on about how to use _httpk3y_ in [README](http://github.com/intarstudents/httpK3y/blob/master/README.md), but I will give you simple example how I use it in [Mint](http://www.linuxmint.com/) ([Ubuntu](http://www.ubuntu.com/)).

```bash
$ wget http://localhost:7700/key_reload --spider --no-cache
```

Simple as that! And here you can grab package for [Firefox](https://addons.mozilla.org/en-US/firefox/addon/242725/) or/and [Prism](http://github.com/downloads/intarstudents/httpK3y/httpK3y-prism.xpi). Have fun!

_P.S. Questions?_
