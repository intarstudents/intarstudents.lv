---
comments: true
date: 2011-12-18 22:48:36
layout: post
slug: bytingshark-cross-browser-support
title: Bytingshark cross-browser support
wordpress_id: 318
categories:
- Default
tags:
- bytingshark
- cross-bro
- Firefox
- google chrome
- Grooveshark
- Opera
- Safari
- userscript
---

If someone [asks for it](http://intarstudents.lv/bytingshark/#comment-514), I might as well fix it. Updated [bytingshark.user.js](http://userscripts.org/scripts/show/119253) works (and is tested) with [Firefox](http://www.mozilla.org/en-US/firefox/), [Google Chrome](https://www.google.com/chrome?hl=en) and [Opera](http://www.opera.com/). [Safari](http://www.apple.com/safari/) is somehow experimental and I was lazy [to do this](http://www.simplehelp.net/2007/11/14/how-to-run-greasemonkey-scripts-in-safari/), but hopefully it works :)

## Installation

### Firefox

You will need to install [Greasemonkey](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/) add-on. After that just open _bytingshark.user.js_ and install it.

### Google Chrome

Just open _bytingshark.user.js_ and it should prompt install wizard.

### Opera

Copy _bytingshark.user.js_ script into User JavaScript folder. If you don't know where yours located at (or haven't added it yet):

1. Goto Preferences > Advanced > Content > JavaScript Options ...
2. There will be field named "User JavaScript folder", set it where you putted _bytingshark.user.js_ script.
