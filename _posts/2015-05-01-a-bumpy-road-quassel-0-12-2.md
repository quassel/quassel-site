---
tags:
- security
- release
title: A Bumpy Road - Quassel 0.12.2!
---
Hi all,

I'm happy to announce the release of Quassel IRC version 0.12.2! This version now fully supports KDE Frameworks, so Quassel behaves properly in a Plasma 5 environment. Other new features include an improved password hashing algorithm, proper unicode-aware message splitting for both normal and CTCP messages, improved handling of PostgreSQL database connections, a bunch of bugfixes and updated translations. If you connect to a 0.12.x core, you can also now change your core password from the client. Please see the <a href="http://git.quassel-irc.org/?p=quassel.git;a=blob;f=ChangeLog;h=244824f03e443c1b73c8add0aee446ddd6ca9780;hb=9c5e6c666d5faa976eec2e0ac8bf8e1dd6c0332c">ChangeLog</a> for a more complete list.

Now you might ask: What happened to 0.12.0 and 0.12.1? This is the reason I titled this post "A Bumpy Road". Very shortly after tagging the 0.12.0 release, we've discovered a behavior change in Qt5 in regards to timezone handling in PostgreSQL databases. This resulted in backlog messages being stored with the wrong timezone information for some server setups. The fix for this went into the 0.12.1 release. Unfortunately, this fix also uncovered a more serious issue that has been around for a long time: restarting a PostgreSQL database while Quassel Core is running would not properly re-initialize the database session inside Quassel, bringing back an old <a href="http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2013-4422">security issue</a> that we had deemed fixed. This forced us to create yet another release, so that's why we are now at version 0.12.2. The new issue is being tracked as <a href="https://marc.info/?l=oss-security&m=143014582328491&w=2">CVE-2015-3427</a>. Thanks to Pierre Schweitzer for registering this!

To be clear: <em>We strongly recommend upgrading Quassel to 0.12.2 due to vulnerabilities in older versions, or backporting the patches referenced in the relevant CVE entries!</em> We have also prepared a <a href="http://quassel-irc.org/pub/quassel-0.11.1.tar.bz2">0.11.1 release</a> that contains the security fixes, but no new features. Older versions are no longer supported.

With that out of the way, we hope that you'll enjoy the new version of Quassel! Head on over to our <a href="/downloads">downloads page</a> to grab it, or wait for your favorite distro to provide packages!

Cheers,\
~ Sputnick on behalf of the Quassel Team
