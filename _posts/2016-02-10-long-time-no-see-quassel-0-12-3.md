---
tags:
- release
title: Long Time No See - Quassel 0.12.3
---
Hi all,

it's been a while that we did <a href="/pub/quassel-0.12.3.tar.bz2">a new release</a>, and it's still "just" a bugfix release this time. Turns out that real life is still keeping us busy... but it's the good kind of busy, so there's that. Thankfully, we have a bunch of cool people in the community who contribute patches, fixes and features while the core development team is on semi-hiatus -- many thanks to all of you!

Anyway, say hello to <a href="/pub/quassel-0.12.3.tar.bz2">Quassel 0.12.3</a>. Many fixes went into that one, and we encourage you to upgrade! One particularly nasty bug was fixed: if you have multiple users on a single Quassel Core, and use PostgresQL as a database backend, messages could be lost in earlier 0.12.x versions. So if you happen to run 0.12.{0..2}, and run a core for multiple users, you definitely should upgrade. A more extensive list of fixes can be found in the <a href="https://github.com/quassel/quassel/blob/0.12.3/ChangeLog">ChangeLog</a>.

A short heads-up: The next feature release (0.13.x) will be the last one still supporting Qt 4 and, consequently, KDE 4. Supporting two diverging frameworks (Qt 4 and Qt 5), and two rather different desktop environments (KDE 4 and Plasma 5), proves to be increasingly challenging. Additionally, Qt 4 has officially reached end-of-life by now. So once 0.13 is release, we'll take the opportunity to clean up the codebase and remove a few hundred #ifdefs, wrappers and workarounds! This is still a few months away, and we plan to add a long-desired feature or two to the next release -- but now you know and can prepare for life after Qt 4!

That's it for today. Please head to the <a href="/downloads">downloads page</a> to grab the new source tarball. Binary packages for the various platforms will show up there over the next few days, and if you run Linux, I'm sure your friendly package maintainer is already working on getting an updated package near you soon!

Have a nice one!\
~ Sput
