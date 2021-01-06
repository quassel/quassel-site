---
tags:
- packagers
- release
title: We are back - with Quassel 0.8.0
---
Has been a while that this page has seen updates, as we, the main developers, are still too busy with real life to get as much done as we would like. So many plans, so little time...

Thankfully, we have some pretty awesome guys from the community (al, Tucos, johu, kode54, Fish-Face, to name but a few) who help out not only with support in our IRC channel, but also with triaging bugs, and especially with sending patches. So we finally managed to clean out our merge request queue and got a new feature release going!

Quassel 0.8.0 brings you the usual slew of bugfixes, a ton of new languages and additional translations for the existing ones, and a few new features such as syslog support, configurable tab completion key, improved desktop integration and more.

Behind the scenes, and hopefully not noticeable for you, we've merged the new event backend into the core. This is more or less a complete rewrite of how the IRC protocol is handled, and the first major step towards full scripting support!

So don't hesitate to <a href="/downloads">grab the new release</a> and get rollin'!

<b>A note for packagers:</b> The Qt 4.8 release introduced an issue with QTreeView handling that causes parts of the nick list (and sometimes the chat lists) not being shown sometimes. For distributions that don't believe in frequent feature upgrades, we've rolled <a href="https://github.com/quassel/quassel/archive/0.7.4.tar.gz">a 0.7.4 release</a> that only contains this and some other bugfixes, but does not introduce new strings or features. If your distribution backports Qt 4.8, we warmly recommend backporting this version of Quassel as well!

That's all.\
~ Sput
