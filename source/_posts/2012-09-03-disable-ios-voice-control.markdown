---
layout: post
title: "Disable iOS Voice Control"
date: 2012-09-03 22:40
comments: true
categories: 
---

Some days ago, I got annoyed with that, everyone couldn't pick up my iPhone and start messing with [Voice Control](http://support.apple.com/kb/HT3597). And because I never use (or will use) this feature, I took journey to turn it off, ones and for all.

Google [gave me some hints](http://www.ifans.com/forums/threads/speed-up-your-iphone-ipod-by-removing-launch-daemons.224341/) about [daemons](http://en.wikipedia.org/wiki/Daemon_\(computing\)) running in background, responsible for Voice Control interactions. With that knowledge in my head, I started moving them into backup folder:

```bash Disable iOS Voice Control
oolongtea:~ root# mkdir ~/backup/
oolongtea:~ root# cd /System/Library/LaunchDaemons/
oolongtea:/System/Library/LaunchDaemons root# mv com.apple.scrod.plist ~/backup/
oolongtea:/System/Library/LaunchDaemons root# mv com.apple.VoiceOverTouch.plist ~/backup/
oolongtea:/System/Library/LaunchDaemons root# mv com.apple.voiced.plist ~/backup/
```

And after quick restart, no one could open Voice Control, because it crashed before any harm could be done. *Excellent!*