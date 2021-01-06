---
tags:
- release
title: Doing Some Maintenance - Quassel 0.13.1
---
Hi all,

we're back in 2019 with a maintenance release for the 0.13 cycle, Quassel 0.13.1. Besides a handful of fixes and improvements over the previous release, 0.13.1 fixes a particularly annoying issue with 0.13.0 on Qt4-based systems where backlog messages would not all be fetched. I'd like to thank <a href="https://github.com/justjanne">Janne "justJanne" Koschinski</a> and <a href="https://github.com/digitalcircuit">Shane "digitalcircuit" Synan</a> in particular for finding the cause for this problem, as well as implementing and testing the fix!

So if you happen to run Quassel 0.13.0 on a system or distro still using Qt4, be sure to upgrade (or ask your friendly distro maintainers to do so), otherwise your chat history may be spotty... Official 0.13.0 builds for Windows and OSX already use Qt5, so they're not affected. Also any recent distro release should have done the migration already, as Qt5 has been out for quite some time.

Quassel 0.13.1 also makes database schema upgrades more robust by making them resumable, and allows to configure the listen addresses for the built-in identd. Please see the <a href="https://github.com/quassel/quassel/blob/0.13.1/ChangeLog#L16">ChangeLog</a> for a full list of changes.

As always, you can find the <a href="/pub/quassel-0.13.1.tar.bz2">sources</a>, as well as precompiled binaries for Windows and OSX on the <a href="/downloads">downloads page</a>.

Cheers,\
~ Sputnick
