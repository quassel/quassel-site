---
tags: []
title: 'Bug Wars: The Phantom Release'
---
People closely following our development in git will have noticed that we have tagged a 0.4.2 release back in May. Some distros also have been shipping 0.4.2 for quite a while now. However, there never was an official release announcement. Why?

Well, shortly after tagging this release, we got feedback from several users that Quassel would crash on startup, in particular (but not only) if it was started hidden to tray and one clicked the tray icon to bring it to front. With Quassel crashing consistently for some people, we decided to not announce the release until a solution has been found.

This crash bug is documented in http://bugs.quassel-irc.org/issues/663 and we have been frantically trying to hunt it down and fix it. However, so far we haven't been successful. For once, I can't reproduce this, which makes debugging hard; also, it seems to be a Heisenbug which goes away as soon as you attach a debugger to look into it.
In our desperation, kaffeedoktor is now trying debugging this issue on Windows using MSVC, hoping that its debugger can shine some light to the reason. At the moment, it appears to be hidden deeply in Qt's MVC framework. Investigation is still ongoing.

We have, however, figured out a way to workaround this crash-on-startup, and this workaround is currently being evaluated. If it works well, we'll be releasing a 0.4.3 together with 0.5.0 in roughly a week from now. So stay tuned!
