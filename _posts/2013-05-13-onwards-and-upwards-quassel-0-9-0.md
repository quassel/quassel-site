---
tags:
- packagers
- release
title: Onwards and Upwards - Quassel 0.9.0!
---
Yes, yes, I know. Again I have been too quiet on this page, while several major changes have happened in my real life. However, things are slowly settling down, and I could spend more time on Quassel again during the past few months. And as usual, the community has been active as well providing patches, fixes and features - thank you all for that!

So without further ado, I present to you <a href="/downloads">Quassel 0.9.0</a>!

A list of the most important changes can be found in the <a href="https://github.com/quassel/quassel/blob/0.9/ChangeLog">freshly updated ChangeLog</a> - improved certificate handling, improved OSX support, DockManager compatibility, channel-specific highlights just to name a few features that have been contributed by the community (special thanks goes out to Tucos, who is restless indeed).

Meanwhile, I am slowly continuing to refactor the heart of Quassel, which is the communication between the client and the core. My goal is to abstract the protocol, so in the future it will be easier to write third-party clients. Having a clean protocol abstraction is also a prerequisite for getting things like events and scripting going. Expect more news along those lines in the future!

Oh, we've also switched to <a href="https://github.com/quassel/quassel">GitHub</a> as primary means for source code hosting and managing contributions. The main reason for this is that people were unhappy with Gitorious because it was slow, sometimes unreliable, and has a less advanced web interface. So please, if you like to send patches, use pull requests on GitHub - that way, we'll make sure they won't get lost.

For translations, please continue to use <a href="https://www.transifex.com/projects/p/quassel/">Transifex</a>.

And that's it, I think. Thank you all for your patience and continued support of Quassel, and have fun with the new release!

~ Sput
