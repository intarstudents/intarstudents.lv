---
comments: true
date: 2010-11-14 11:08:15
layout: post
slug: linux-mint-10-with-shiki-wise-theme
title: Linux Mint 10 with Shiki-Wise theme
wordpress_id: 202
categories:
- Default
tags:
- Linux Mint
- Mint
- Shiki-Mint
- Shiki-Wise
- Theme
---

Some days ago [Linux Mint 10 was released](http://blog.linuxmint.com/?p=1581). I upgraded as soon as could, but didn't like [new theme](http://www.linuxmint.com/pictures/screenshots/julia/julia.png). So after _Google'ing_ around and wasn't able to found solution, I was forced to write my own. And here it is.

**Update**: as of now there is easier way to install Shiki-Wise theme, but I will leave second option anyway :) (thanks to [Mantas](http://mantas.malcius.lt/) for pointing out it).

```bash
sudo aptitude install shiki-wise-theme
```

First, download [Shiki-Wise theme](https://github.com/downloads/intarstudents/Shiki-Wise-Minty/Shiki-Wise-Minty.tar.gz) (not the one from [Shiki-Colors](http://gnome-look.org/content/show.php/Shiki-Colors?content=86717), but extracted from previous Mint version, because they are bit different) and extract it.

```bash
cd ~
wget https://github.com/downloads/intarstudents/Shiki-Wise-Minty/Shiki-Wise-Minty.tar.gz --no-check-certificate
tar zxvf Shiki-Wise-Minty.tar.gz
```

Now copy theme folder over to `/usr/share/themes/` and install dependencies.

```bash
sudo mv Shiki-Wise /usr/share/themes/
sudo aptitude install shiki-colors-metacity-theme gnome-wise-icon-theme
```

You are done. Navigate to Preferences > Appearance and select _Shiki-Wise_ as your theme :)
