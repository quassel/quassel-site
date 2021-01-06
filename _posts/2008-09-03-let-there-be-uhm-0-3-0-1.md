---
tags: release
title: Let there be, uhm, 0.3.0...1!
---
After quite a long while, we finally <a href="/downloads">present</a> to you a new shiny Quassel IRC release! It so happened that we decided to call it 0.3.0.1, which, as attentive readers will certainly notice in an instant, is not the long-expected 0.2.0 (and not even 0.3.0, for that matter). So, uhm, what's up with those Quassel developers and their versioning scheme?

As some of you know, we have been working on a rewrite of the old ChatWidget for quite some time now, and it was always planned that this rewrite would end up as a 0.3 release, whereas the old ChatWidget would live in 0.2. It turned out that we would not only rewrite the ChatWidget (which is now called ChatView), but also most of the client-side message handling. We have switched to a Model-View-Controller-based architecture now. Other than being much easier to maintain and improve on, this approach also allows maximum resource sharing (for example, a chatline is now only stored once, no matter how many ChatViews display it). This results in a Quassel Client that needs much less RAM than versions from the 0.2 branch. Also, we have been (and still are) working on making things more efficient both time- and space-wise, and the current 0.3.0.1 client is already much leaner and meaner than 0.2.0-rc1.

In addition to that architectural rewrite and the optimizations, with the new ChatView and its new and improved code base we could finally start adding new features and improvements to your chat window. So you'll notice a bunch of new stuff, like visible column handles, a last-seen remember line, in-buffer search and more. I won't give you a comprehensive list of new features this time, since it's just too much - just <a href="/downloads">check it out for yourself</a>!
<!--break-->

So, back to versioning. We've been developing 0.3 in parallel while stabilizing 0.2.0 for several months, when we suddenly noticed that 0.3 had become more stable than 0.2 in the meantime, in addition to all the new features and shiny stuff it got... sure, there are still some minor regressions caused by rewriting everything, but overall, we were much happier with 0.3 than with 0.2. And since it doesn't make sense to maintain an inferior version that is not even more stable than the new stuff, well, we decided to pull a Larry[*] and just skip over to 0.3.0.

Of course, and in accordance to Murphy's Law, it took us less than an hour after the tagging to realize that some really annoying bugs had crept into the release in the last minute. So we decided to, well, skip over 0.3.0 as well, worked hard during the past week to fix the most annoying bugs, and now finally officially let this bugfix release out in the wild :)

Since Murphy never sleeps, it took us only 2 minutes after tagging this time until we got alerted that 0.3.0.1 won't actually build on Windows, and MacOSX. But, oh well. If you plan to build your own binaries on those platforms, please get a current checkout of the 0.3.0-backport branch rather than the 0.3.0.1 tag. On our <a href="/downloads">download page</a>, you'll find pre-built binaries for all platforms as usual.

Oh, you probably are not surprised by now that we've changed the core/protocol between the 0.2 and 0.3 versions, so you should be aware of the fact that a 0.2 client won't work with a 0.3 core and vice versa. Upgrading the core will work seamless, upgrading the client will remove custom color settings you might have had, but otherwise work seamless as well. As usual, downgrades are not supported.

Another known issue is that Quassel Client will start eating CPU after running for a while (a day or so). We are working on finding the cause for that, but for now, please bear with us.

Now enough of the blabbering, go grab your shiny new Quassel and have fun with it :)

~ Sputnick

[*] There never was a fourth part!
