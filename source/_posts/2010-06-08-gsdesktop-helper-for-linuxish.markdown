---
comments: true
date: 2010-06-08 17:18:00
layout: post
slug: gsdesktop-helper-for-linuxish
title: GSDesktop Helper for Linux'ish
wordpress_id: 9
categories:
- Default
tags:
- API
- Grooveshark
- GSDesktop
- keyboard shortcuts
- Linux
- PyGTK
- python-keybinder
- Ubuntu
---

We all know, that Windows and Mac users are able [to use new "API"](http://grooveshark.wikia.com/wiki/GSDesktop_Global_Keyboard_Shortcuts) for [Grooveshark Desktop](https://vip.grooveshark.com/), but why should Linux users be different? So without long introduction - [GSDesktop Helper for Linux](http://github.com/intarstudents/GSDesktop-Helper). It's written in pure [PyGTK](http://www.pygtk.org/) and needs [python keybinder](http://kaizer.se/wiki/keybinder/) to work, so have everything installed, ok?

```bash
sudo aptitude install python-keybinder python-gtk2 python
```

After that, just grab script from git in your favorite fashion:

```bash
cd ~
git clone http://github.com/intarstudents/GSDesktop-Helper.git
```

Now, for example, you could press `ALT + F2` and in "Run Application" dialog enter `GSDesktop-Helper/helper.py` and press "Run".

That's all! Now you can control your Grooveshark Desktop with global keyboard shortcuts defined in [wiki](http://grooveshark.wikia.com/wiki/GSDesktop_Global_Keyboard_Shortcuts).
