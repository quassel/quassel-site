---
tags:
- release
title: Into the Double Digits - Quassel 0.10.0 Is Out!
---
Hi all,

we proudly announce the latest release of Quassel IRC, version 0.10.0! As promised, development has become more active in the past few months (both because we gained several new contributors (thanks a bunch!), and I myself have finally some more time for development), so besides a host of bugfixes that already went into 0.9.x, this development cycle also saw various new features as listed in the <a href="https://github.com/quassel/quassel/blob/0.10/ChangeLog">ChangeLog</a>. Besides, for example, various improvements related to SSL connections, optional multi-line input field, support for the <a href="https://github.com/TheOneRing/Snorenotify">Snore notification framework</a>, the ability to show backlog messages in the ChatMonitor (beware though; it will slow down your sync!), the possibility to hide inactive networks in your Chat List, more translations, and a new version of the <a href="https://code.google.com/p/inxi/">inxi</a> (/sysinfo) script, this release features a new core/client protocol: the DataStream protocol.

This new protocol is one (intermediate) result of the refactoring work that has been going on behind the scenes for several releases now, aiming for separating out protocol-specific code from the rest of the codebase in order to be able to do things like, well, replacing the protocol (and making it easier for third-party client authors to work with it). The DataStream protocol is not much different from the original ("legacy") protocol, but it removes some of the unnecessary overhead. Due to a change to data compression, <a href="https://play.google.com/store/apps/details?id=com.iskrembilen.quasseldroid">QuasselDroid</a> can finally use compression when connecting to a 0.10.x quasselcore! You can read more about the protocol changes in <a href="http://bugs.quassel-irc.org/projects/quassel-irc/wiki/Doc_quassel_protocols">the Wiki</a> (work in progress). Note that we kept backwards compatibility, so using a new client with an older core, or vice versa, is fine (but won't get you the new protocol, of course).

That's about it. Go now and grab the newest version from our <a href="/downloads">downloads page</a>, or directly from your friendly distro's repositories once it's there!

One last note for people following development closely and interested in the goings-on in Git: The <a href="https://github.com/quassel/quassel/commits/master">master branch</a> has seen a revamp of the build system and features full support for Qt5 now (minus some glitches). Soon, we will start using C++11, as <a href="http://lists.quassel-irc.org/mailman/pipermail/quassel-devel/2014-March/000007.html">announced previously</a>; so make sure to update your toolchain if it's ancient!

Cheers,\
~ Sput on behalf of the Quassel Team
