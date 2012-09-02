---
comments: true
date: 2011-03-26 14:13:07
layout: post
slug: groovesharks-global-keyboard-shortcuts-in-windows
title: Groovesharks global keyboard shortcuts in Windows
wordpress_id: 248
categories:
- Default
tags:
- Firefox
- gsAPI
- HotAutokey
- keyboard shortcuts
- keySharky
- Prism
- wget
- win7
- windows
---

While playing with [Windows 7](http://www.microsoft.com/windows/windows-7/default.aspx), I had no other choose as to put up solution for missing global keyboard shortcuts in [Grooveshark player](http://listen.grooveshark.com/) (who sits inside [Firefox](http://www.mozilla.com/en-US/firefox/) or [Prism](http://prism.mozillalabs.com/), because that's a way I roll), similar to solution in [Ubuntu](http://www.ubuntu.com/). Luckily it's (kinda) easy to achieve, so here we **gooo**!

First of all, we will need some software to begin with: [Wget for Windows](http://gnuwin32.sourceforge.net/packages/wget.htm) (grab "Complete package, except sources" download or if you are lost, here is [direct link to 1.11.4](http://downloads.sourceforge.net/gnuwin32/wget-1.11.4-1-setup.exe) version) and [AutoHotkey](http://www.autohotkey.com/download/). Install both of them.

{% img center /static/2011/2011-03-26_1035.png %}

Now open _AutoHotkey_ (located in your _Program Files_ or _where ever did you install it_). It should ask if you would like to create a sample script in _My Documents_ folder (if that file doesn't exist yet). What are you waiting for? Yes, of course! Great now when _AutoHotkey_ sample script pop-up on screen wipe it clean.

{% img center /static/2011/2011-03-26_1039.png %}

Now some magic. To create new keyboard shortcut for _Grooveshark_ player using [keySharky API](https://github.com/intarstudents/keySharky/wiki/api-server), just add a line that goes something like this:

```
HOTKEY::Run, WGET_EXE --spider --no-cache KEYSHARKY_API, , Hide
```

In place of **HOTKEY** you could write `^H` which when translated into keyboard shortcut would assign `CTRL + H` combo. Other basic modifier keys are `#` _Windows key_, `!` _Alt_ and `+` _Shift_. For more, check out _AutoHotkey _[documentation on that subject](http://www.autohotkey.com/docs/Hotkeys.htm).

For this example, I will use `^!+Z` as `CTRL + ALT + SHIFT + Z`.

{% img center /static/2011/2011-03-26_1147.png %}

Next in line: **WGET_EXE** you must replace with _wget.exe_ binary location path. By default in Windows 7 (64-bit), _Wget _installs in "C:\Program Files (x86)\GnuWin32\bin\wget.exe". But if you aren't sure where did you install it in your machine, you can search for it by doing _Start (Orb) > Run > cmd_ (or just search for _cmd_). When in command line execute this command. What it does is, tries to find _wget.exe_ in your `C:\` drive and return its full path.

```
dir c:\ /s /b | find "wget.exe"
```

Last on list is **KEYSHARKY_API**, but how to setup/use it you can (and should) read [here](https://github.com/intarstudents/keySharky/wiki/api-server). When done, it should look something like this:

```
^!+Z::Run, "C:\Program Files (x86)\GnuWin32\bin\wget.exe" --spider --no-cache "http://localhost:8800/play", , Hide
```

This example will toggle play/pause in _Grooveshark_ player when `CTRL + ALT + SHIFT + Z` combo is pressed.

{% img center /static/2011/2011-03-26_1139.png %}
