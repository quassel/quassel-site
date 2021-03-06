---
tags:
- release
title: Fixing Bugs - Quassel 0.12.4
---
Hi all,

while feature development is still slow -- too slow for my own taste, really, but what can you do -- some rather annoying bugs have been fixed that warrant another maintenance release. Most notably, Tucos (thanks a lot!) has figured out that invalid handshake data may cause the core to crash. Another annoying issue was the lack of support for the STATUSMSG feature available in some IRC networks. This one was recently abused by idio^Wpeople to pop up tons of spam queries for some of our users.

Both issues are fixed in <a href="/pub/quassel-0.12.4.tar.bz2">version 0.12.4</a>. We highly recommend people to upgrade their cores, and distros to backport the related patches to older versions they still maintain. As a bonus, translations have been updated for this release, and support for non-compliant IRC networks has been improved. You can find the usual artifacts on our <a href="/downloads">downloads page</a>.

Here's hoping that my next blog finally talks about new features instead of new bugs!

All the best,\
~ Sput on behalf of the Quassel Team
