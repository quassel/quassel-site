---
tags:
- translations
title: Rosetta's Stone - Note for Translators
---
This is primarily a message for our current translators.

Daniel "al" Albers has finally managed to figure out a workflow how to correctly handle .po (gettext) files for translating Quassel (a non-trivial problem, since Qt stupidly insists in using its own format). Now that Quassel uses what the rest of the world uses, this also means that we now enable the use of standard tools for
translating.


It so happens that Quassel has now been <a href="https://translations.launchpad.net/ubuntu/lucid/+source/quassel/">imported into Rosetta</a>, Launchpad's (Ubuntu's) tool for managing translations. Which is cool, because in the two days it's been sitting there, we can already see a ton of new translated strings, plus it looks like we are getting heaps of new languages up to fun things like Colognian or Low German...

But this also means that there will be a change in our current way of handling translations. Until now, various cool people have been sending translations patches directly to us, maintaining a dozen of languages that way. In the future, this probably will have to happen via Launchpad. We are still figuring out a workflow how to get the Rosetta translations back upstream, but it certainly is our intention to do that, rather than letting Ubuntu maintain their own set of language packs.

<strong>If you helped with translating Quassel before, please wait with further work until we have put all the pieces together.</strong> We wouldn't want you to duplicate work, or do work that gets invalidated later. So far, your existing translations have been imported into Rosetta, so nothing got lost :) I will come up with a follow-up blog as soon as we have figured out how to handle translations in the future.

Let's answer a few Q&A:
<!--break-->

<em>Q: Why do you intend to switch over to manage translations by third-party tools/teams?</em>
A: While some languages are very well maintained, others have grown stale over time, as some contributors are busy or have found other interests. Also, while a dozen languages is quite impressive for an independent, rather small project like Quassel, there are many more languages in the world. Having experienced teams to handle that will certainly improve both the number and the quality of our translations.

<em>Q: I would like to continue helping you with translations!</em>
A: I am sure the Rosetta language teams will be happy to accept contributions. It is a community site that also seems to make it quite easy for individual translators to add strings without going through the hassle of getting a git checkout, sending patches etc.

<em>Q: Why did you choose Ubuntu's Launchpad, and not, say, KDE's teams for translating Quassel?</em>
A: First of all, we didn't "choose" this, it was offered to us and the import happened more or less automatically once we had proper gettext support going. Secondly, we do have quite good relations with Kubuntu downstream, and they helped us getting the localization stuff in shape in the past months. We also have synced our releases with Kubuntu releases for a while now, which certainly helps getting translations in time for final releases (due to a string freeze in place a few weeks before that). Lastly, getting Quassel to use KDE's infrastructure would've been a lot of effort. We're not hosted in their repositories and we don't use KDE's localization mechanisms (due to KDE support being optional). Supporting Rosetta, on the other hand, didn't require any upstream changes (so far) other than getting gettext working properly.

<em>Q: I used to translate Quassel, and now I feel alienated by your decision to switch to something else!</em>
A: Don't! We are very thankful for all the hard work you've done before, and none of your work has been lost as it all has been imported. You can also continue to contribute via Rosetta, if you'd like!

That's it for now!

~ Sput, feeling excited about getting a Quassel in Colognian
