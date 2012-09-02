---
comments: true
date: 2010-05-27 16:36:00
layout: post
slug: reaction-test-with-html5-audio
title: Reaction test with HTML5 audio
wordpress_id: 13
categories:
- Default
tags:
- audio
- false start
- html5
- reaction test
---

Yesterday friend asked if I could build reaction test with sound (he till now was using graphical) and I of course couldn't crush his dreams (and because I really haven't build anything interesting [using audio tag](http://html5doctor.com/native-audio-in-the-browser/)).

So after while, [falstart](http://github.com/intarstudents/falstart) was made ([online demo](http://i.tldr.lv/falstart/) for those who aren't interested in source code). It of course isn't perfect (no _fallback_ for unsupported browsers), but with _Firefox 3.6.3_ and _Google Chrome 6.0.408.1 dev_ works good (Google Chrome better then Firefox, because of faster JavaScript engine).

And there was one interesting bug that I encountered during writing it, that Google Chrome was very slow with seeking audio file to beginning and made big gasp (well ~900 ms) before started playing it again (and those added it to user reaction time). Fast fix for it, was setting it by myself.

```javascript
audioObject.pause();
audioObject.currentTime = 0;
```

That's all, what was on my mind. Happy, your reaction testing!
