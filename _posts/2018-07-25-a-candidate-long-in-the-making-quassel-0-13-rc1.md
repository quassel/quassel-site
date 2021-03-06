---
tags:
- prerelease
title: A Candidate Long in the Making - Quassel 0.13-rc1
---
Hi all,

more than three years since 0.12.0 was released, and over 500 commits on top of what went into the current stable branch, we're finally in the last stretch of the next major feature release!

Since so much work and <a href="https://github.com/quassel/quassel/blob/0.13-rc1/ChangeLog#L16">changes</a> went into this, this time we've decided to not only roll a release candidate, but also announce it publicly, so daring people can test things before final release.

Some caveats upfront: Both the database schema and the config file formats have been updated since 0.12. Quassel will automatically upgrade both once the new version is started for the first time, however <strong>no rollback is possible</strong>, so do make a backup! Also the upgrade may take a <em>long</em> time (several hours) if your database is (un)reasonably large, during which the core or mono client cannot be used. The upgrade may also temporarily require up to double the disk space. Do not interrupt the upgrade process, otherwise your database may become corrupted!

Nevertheless, the Quassel protocol between remote cores and clients still is backwards-compatible all the way down to 0.5.0, which was released in 2009. While you may not be able to use all the newer features when connecting to older versions, things still work, and there is no need to upgrade both ends at the same time.

This is also a <strong>call for translators</strong>. If you'd like to improve the localization of Quassel in your language, please head over to <a href="https://www.transifex.com/quassel/quassel/">Transifex</a> and contribute. We'll merge back the updated translations shortly before final release of 0.13.0.

Too many changes went into this release to be able to list them all (have a look at the <a href="https://github.com/quassel/quassel/blob/0.13-rc1/ChangeLog#L16">ChangeLog</a> for a reasonable overview), but here are some highlights:

- New branding, more modern icons (from the Breeze icon theme)
- Better support for icon themes
- Many UI improvements
- Support for many IRCv3 features, including the display of modern formatting codes
- Functionality such as highlights and chat activity tracking move into the core to help <a href="https://quasseldroid.info/">mobile clients</a> to be more efficient
- Support for containerization, i.e. config-less core
- Optional authentication via LDAP
- Database improvements, including support for 64 bit IDs and timestamps, and performance tweaks
-... and much more!

The usual packages are available for download now:
- <a href="/pub/quassel-0.13-rc1.tar.bz2">Source tarball</a>
- OSX <a href="/pub/QuasselCore_MacOSX-x86_64_0.13-rc1.dmg">core</a>, <a href="/pub/QuasselClient_MacOSX-x86_64_0.13-rc1.dmg">standalone client</a>, <a href="/pub/QuasselCore_MacOSX-x86_64_0.13-rc1.dmg">monolithic client</a>
- Windows installer (<a href="/pub/quassel-x86-setup-0.13-rc1.exe">32 bit</a>, <a href="/pub/quassel-x64-setup-0.13-rc1.exe">64 bit</a>) containing core, client and the standalone client

We're discontinuing the pseudo-static core, because creating static binaries that run on most platforms becomes increasingly fragile; bundling things like OpenSSL also introduces security risks, since the bundled version will not be updated with the system. Additionally, our binary packages for OSX and Windows do not support the PostgreSQL database backend for the core due to limitations in our build environments, as well as lack of demand.

Do let us know if you run into issues or regressions. Otherwise, we're expecting a final release in the coming weeks!

**NOTE:** As announced several times already, 0.13.0 will be the last feature release still supporting Qt4 and KDE4. We'll significantly bump the build and runtime requirements for future releases in order to be able to modernize the code base. Planned baseline for 0.14 onwards is Ubuntu 16.04 "Xenial", as well as reasonable recent toolchains for OSX and Windows.

That's it for now!

Always yours,\
~ Sput
