---
comments: true
date: 2010-07-05 15:56:28
layout: post
slug: groovesharks-remote-with-arduino
title: Groovesharks remote with Arduino
wordpress_id: 135
categories:
- Default
tags:
- Arduino
- Ethernet shield
- Grooveshark
- IR receiver
- keySharky
---

Last day or so, I have been playing with [Ethernet shield](http://arduino.cc/en/Guide/ArduinoEthernetShield) and [IR receiver](http://www.adafruit.com/index.php?main_page=product_info&cPath=35&products_id=157&zenid=d87b8aa6a565161807099aed97b69fbf) for my [Arduino](http://arduino.cc/en/Main/ArduinoBoardDuemilanove). And what else could come to mind when I hear theses two together? Of course - controlling [Grooveshark](http://listen.grooveshark.com/) with old _TV'ish_ remote.

So, how its working, you might ask? Well, will try to answer that briefly. TV remote sends signal to _IR receiver_, who then passes it to _Arduino_ for decoding. _Arduino_ builds up [binary code](http://en.wikipedia.org/wiki/Binary_numeral_system) from [signal](http://zovirl.com/2008/11/12/building-a-universal-remote-with-an-arduino/) and then converts it to integer (key code). Knowing what button was pressed, it then opens socket to [keySharky](https://addons.mozilla.org/en-US/firefox/addon/54954/) [API server](http://wiki.github.com/intarstudents/keySharky/api-server) and sends method who needs execution.

It might not be perfect, but that's how it rolls :)
