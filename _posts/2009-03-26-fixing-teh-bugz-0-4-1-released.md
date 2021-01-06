---
tags: release
title: 'Fixing teh bugz: 0.4.1 released'
---
We have recently tagged a bugfix release for the stable branch, appropriately named 0.4.1. Users of 0.4.0 are heavily recommended to upgrade. Note that no new features have been added; users of the development version from git should not use 0.4.1 as it would be a downgrade.

Some of the bugs fixed include:
<ul>
<li>Correctly display images in the web preview in static builds</li>
<li>Improve selection and multi-line paste behavior</li>
<li>Fix cert handling for identities</li>
<li>Create a proper default identity for new networks</li>
<li>Improve ping timeout detection (don't time out after 30 seconds with a shaky connection)</li>
<li>Fix bufferview sorting</li>
<li>Updated and new translations: Slovenian, Russian, French, Czech, German, Turkish</li>
<li>Improve flood control (avoiding Excess Flood in most cases)</li>
<li>Various improvements to the build system</li>
</ul>

You can grab the new release from our <a href="/downloads">download page</a>; many distributions also have updated packages available already.
<
