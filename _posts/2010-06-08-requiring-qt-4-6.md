---
tags:
- qt
- packagers
title: Requiring Qt 4.6
---
In a few days, the master branch (which will become quassel-0.7) will start depending on Qt 4.6 for the client only. Besides giving us some very welcome API additions, and fixing a few bugs we currently have to work around, this also allows us to use Qt Kinetic and the Animation Framework in the future.

Qt 4.6 has been released about half a year ago, and is also required by the current stable KDE release, so we think that most desktop distros should be up to par by now (or don't care enough about staying up-to-date, in which case they shouldn't be expected to ship a bleeding edge Quassel anyway). By the time quassel-0.7 is released, even more time will have gone by (and the next stable Qt release should be out).

The core's dep will remain at Qt 4.4.0 for now, so people running Debian Stable on their server should be ok. The deps for the current stable release 0.6.x won't be changed, so subsequent 0.6.x releases will still be fine with Qt 4.4 for the core and Qt 4.5 for the client.
<!--break-->
