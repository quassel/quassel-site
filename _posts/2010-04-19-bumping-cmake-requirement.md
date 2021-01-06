---
tags:
- buildsys
- packagers
title: Bumping cmake requirement
---
<a href="http://permalink.gmane.org/gmane.comp.kde.devel.core/64615">Following KDE's example</a>, Quassel's master branch (what will become 0.7.x) will require CMake >= 2.6.4 for building starting in May (about two weeks from now). The reason for this is that our KDE integration obviously uses parts of KDE's build system, and we'd like to avoid spurious bugs by something not working as expected in some random script included somewhere, just because your CMake is too old.

CMake 2.6.4 has been out for a long time (we've been at 2.8.x for ages!) and should be included in most, if not all, distros. If it isn't, you can just use <a href="http://www.cmake.org/files/v2.8/">a recent binary release for cmake</a>, untar it somewhere, and use that instead of the system installed one.

Quassel 0.6.x will continue to work fine with cmake-2.6.2; this change will only affect the development branch.
