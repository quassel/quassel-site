---
tags: []
title: quassel-0.2.0-alpha3 has landed!
---
We are pleased to announce the immediate release of <a href="https://github.com/quassel/quassel/archive/0.2.0-alpha3.tar.gz">alpha3</a>! This release contains many performance improvements, especially during core sync and backlog replay. Furthermore, buffer switches should now be much faster. Also, the sync-to-core process now is not only faster, but also much more reliable than in alpha2, where sometimes not all channels were synced.
As a bonus feature, you'll get an all new topic widget that displays mIRC-style formatting, and various other GUI tweaks.

Please note that we have broken both the client/core protocol and the database schema with this release. This means you cannot connect with an older client to an alpha3 core or vice versa. The database schema will be automatically upgraded once you run your shiny new core for the first time. Please note that after this upgrade, you will no longer be able to run a pre-alpha3 core with your database! As always, backups are recommended :)

So <a href="https://github.com/quassel/quassel/archive/0.2.0-alpha3.tar.gz">get it</a> while it's hot! Updated distro packages and precompiled binaries will soon be available on the <a href="/downloads">download page</a>.
