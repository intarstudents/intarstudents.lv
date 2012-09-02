---
comments: true
date: 2010-08-06 12:07:24
layout: post
slug: checkboxes-all-the-way
title: Checkboxes all the way
wordpress_id: 149
categories:
- Default
tags:
- Grooveshark
- GSDesktop
- keyboard shortcuts
- shark week
---

Thanks to [ppannuto](http://www-personal.umich.edu/~ppannuto/), new version of [GSDesktop Helper for linux](http://github.com/intarstudents/GSDesktop-Helper) comes with feature that allows you to disable unwanted keyboard shortcuts. Its great for those you doesn't like to clutter their keyboard shortcuts with unwanted stuff.

{% img center /static/2010/syhee1u.png %}

If you want to install _GSDesktop Helper_ in [Ubuntu](http://www.ubuntu.com/)/[Debian](http://www.debian.org/), you can use already packed package:

```bash
cd ~
wget http://github.com/downloads/intarstudents/GSDesktop-Helper/gsd-helper-0.4.2_all.deb
sudo dpkg -i gsd-helper-0.4.2_all.deb
```

Or if your distributive doesn't support [Debian packages](http://en.wikipedia.org/wiki/Deb_%28file_format%29), you can always run it directly from command line (but before this you may be needed mess with [dependencies](http://github.com/intarstudents/GSDesktop-Helper/blob/master/README)):

```
cd ~
git clone http://github.com/intarstudents/GSDesktop-Helper.git
cd GSDesktop-Helper/
./helper.py
```

That's it for this [shark week](http://en.wikipedia.org/wiki/Shark_Week), keep swimming with [Grooveshark](http://listen.grooveshark.com/) and everything will be alright :)
