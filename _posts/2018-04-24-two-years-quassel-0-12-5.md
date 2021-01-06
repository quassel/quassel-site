---
tags:
- security
- release
title: Two Years!? - Quassel 0.12.5
---
Hi all,

yes, it's been exactly two years today since 0.12.4 was tagged… Even though development speed has picked up again recently (mostly thanks to some very active new and old contributors, and only to a small degree thanks to myself), and several hundred commits have gone into the main development branch since 0.12 was forked away, we're still some weeks away from a new feature release.

However, <a href="https://twitter.com/chaign_c/">chaign_c</a> has recently discovered two vulnerabilites in the 0.12.4 core, so <a href="/pub/quassel-0.12.5.tar.bz2">a new maintenance release</a> is warranted (and an immediate upgrade of 0.12.4 cores is highly recommended!). Since it has been so long since the last release, we've decided to backport over a hundred commits worth of bugfixes and quality-of-life improvements to make upgrading worth your while. Go grab Quassel 0.12.5 from the <a href="/downloads">downloads page<a>!

Following our usual policy, we did not change the config file format nor the database schema compared to previous 0.12.x releases, and we avoided string and UI changes. Thus, upgrading should be safe, and going back to a previous 0.12.x release is possible in case anything goes wrong anyway. Please have a look at the <a href="https://github.com/quassel/quassel/blob/0.12.5/ChangeLog#L16">ChangeLog</a> for a list of major things that went into this release, or check out the <a href="https://github.com/quassel/quassel/compare/0.12.4...0.12.5">full list of commits</a> since the last release.

I'd like to use this opportunity to thank all contributors who keep Quassel alive and kicking despite my own lack of time, be it by providing pull requests, community support, translations, testing, or just being active in our IRC channels. For this release, I want to particularly express my thanks to <a href="https://github.com/justjanne">Janne "justJanne" Koschinski</a>, <a href="https://github.com/mamarley">Michael "mamarley" Marley</a> and <a href="https://github.com/digitalcircuit">Shane "digitalcircuit" Synan</a> for their timely support in handling the afforementioned vulnerabilities so professionally, both providing fixes and very thorough testing! You rock!

Next stop (hopefully): Quassel 0.13. As announced, well, two years ago, this will be our last release still supporting Qt 4 and KDE 4. Afterwards, we'll also bump our build requirements significantly.

Until then, all the best,\
~ Sput
