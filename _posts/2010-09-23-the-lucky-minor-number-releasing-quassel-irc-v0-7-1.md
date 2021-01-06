---
tags:
- packagers
- release
title: The Lucky (minor) Number -- Releasing Quassel IRC v0.7.1
---
It's that time of the year when we're releasing a new Quassel, and this time <strong>we strongly recommend updating your core or monolithic client</strong> at least, as in older versions there was an issue with CTCP handling that might allow bad and ugly people to make your core unresponsive. This issue is also the reason for the 0.7.0 release being officially skipped. People still on 0.6.x and not wanting to update to a new feature release should upgrade to <a href="https://github.com/quassel/quassel/archive/0.6.3.tar.gz">version 0.6.3</a> in which this issue is fixed as well.

Now read on for a short list of the major new features <a href="https://github.com/quassel/quassel/archive/0.7.1.tar.gz">the 0.7 flavour</a> gives you, besides a ton of bugfixes and translation improvements!
<!--break-->

<ul>
<li>Improved Desktop Environment integration: We now properly support DBusMenu (which gives you a proper tray menu in both GNOME and KDE), improved Ayatana support, and fixed some issues with StatusNotifier</li>
<li>Editable shortcuts for all platforms, not only KDE</li>
<li>Shortcuts for navigation between chats (Alt+Left/Right/Up/Down) -- though there are still some known bugs there</li>
<li>Emacs-style keybindings for the input line</li>
<li>Marker line can now be set manually (Ctrl+R), and one can jump directly to the marker line (Ctrl+K)</li>
<li>Blowfish encryption (via /setkey and /delkey), also known as mircryption, FiSH or RFC 2045</li>
<li>Fullscreen mode</li>
<li>New languages: Greek, Galician, Japanese</li>
</ul>

You can grab <a href="https://github.com/quassel/quassel/archive/0.7.1.tar.gz">the tarball</a> and the usual binary packages on our <a href="/downloads">download page</a>.

Now on to rewriting most of the core on the road to scripting support!\
~ Sputnick
