---
tags: []
title: 'Short Notice: Protocol Break'
---
As we have tagged a 0.5 release candidate now, which has made its way in Kubuntu Karmic and Jaunty backports, among others, we should point out that the client/core protocol used in 0.5 is <b>not</b> compatible to the 0.4.x releases anymore. This means you'll need to use a 0.5-rc1 client with a 0.5-rc1 core. Same for current git master, of course. The protocol change gives you a great performance boost in the core, in particular for startup, shutdown, and joining/quitting large channels. So it's definitely worth it :)

As this is isn't an official release yet, it's not linked from the download page. However, you can find binary builds for Windows and MacOSX <a href="/pub">here</a>.
<!--break-->
