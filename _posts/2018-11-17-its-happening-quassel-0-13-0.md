---
tags:
- release
- packagers
title: It's happening! - Quassel 0.13.0
---
Hi all,

1312 days have gone by since the last feature release of Quassel IRC. At times, the project went almost dormant; then it was buzzing with activity again due to some very active contributors (digitalcircuit, justJanne, romibi, mamarley, just to name a few). And in the end, even I could not help myself and had to start coding again! As a result, we can finally unleash a new feature release on you. And what a release it is!

We have a new branding and application icon, support the modern Breeze iconset, and improved icon theme support as a whole. We added a whole bunch of UI improvements, from the ability to show user modes in chat to spell checking on all platforms. Many IRCv3 features are now supported, including the rendering of almost all of modern formatting options. New authentication and configuration options allow for containerization, or for using an LDAP backend for the core. The database now uses 64 bit message IDs and timestamps, making it future-proof for giant backlogs and the year 2038.

Much work went into supporting mobile clients better and improve performance. For example, chat activity tracking and highlight rules moved into the core, so clients don't need to pull all the backlog at once. The first mobile client to benefit from this is <a href="https://quasseldroid.info/">Quasseldroid</a>, which itself has seen a full rewrite that will soon be released to Android phones near you. Of course, these improvements also lay the groundwork for future improvements for the desktop client's performance.

Please see the <a href="https://github.com/quassel/quassel/blob/0.13.0/ChangeLog">full ChangeLog</a> for a more detailed list of changes.

Before you upgrade, please be aware that both the database schema and the config file formats have been updated since 0.12. Quassel will automatically upgrade both once the new version is started for the first time, however <strong>no rollback is possible</strong>, so do make a backup before starting the new version! The upgrade may take a long time (up to several hours) if your database is (un)reasonably large, during which the core or mono client cannot be used. The upgrade may also temporarily require up to double the disk space. Do not interrupt the upgrade process, otherwise your database may become corrupted!

With that out of the way, please head on over to the <a href="/downloads">downloads page</a> to get yourself a fresh Quassel tarball, Windows installer or OSX package. Or wait until the new version hits a distro near you! As always, feel free to join us in #quassel on the <a href="https://freenode.net/">Freenode IRC network</a> if you have questions, or just want to talk to our friendly community.

One final remark: As we have announced a few times now, the 0.13 release cycle is the last one still supporting the all-but-dead-for-years Qt4 and KDE4 libraries. But this it not the only change; behind the scenes, we have already been very busy modernizing the codebase, and we will merge a giant pile of changes into the master branch soon after branching out 0.13. Going forward, Quassel will require a more recent toolchain, as well as system libraries; the baseline we have chosen for the time being is Ubuntu 16.04 "Xenial", with no intention to support older versions than what's available there. We hope that this won't affect too many users; we think supporting a more than three year old setup is reasonable, and it gives us the opportunity to do some sorely needed cleanup and use modern C++ features and libraries going forward.

With all that said, I'm wishing you a nice weekend, and hope you like the new Quassel 0.13.0!

Cheers,\
~ Sput
