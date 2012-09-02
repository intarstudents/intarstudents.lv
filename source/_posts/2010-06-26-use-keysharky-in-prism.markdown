---
comments: true
date: 2010-06-26 19:43:39
layout: post
slug: use-keysharky-in-prism
title: Use keySharky in Prism
wordpress_id: 87
categories:
- Default
tags:
- Add-ons
- API
- Grooveshark
- Prism
---

2011.03.26. **[Groovesharks global keyboard shortcuts in Windows](http://intarstudents.lv/groovesharks-global-keyboard-shortcuts-in-windows/)**

**Updated: to new version of keySharky for Prism (1.5)**

It's really nice to receive ideas from users of add-on and make them into reality. One month ago [vsilvar](http://github.com/vsilvar) requested port to [Prism](http://prism.mozillalabs.com/). Sadly, at the time [keySharky](https://addons.mozilla.org/en-US/firefox/addon/54954) didn't have that great [API server](http://wiki.github.com/intarstudents/keySharky/api-server) feature, so I didn't see any reason for porting. But now, things are bit different and thanks to [pandronic](http://github.com/pandronic) of reminding me that.

Funny or not, but port is already [online](http://wiki.github.com/intarstudents/keySharky/build-package-for-prism)! So, you might ask, how to install and use all of that goodness? For that was wrote this tutorial ;)

## Setup Prism

_Prism_ lives in [Mozilla Labs page](http://prism.mozillalabs.com/) and you can [download](http://prism.mozillalabs.com/started/) it for your [OS](http://en.wikipedia.org/wiki/Operating_system). Then extract, install or [do whatever you need](http://www.google.com/search?hl=en&q=install+prism&aq=f&aqi=g-p1g1g-m2&aql=&oq=&gs_rfai=) to get _Prism_ running.

## Create Grooveshark WebApp

Open _Prism_ "application creator" and fill forms like so (of course you could go more fancy, about configuring it, but be sure to have checked "_Show status messages and progress_" because we will need it to configure _keySharky_):

{% img center /static/2010/12tzsr2.png %}

Now you are allowed to press _Ok_.

## Installing keySharky

Grab package of [keySharky for Prism](http://github.com/downloads/intarstudents/keySharky/keySharky-prism-latest.xpi). In newly created _WebApp_ at bottom right corner find gear icon and click on it. Navigate to _Tools > Add-ons_.

{% img center /static/2010/14tzsr2.png %}

_Add-ons_ window should appear. To add _keySharky_ click on _Install_ button, then find where you downloaded _keySharky_ package and select it. If all is good, you should by now have installed _keySharky_ waiting for restart of _Prism_.


{% img center /static/2010/15tzsr2.png %}

Now restart _Prism_ (for me _Restart Prism_ button wasn't working (like I was hopping), so I just closed every window associated with _Prism_ and then relaunched _Grooveshark WebApp_ from _Desktop_).

## Configuring keySharky API server

Again open _Add-ons_ window and then:

  * In _Port_ input box, select your desired port number;
  * Choose if you want to start _API server_, when you open _Prism_, in _Start with Firefox_ checkbox;
  * Press _Start_ to run server;

## Fullscreen goodness

If you don't like status bar, after you configured _keySharky_, you can remove it! You will need find _Web Apps Bundles_ folder:

{% blockquote WebApp bundle https://developer.mozilla.org/en/Prism/Bundles %}
This folder is located in the Application Data folder of the user's home directory on Windows, in the ~/.webapps directory on Linux and under ~/Library on OS X
{% endblockquote %}

Inside _Web Apps_ folder find similar folder to "grooveshark@prism.app" (or whatever you named your _Web App_) and open it. With your favorite text editor open _webapp.ini_. You will see that `status=true`, but you don't want that, so change it to `status=false` and hit save. Lastly restart _Prism_ and _Volla_, status bar is hidden away.

Well, and thats all folks! Now you can use _API server_ to control [Grooveshark](http://listen.grooveshark.com/) player inside _Prism_ (add global keyboard shortcuts, create notifiers - its up to you!).

**P.S.** If you have any questions feel free to ask me
