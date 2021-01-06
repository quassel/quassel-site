---
tags:
- prerelease
title: The Final Stretch - Quassel 0.13-rc2
---
Hi all,

the first release candidate for the impending 0.13 release uncovered some issues, the fixing of which required some more complex changes than we would have liked. Thus, we decided to roll a second release candidate.

Most significant changes compared to rc1:

- Rework the init and shutdown sequence as well as signal handling to properly clean up everything on shutdown
- Rework the handling of regular expressions e.g. for ignore and highlight rules for more flexibility and better performance. This may break legacy ignore rules; see the <a href="https://bugs.quassel-irc.org/projects/quassel-irc/wiki/Pattern_matching#Migrating-to-Quassel-013">migration guide</a> for more information

Please see the <a href="https://github.com/quassel/quassel/blob/0.13-rc2/ChangeLog">updated ChangeLog</a> for more. Of course, the information and caveats mentioned in the <a href="/node/132">release announcement for 0.13-rc1</a> still apply.

Please head on over to the <a href="/downloads">downloads page</a> to grab the packages, or just click here:
- <a href="/pub/quassel-0.13-rc2.tar.bz2">Source tarball</a>
- OSX <a href="/pub/QuasselCore_MacOSX-x86_64_0.13-rc2.dmg">core</a>, <a href="/pub/QuasselClient_MacOSX-x86_64_0.13-rc2.dmg">standalone client</a>, <a href="/pub/QuasselCore_MacOSX-x86_64_0.13-rc2.dmg">monolithic client</a>
- Windows installer (<a href="/pub/quassel-x86-setup-0.13-rc2.exe">32 bit</a>, <a href="/pub/quassel-x64-setup-0.13-rc2.exe">64 bit</a>) containing core, client and the standalone client

We expect to do a final 0.13.0 release in just a few days, pending discovery of serious issues that would warrant another delay.

Cheers,\
~ Sput
