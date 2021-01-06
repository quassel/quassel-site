---
tags:
- security
- packagers
- release
title: 'Yet Another Important Update: Quassel 0.9.2'
---
Hi all,

the last update in the 0.9.x series has been released only a few weeks ago, and now it's already time for <a href="/downloads">another one</a>. Besides various bugfixes (among those, Phonon notifications play sound again!), and a bunch of new and improved translations, the main reason for this one is, unfortunately, another vulnerability: with a carefully manipulated client, you can retrieve the backlog of other users on the quasselcore you're using. Proper authentication is still needed, so this will only affect people who allow untrusted and malicious users on their shared core. Still, an upgrade is highly recommended.

If you happen to be a distro packager, please be advised to backport (i.e. simply apply) <a href="https://github.com/quassel/quassel/commit/1fc8eb59a87c005ddfe7d21bc225bef8692b9743">this</a> and, if you haven't done so yet since the release of 0.9.1, <a href="https://github.com/quassel/quassel/commit/aa1008be162cb27da938cce93ba533f54d228869">this</a> patch to your packages, if you can't bump them to 0.9.2 for release process reasons.

Well, here's hoping that next time we won't have that sense of urgency again :)

Have a nice day, and happy updating,\
~ Sput
