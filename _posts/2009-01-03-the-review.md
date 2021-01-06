---
tags: []
title: The Review
---
Since people keep asking us what our view is on the <a href="http://weblog.obso1337.org/2008/expert-review-of-quassel-031/">usability review</a> seele recently did about Quassel IRC, I thought I should blog a little something.

First of all, it didn't hit us as a surprise. We've been in contact with kubuntu about their plans before, and we've ongoing discussions with seele and other kubuntu devs about how to make Quassel suitable for new users, in particular for kubuntu's main target group. Many things seele mentions in her review have been on our TODO list for a while now, but of course, being developers, we tend to put such issues off in favor of new features... now this whole thing shifts our priorities to focus on usability for a change. Sorry guys, this also means scripting support has to wait again...

Meanwhile, <a href="http://apachelog.blogspot.com/">apachelogger</a> is busy making the Quassel packages rock on kubuntu, and now provides nightly Quassel builds via <a href="http://amarok.kde.org/wiki/User:Apachelogger/Project_Neon/KDE/Info">Project Neon</a>. And the Quassel developers, of course, are now busy to convert the review into code :)

Read on for some specific points.
<!--break-->

The main issues we have on our agenda now:
<ul>
<li>Streamline the monolithic client to act more like a traditional IRC client</li>
<li>Provide better defaults</li>
<li>Make configuration easier</li>
</ul>
The first issue, of course, is key to provide a good first-run experience for users who are not familiar with Quassel's client/core concept, or who are just looking for a "normal" IRC client. Of course, we mainly had that use case in mind when we decided to provide a monolithic client. As seele points out, currently our core connection dialog does not make it obvious how to use Quassel like that. We will streamline this to make the internal core more prominent (i.e. don't ask for creating a remote core account), and probably add a way to directly enter network and identity settings if one wants to use the internal core. We won't completely remove the ability to connect to remote cores from the monolithic clients; we'll rather make it clear that this is an advanced feature. For kubuntu, we will probably add a compile-time option to hide the remote core options altogether by default. This should help new users to quickly get started with Quassel, and still allow advanced users to use remote cores.

"Better defaults" mainly concerns the buffer views we show when you start Quassel for the first time. Many of our users don't even know that they can create custom views which allow the hiding and rearranging of channels. Instead, we plan to create a sensible set of custom views by default, and hide the "All Buffers" view. In fact, EgS has recently added a way to unhide hidden channels without resorting to the All Buffers view. Lack of that ability was the main reason for even having the All Buffers view, so this is the first step in making this better.

The configuration dialogs need some love as well. seezer is already busy fixing many of the UI issues seele pointed out, and I will tackle the styling options soon (i.e., make setting colors and fonts easier). With KDE integration enabled, you already get the standard "Configure Notifications" dialog from KDE rather than our own notifications, which should help to remove confusion about all the different options.

There are more issues, of course, and we'll see how far we get with those until kubuntu goes into version freeze. Rest assured that the Quassel developers put a lot of effort into this, so the next release should have some visible improvements for you guys :)

Back to hacking now. Oh, and a Happy New Year!\
~ Sput
