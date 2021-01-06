---
tags: []
title: Static alpha3 core for Linux
---
Many people don't have Qt installed on their servers (even though the needed parts can be installed without X11), which makes using Quassel quite cumbersome. I have been looking into providing a static core (i.e. one that does not have external dependencies like Qt) for a while now, but on Linux, this is surprisingly hard. Anyway, on the <a href="/downloads">download page</a> you'll now find an experimental core to try out even on servers without Qt.

Note that this is highly experimental, since certain features seem to require a compatible shared glibc installed. Also on one of my test systems, charset encodings don't work, because iconv cannot be used even though it is installed... so please test it, and if anything is strange, please report.
