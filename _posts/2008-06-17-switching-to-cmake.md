---
tags: []
title: Switching to CMake
---
After our switch to Git as our version control system, we now also have changed our build system from qmake to <a href="http://www.cmake.org">CMake</a>. Long-time Quassulans will know that we already had a CMake-based build system before switching to qmake in the first place :) Back then, we decided we'd need qmake to support Qtopia, plus CMake was quite clumsy at the time (and our old build system was uber-complex). Now, it has turned out that we can easily generate Qtopia build files from any build system, plus in the meantime our qmake stuff has grown much more complex than the old system ever was - and it came to the point where qmake just couldn't do all we needed it to do anymore.
<!--break-->
So now we're back to CMake. You'll find build instructions in INSTALL.cmake (soon that will be moved to INSTALL). It has been tested on Linux, MacOSX and Windows. It is also much simpler than our old CMake-based build system, as CMake has evolved, removing the need for some of the ugly workarounds we had. Thanks to Flameeyes, we also finally have a "make install" that installs the binaries and .desktop files where they belong; soon to be followed by application icons. And last but not least, it's colorful and shiny :)

So if you happen to run buildscripts or similar, please migrate them over to the new build system, since we will be removing the qmake stuff in a few days!
