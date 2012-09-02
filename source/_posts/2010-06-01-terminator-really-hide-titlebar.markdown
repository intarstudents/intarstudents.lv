---
comments: true
date: 2010-06-01 16:42:00
layout: post
slug: terminator-really-hide-titlebar
title: Terminator - really hide titlebar
wordpress_id: 12
categories:
- Default
tags:
- GitHub
- patch
- terminal
- Terminator
---

You all know [Terminator](https://launchpad.net/terminator), that who brings multiple terminals in one window. But I found one annoying feature. To be processes - titlebar hide feature. What's wrong with it? Well, it doesn't hide that damn thing!

{% img center /static/2010/terminator-before.png %}

See? Yeah right, it sucks and looks ugly (if you don't use titlebar at all). To solve that, you will have to get dirty with patch I wrote, but promise, nothing hard at all. Just follow these steps.

First you need Terminator source and cooked patch.

```bash
cd ~
wget http://launchpad.net/terminator/trunk/0.93/+download/terminator-0.93.tar.gz
git clone git://gist.github.com/421135.git
```

Great, now some hardcore extracting part.

```bash
tar zxvf terminator-0.93.tar.gz
```

Now everything in place. We finaly can apply patch and install patched version of Terminator.

```bash
cd terminator-0.93
patch terminatorlib/titlebar.py < ../421135/terminator-really-hide-titlebar.patch
sudo ./setup.py install
```

If no errors accrue, then you should have patched version installed. Success! :)

{% img center /static/2010/terminator-after.png %}

**_Note before install:_** be sure you have all dependencies to install Terminator: _cdbs (>= 0.4.49), debhelper (>= 5.0.62), intltool, python_.

**P.S.** Almost forgot, you can toggle hide option in _Right Click (anywhere in terminal) > Preferences > Profiles > Show titlebar_.

**P.S.S.** Yeah, lazy me, didn't do search in launchpad and those [missed this](https://bugs.launchpad.net/terminator/+bug/552539), but I had fun building patch so, no hard feelings.
