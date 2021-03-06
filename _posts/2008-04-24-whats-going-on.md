---
tags: []
title: What's going on?
---
Got asked today what's happening on the Quassel front, since there haven't been many commits in the past few days, which, after several weeks of frantically committing stuff, is quite unusual... To calm down everybody: even though all devs currently are quite busy at work and in the so-called, yet mythical "Real Life" (which explains while we have gotten somewhat more quiet lately), we are still working on Quassel as well :) Read on for details on Quassel's current state and our plans for the near future!
<!-- break -->

We have put the 0.2.x branch in feature freeze, since we believe that Quassel IRC is now featureful enough to be usable. We plan to release a beta soon, followed by an RC and the final hopefully not too far in the future.

While we keep using and testing and fixing 0.2.x, we have started work on the 0.3 branch (which is not trunk yet, since we don't want to screw up the people keeping current with svn builds). This branch will include a complete new message handling architecture on the client side, based on Qt's MVC classes. This will allow us to implement much more flexible buffers (e.g. containing merged contents from multiple channels/queries, a highlight buffer and more), and it should also be much more efficient RAM-wise. We will have yet to see how efficient that turns out to be speed-wise though...
This architecture will enable us to finally start real work on the famous new ChatWidget, which will just be a view on the MessageModel (or various filtering proxy models).

Another point on the agenda for 0.3 is the long-awaited plugin interface, though we are not sure yet how extensive this will be - if we manage to implement a full-flegged scripting interface in the not too distant future, or if we'll only provide a few hooks for simple plugins as a temporary work-around...

So while our commit count seems to be down, and our channels are a little bit more dormant than usual, rest assured that a lot of good stuff is going on behind the scenes :)

Back to work.\
~ Sput
