
## 2019-July-02 (Tuesday) | ⭐️ ⒫＝⒫

I believe decentralized applications are very important and I'm not the only one to think that.<br/>
I've been watching the P2P and crypto space for years. For me personally, [decentralization technologies](https://github.com/croqaz/awesome-decentralized) =equal= freedom. Freedom to choose where you send your data and where you store it. Because if there are no "cloud" servers, you are in control.

I want to use P2P network protocols for the Trinkets suite, because there won't be any servers.<br/>
This is not the most natural, or the most confortable thing to do, but it's the only way that aligns to my vision.<br/>
This will be needed to allow the [Spinal 🌀](https://github.com/ShinyTrinkets/spinal) applications talk to each other, sync up, share logs, share data, or collaborate to finish tasks.

I started to watch some podcasts about decentralized technologies:
* IRL podcast [S4 Ep6: Decentralize It](https://irlpodcast.org/season4/episode6/)
* Changelog podcast [Ep 346: Off the grid social networking with Manyverse](https://changelog.com/podcast/346)
* Changelog podcast [Ep 42: Decentralizing the web with Beaker](https://changelog.com/jsparty/42)

I'm sure there are many others and I'll find them.

--------------------------------------------------------------------------------

## 2019-July-01 (Monday) | ⭐️ ⚙️

I believe the [Overseer](https://github.com/ShinyTrinkets/overseer) project is quite stable now, I put a lot of effort into making it better. I had to re-write a lot of the code, because when I started working at it, my Go-lang skills were horrible.
I created a lot of tests, the coverage is ~94% now. Of course, that doesn't mean there are no bugs, but at least it's a good measure of how well are the tests hitting the code.
Overseer is very important, because it's the core of dealing with other processes, so it needs to be rock solid.

The next step for [Overseer](https://github.com/ShinyTrinkets/overseer) will be to organise the code a little better.<br/>
I asked the creator of [go-Cmd](https://github.com/go-cmd) (a very important dependency for Overseer) to let me maintain his library and he agreed. This will force me to deal with real people, actually issues in this code and to learn how to maintain a code that is not written by me. But the most important is to give back to the community. I didn't have to do this, but I thought it's a nice thing to to, because go-Cmd has a lot of potential.<br/>
If I'll have enough features in go-Cmd to remove the Cmd struct and logic from the Overseer, that will make me very happy.

I also started thinking how to parse the infamous custom tags for [TwoFold (2✂︎f)](https://github.com/ShinyTrinkets/twofold.js). I don't think I'll be using [Nearley](https://nearley.js.org/), or any other JS library for parsing the tags. But... I never say never.

I started another project that I think might be a part of Trinkets: [text-DB](https://github.com/croqaz/text-db). This might be the Database I could use to save the events and/or the Data generated from the scripts running with [Spinal 🌀](https://github.com/ShinyTrinkets/spinal).<br/>
It will not be good enough for large scale data, but it should easily handle a few millions of records. I tested it with 4 millions and they are loaded in 60 seconds on my Macbook Air.<br/>
I don't worry too much. This can be optimised a lot. I just need to be flexible with the implementation.

I have a pretty good idea about the architecture of the Spinal app. I drew a few schemas. I feel a little lazy to convert them in digital format, because I know how hard it is to find a nice app to draw this kind of stuff... But I have to do this 😅

--------------------------------------------------------------------------------

## 2019-July-27 (Thursday) | ⭐️ 🧪

I was really silent (publicly), for such a long time, wow...

I was quite busy actually, on all the projects. More details will follow.

What I wanted to write is: WOOOW, [Elixir-lang](https://elixir-lang.org) implemented "build release" in their latest version !!

https://elixir-lang.org/blog/2019/06/24/elixir-v1-9-0-released/
> Releases allow developers to precompile and package all of their code and the runtime into a single unit.
> A release is a self-contained directory that consists of your application code, all of its dependencies, plus the whole Erlang Virtual Machine (VM) and runtime.
> Code preloading, configuration and customisation, Self-contained, multiple releases, management scripts...

I made a small test with a basic "Hello world" app in Elixir 1.9. After that, I executed:
> MIX_ENV=prod mix release

In the folder "_build/prod/rel/", the production app is only 8MB !! 😱

I uninstalled Elixir and Erlang after compiling the app and I executed "_build/prod/rel/kv/bin/kv version" and some commands to run the "hello" function and it worked perfectly. That's why I'm so excited about it!

Because one of the most important reasons I stopped using Elixir a few years ago, was that I couldn't find any way to export my app in a portable way, like they just implemented. And the smallest container with Elixir was a few hundred MB. Well, the second reason was the ecosystem was too small, so I had to write a lot of code just to make simple automation stuff, so I switched to Python.<br/>
But I don't regret my decision now that I'm using Go-lang.<br/>
Even if Go syntax is horrible and Elixir syntax is for sure, the most beautiful thing you could possible write, as a programmer. In my opinion.

--------------------------------------------------------------------------------

## 2018-November-22 (Thursday) | ⭐️ 🕸

I just started a new job at [ScrapingHub](https://scrapinghub.com) and I'm really excited about it.

But at the same time, this means I'll have to delay my work on these projects a little longer, until I get used to the new tools and projects.

--------------------------------------------------------------------------------

## 2018-October-07 (Sunday) | ⭐️ ⚙️

Not too much progress with [TwoFold (2✂︎f)](https://github.com/ShinyTrinkets/twofold.js).

I discovered [nearley.js](https://nearley.js.org/) and I think this will solve my parsing dilemma.

Unfortunately, I have to work on some personal things these weeks, so I don't think I'll make any progress this month 😢

--------------------------------------------------------------------------------

## 2018-September-27 (Thursday) | ⭐️ ⚙️

Wow man, where has this week gone ?! It's already Thursday...

I'm still working on [TwoFold (2✂︎f)](https://github.com/ShinyTrinkets/twofold.js) v0.2, because v0.1 is not that usable and friendly.

I added the option to define you own tag start and end characters to create fancy tags like `{{ whatever ? }}`, or double tags like `[[ whatever >]] ... [[< whatever ]]`.

I'm passing the parameters that could come from the tags, into the transformer functions. So that works, but I'm blocked at parsing those options from the template tags. So if I would have a tag like `{{ foo bar=true qaz=1 qwerty="yes please" }}`, I can't parse that so easily with a simple Regex ...

So I'm looking at a flexible enough XML / HTML parser. I checked [Parse5](https://github.com/inikulin/parse5) (used by [Reshape](https://github.com/reshape/reshape)), [HtmlParser2](https://github.com/fb55/htmlparser2) (used by [Cheerio](https://github.com/cheeriojs/cheerio)) and [HtmlJs-Parser](https://github.com/marko-js/htmljs-parser) (used by [Marko](https://github.com/marko-js/marko)). And [Snapdragon](https://github.com/here-be/snapdragon) (used by [Breakdance](https://github.com/breakdance/breakdance)). I kind of worked with all of them one way or the other, but not directly :smiley:

So I have to evaluate and decide if I'll use one of them, or something else, or implement my own thing.

--------------------------------------------------------------------------------

## 2018-September-22 (Saturday) | ⭐️ ⚙️

I just launched [TwoFold (2✂︎f)](https://github.com/ShinyTrinkets/twofold.js) v0.1 on NPM !! 🎉

**No. 1** reason I created TwoFold is ... to sort lines in my awesome lists :D And no. 2 is to fetch the Github or Gitlab status for those projects in the awesome lists. That's what I want to do ASAP, but I want it done properly so I'm taking the time.

I have huge hopes for this library, but there's so much to do... v0.1 is just a proof of concept. I intend to go up to a certain point and I'll wait for feedback from the people using it. If the people are not too excited, I'll focus my energy back to Spinal.<br />
If people are not too excited, it means I didn't explain it clear enough, or it's not that easy to use day by day, and that would make sense because not many people like command line tools. At least I'll learn something from that.

Anyway, for v0.2, I have to create a Changelog file and maybe a Roadmap file. And I'll direct people to this blog to read the history and the news.

I started 2/3 of my goals now: Spinal is work in progress, TwoFold is work in progress. I haven't started Zero-F yet, but I don't think I'll start it this year, there's too much on my plate already...

--------------------------------------------------------------------------------

## 2018-September-18 (Tuesday) | ⭐️ ⚙️

Let's start with the beggining: what's the focus of the **Trinkets** applications, when and where did this idea start and why this is still relevant today. I'll talk about the "how" another time.

In 2008, I was working in a data processing company and I noticed that I was repeatedly doing the same things every X intervals of time. Depending on the client, some tasks were daily, others weekly, others monthly. And with some exceptions, when humans weren't respecting the procedures, the flow was exactly the same: get the data as ZIP/RAR from somewhere, extract it, make some preparation of the data, run some commands that convert the data to invoices/letters, compress the result, generate some reports of the input and output numbers and upload the results somewhere, or send an e-mail.

I also noticed that when I was doing all this stuff manually, I was forgetting some details about that particular job, or I got interrupted and I was making mistakes. And after some time, this became incredibly boring and I was going crazy.

So I started first by automating the beggining of the process, and then, some parts from the end. And before I left the company, I had a really good automation flow, all written in Python.

But while I was doing all that, I wasn't focused on fixing just the little problems I had at work, I was thinking about a more general application. Something that I can use at home, something that my wife would use to convert her jewelry photos and automatically upload them on her website, or something to syncronize my different documents in different places, but even more general than that... I had no idea how to call this kind of application other than "automation stuff" and I had no idea how it would look like.

So I started taking notes and organizing ideas about all this project since then, and I called this "Project Triceratops".

Over the years, I did spend some time here and there on this project, but my focus was changing all the time and the general idea of the project was evolving.

* 2009 - First major attempt in Python + PyQt, using a nice drag & drop modular interface
* 2014 - Triceratops.rb - written in Ruby (pretty small experiment really)
* 2016 - Triceratops.js - before ES6 (pretty small and sad experiment)
* 2016 - Triceratops.ex - written in Elixir, probably the most elegant implementation
* 2016 - Triceratops/Trinkets.py - written in Python3.5, this was the most advanced version, the scripts were written in in Coconut

At the end of 2016 I renamed the project to "Trinkets".

* 2017 - Trinkets.js take 2 - using ES6, I spent a lot of time in this one, before I switched to Golang
* 2018 - TwoFold.cr - some experiments in Crystal lang (will be re-written to TwoFold.js)
* 2018 - Spinal.go - the current implementation

In 2018 I spent a lot of time thinking about the overall directions and I believe the vision of the project has matured.
Also, instead of 1 app, now there are 3 apps and some helper libraries.

1. most of the old idea of Triceratops/old Trinkets is now called [Spinal 🌀](https://github.com/ShinyTrinkets/spinal)
2. the template/ translation/ calculator is called [TwoFold (2✂︎f)](https://github.com/ShinyTrinkets/twofold.js)
3. the intelligence engine is called [Zero-f (0-f)](https://github.com/ShinyTrinkets/zero-f)
4. [Overseer-go](https://github.com/ShinyTrinkets/overseer) is a light process manager library

These applications and libraries working together should accomplish my vision. I hope you're prepared for this: I imagine Trinkets as a *distributed, self-healing, self-managing, self-hosted* alternative to *Siri + Google Now + Alexa*, combined with *IFTTT + Zapier + Automate.io + Integromat* ...

Sure, there are some challenges... 😄

If you'll look at the code, you'll quickly notice the current implementation is 1 million years far away from how I present it... There's a huge amount of work to make that happen...

For this to become reality the way I see it, I roughly estimate it will take me alone 10+ years to implement 😅 ...
Considering I'm already working full time, so I have like 1-3 hours spare time to work on this everyday.
And of course, I would have to find the time to work everyday.

I already have a huge private blog for the Trinkets projects suite, like I have for all the major projects I was ever part of. I made the first record in April 10, 2016.

Now that the project is matured, I created this public blog to open my ideas around Trinkets suite to the general audience.

Pheeew! I finally explained what's this all about! I want to start writing here more often, I'm writing a lot of ideas in private already.

--------------------------------------------------------------------------------

## 2018-August-15 (Wednesday) | ⭐️ ⚙️

Now is the time to explain the purpose of Trinkets and why it exists.

Some of the things are not yet crystal clear in my mind, so it might take some time to put them in writing and I might come back to edit this text in the future.

I'm using a Github repository and not a normal blog post, both because I'm lazy and because this is how I've worked for years, anyway. I kind of feel nervous when I post something in public, but writing to myself feels natural... maybe I'll repost this text on Medium, or whatever, when I consider it finished.

## What is Trinkets

"Shiny Trinkets" or "Trinkets" is the name of a Github organisation - a place to create free & open applications and libraries.

I've been writing open-source for 10 years now, but the Trinkets project has a unique history that I'll write about later.

I have taken a lot from the open-source community and this is my humble way of giving back.

Even if not the entire suite of applications is useful for someone, each application can be used separately and even more, parts of the apps can be hacked together to create new things, because the MIT license is very permissive.

These are the goals of this organisation:

## Constitution / Manifest / Philosophy

Our applications are created by humans and for humans. They are not created for machines; nor are they created for companies, whether they be in IT or marketing.

The focus of the applications is neither to empower their creators nor to turn a profit - the focus is for the applications to be really useful and easy to use.

We believe that the tools should be totally out of our way and because of that, the software we build has special limitations and requirements.

The first thing is that a piece of software should enable good practices in the user, in such a way that if the software is eliminated, the user can still use the good practices in his daily life and all the data created and used by the software is still usable by the user.

A user's data are solely their own and they must have absolute control over it. By default, all data are stored on user's devices and can be easily seen by the user in their entirety. The user may decide to store the data somewhere else (e.g. cloud storage). The user knows where that data are located and is free to change their own past data (e.g. they might want to enrich past events, or redact sensitive data).

The conclusion that comes from the previous ideas is that it's highly preferable to store the data in human-readable text files, than in a binary database, even with the risk of an acceptable performance loss.

A good compromise can be that the "the only source of truth" is still the readable text files, but a specialized converter translates the text into an efficient binary structure, from time to time and the application uses the optimized structure.

Our software must work offline just as normal as online, because we have no central servers that dictate the behaviour of our apps. But we understand that Cloud Services are important for specific use-cases so the user should be able to use them without limitation.

All the libraries and dependencies we use are carefully selected to be the best quality. And we try to keep them to a minimum.

We like to call these concepts "Ethical software". Don't treat your customers like products. Just like ethical eating, that doesn't treat animals like products.

We understand that this kind of software cannot satisfy everybody, but that's OK. Choice and diversity are important.

There are other people and applications that respect the same principles and we applaud them.

This line is extracted from *[jrnl](http://jrnl.sh/)* manifest:
> jrnl is a simple journal application for your command line. Journals are stored as human readable plain text files - you can put them into a Dropbox folder for instant syncing and you can be assured that your journal will still be readable in 2050, when all your fancy iPad journal applications will long be forgotten.

This paragraph is extracted from *[Urbit overview](https://urbit.org/posts/overview/)*.
> Can you remember all the services you have accounts for? How about the username and password for each? Some of them will let you pull your data out somehow, some won’t. Sometimes you can move your data between them, sometimes you can’t. But they're all good at showing you ads.

^ exactly that 👍

So, this ends my first public post about this. If you have any comments, ideas, please [create an issue](https://github.com/ShinyTrinkets/docs/issues), or let's talk on [Reddit/r/ShinyTrinkets](https://www.reddit.com/r/ShinyTrinkets) (it's pretty lonely down there but hey, let's make it crowded!).

> (U) [^_^] (U)<br/>

PS: I've written parts of these ideas and the constitution 2 months ago somewhere in my text documents, but I forgot about it. And a few days ago, I wrote the constitution again and then, I discovered the text from 2 months ago... I was shocked to discover it's exactly the same!! I used different words, but I said exactly the same things...

~Signed: CroQ

--------------------------------------------------------------------------------

## 2018-July-30 (Monday) | 🤖 ☀️

This is my first ever public post regarding the Trinkets projects! Wheee ⭐️ 🎉 !!

I'll take the time to explain what This Github Org is about, why I created it.

## Eof()
