---
tags:
- release
- packagers
title: New Cuties - Quassel 0.11.0
---
Hi all,

It's that time of the year again for <a href="/downloads">another Quassel release</a>! For 0.11.0, we've focused mainly on full support for Qt 5.2+ (in addition to Qt 4.6+, which will be supported alongside for the time being). Since Qt 4.x has not seen much development for quite some time, and subsequently we've missed out on much work that has been done by the Qt developers, this marks a major improvement in particular for our users on Windows and Mac OSX. Support for both platforms has seen many improvements in Qt 5, and thus our <a href="/downloads">official packages</a> for those platforms are now built against Qt 5. In particular Mac users should be much happier now!

For KDE users it is recommended to still use Quassel built against Qt 4, because KDE integration support has not been ported to the new KDE Frameworks yet. This is something we plan for Quassel 0.12, so stay tuned!

In order to make dual-Qt support easier, we fully revamped the build system, something that was long overdue. The existing build system still came from the dark CMake 2.6 ages, and it was increasingly hard to maintain. So now everything has been rewritten, taking newer CMake features into account. Some build options have changed as a result; in particular, we use package properties now for finding optional dependencies rather than CMake defines. After configuring the build, CMake will output a summary of required and optional packages that could or could not be found, alongside with information on what a particular dependency does and where to find it. The <a href="http://git.quassel-irc.org/?p=quassel.git;a=blob;f=INSTALL;h=a9dc9e2b3762f09c08761550cc03812099ac1768;hb=HEAD">INSTALL</a> file has been updated accordingly.

Starting with 0.11, we also increased the build requirements. A C++11 capable compiler, such as gcc 4.7+, Clang 3.1+, or Visual Studio 2013 (at least the November CTP), is now needed in order to build Quassel from source. In addition, at least CMake 2.8.9 is required. We feel that these are reasonable requirements that should be supported by most current distributions (and there were no objections when we asked around).

Besides these major changes, this release also contains a bunch of bugfixes, most generously provided by our awesome community. Among other things, the handling of database errors has been improved, we now split CTCP lines that are too long (important for role players using /me a lot, I'm told), and some issues with QuasselDroid have been fixed. For those of you who you only want to get those fixes, but not the build system changes, Qt 5 support and the increased build requirements, we tagged <a href="/pub/quassel-0.10.1.tar.bz2">Quassel 0.10.1</a>. This bugfix release marks the last of the 0.10.x releases; we will not provide further support for this branch (as usual).

And now, get downloading unless your friendly package maintainer has already done this job for you!

Cheers,\
~ Sput
