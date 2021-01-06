---
tags: release
title: Releasing the (hopefully) final Alpha for Quassel 0.2.0!
---
It is with great pleasure that we announce <a href="/downloads">immediate availability</a> of what will probably/hopefully/may be the last and final alpha release before we go into the beta cycle. As usual, this alpha release brings you bugfixes and new features, UI tweaks and more goodies, and we highly recommend upgrading. Especially since we fixed a very nasty issue in Quassel Core... and yeah, the fonts should now be working as well :) Also, we can finally provide a precompiled Quassel Core and monolithic Quassel for Windows™, so you should now be able to use it without having access to a *nix server... And we don't forget the MacOSX Tiger users either and now provide a package that runs on both MacOSX 10.4 and 10.5.

For a more detailed list of important changes, read on!
<!--break-->

### Bugfixes:
- Stopped quasselcore from potentially filling up your database with millions of strings when receiving invalid CTCP
- A saner autowho implementation avoids throttling when sending messages to some networks, removing that annoying send lag you might have experienced
- Font issues (garbled fonts, wrong formatting...) have been fixed
- Finally allow parallel makes (make -j<n>)
- Made the core run on Windows™ as well
- Made Quassel compile and run on MacOSX 10.4 (Tiger)

### Features:
- Custom highlights
- Lots of UI tweaks
- QuasselTopia compiles and sorta runs again... well, this is still highly work-in-progress and probably breaks again soon enough.

We will now work on finalizing the feature list and removing the last outstanding issues for Quassel's first beta release, which we expect to release in a couple of weeks.
