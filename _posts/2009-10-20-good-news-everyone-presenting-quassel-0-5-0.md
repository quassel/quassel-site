---
tags: release
title: 'Good News Everyone: Presenting Quassel 0.5.0!'
---
It's been a while that we have announced a new release. Somehow, 0.4.2 and 0.4.3 never made it to the frontpage… Anyway, we haven't been lazy and quietly worked on bringing you a brand new feature release: <a href="/pub/quassel-0.5.0.tar.bz2">quassel-0.5.0</a>!

You can find most features we have added in the <a href="/pub/ChangeLog">FeatureLog</a>, and if you are <em>really</em> interested, you can also browse the <a href="http://git.quassel-irc.org/?p=quassel.git;a=shortlog;h=refs/heads/0.5">Git history</a>. A list of the most important things has been added below for your convenience. First though I want to get a few important notes out:

<b>Client/Core protocol, database schema and config file update:</b> As mentioned before, a 0.5 Quassel Core will not work with a 0.4 client and vice versa. You will have to update both components. First time you run a 0.5 core or client, the config files and database will automatically be updated to the new format. Downgrades are not supported, so do make a backup if you intend to go back to 0.4 afterwards!

<b>A note for distro packagers:</b> We will maintain a <a href="http://git.quassel-irc.org/?p=quassel.git;a=shortlog;h=refs/heads/0.5">0.5 branch</a> in our repository that will receive important bugfixes, but no new features. We will probably also do periodic 0.5.x releases from this branch, while new and shiny stuff is being added to the master branch. If you maintain Quassel on a distro that suffers from version or feature freezes, you should make sure to track the 0.5 branch instead.

Read on for a short list of the most important features, then head over to the <a href="/downloads">downloads page</a> to grab it while it's still sizzling!
<!--break-->

<ul>
<li><b>PostgreSQL Support</b>. In addition to SQLite, the core now also supports using a postgres database for storage. This is recommended in particular if you run Quassel core with several users, as SQLite tends to get slow then. Run <code>quasselcore --help</code> for information about how to switch (your data will be automatically migrated to the new backend if you select it).</li>

<li><b>/exec Support.</b> This allows for running external scripts or programs and piping their output into IRC. For Linux, we provide a sysinfo script (<code>/exec inxi</code>) and a now-playing script for MPRIS-compliant media players such as amarok (<code>/exec mpris amarok</code>).</li>

<li><b>Ignore List.</b> Yes, finally you can get rid of all the trolls (no, I don't mean you, Nokia Trolls! ;-)… either dynamically (so you can retroactively show them again) or permanently (in which case they won't get into your database at all).</li>

<li><b>Multiline Input.</b> A long requested feature that allows you to have multiple lines in your input field and edit them before sending them off all at once. Press Shift+Enter to start a new line, or paste something with more than one line into the input field.</li>

<li><b>Smart Nick Completion.</b> Quassel will now prefer users that have last talked in a channel, instead of going through the nicknames alphabetically. This should greatly reduce "mis-tabbings" ;-)</li>

<li><b>Full Stylesheet-Based Styling.</b> We have extended support for Qt stylesheets (QSS) to allow extensive styling of the chat window. As an example (and for getting back the nice and colorful appearance we had in prior versions of Quassel), you can select the m4yer.qss stylesheet that should be installed in your data dir. We will work on improving this feature in future versions, and also document how it works soon.</li>

<li><b>Usability Improvements.</b> Most notably, we have renamed all occurences of "Buffer" to "Chat", so instead of Buffer Views, we now have Chat Lists. This has been done because users not familiar with curses-based IRC clients (or Emacs) were getting confused with the term "Buffer". In addition, we have redesigned and reorganized more configuration dialogs, and removed the dreaded color settingspage.</li>

<li><b>Performance Improvements.</b> Ever had trouble with Quassel Core taking minutes for starting up or shutting down? Ever noticed that joining or leaving a large channel could stall both client and core for ages? This has been fixed thanks to an improved client/core synchronization protocol.</li>
</ul>
For a more complete list of new stuff, please have a look at the afforementioned resources, or just try it out yourself!

~ Sputnick out.
