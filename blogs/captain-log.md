
## 2018-September-18 (Tuesday) | ⭐️ ⚙️

Let's start with the beggining: what's the focus of the **Trinkets** applicatins, when and where did this idea start and why this is still relevant today. I'll talk about the "how" another time.

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

At the end of 2016 I renamed the project to Trinkets.

* 2017 - Trinkets.js take 2 - using ES6, I spent a lot of time in this one, before I switched to Golang
* 2018 - TwoFold.cr - some experiments in Crystal lang (will be re-written to TwoFold.js)
* 2018 - Spinal.go - the current implementation

In 2018 I spent a lot of time thinking about the overall directions and I believe the vision of the project has matured.
Also, instead of 1 app, now there are 3 apps and some helper libraries.

1. most of the old idea of Triceratops/Trinkets is now called [Spinal 🌀](https://github.com/ShinyTrinkets/spinal)
2. the template/ translation/ calculator is called [TwoFold (2✂︎f)](https://github.com/ShinyTrinkets/twofold.js)
3. the intelligence engine is called [Zero-f (0-f)](https://github.com/ShinyTrinkets/zero-f)
4. [Overseer.go](https://github.com/ShinyTrinkets/overseer.go) is a light process manager library

These applications and libraries working together should accomplish my vision. I hope you're prepared for this: I imagine Trinkets as a *distributed, self-healing, self-managing, self-hosted* alternative to *Siri + Google Now + Alexa*, combined with *IFTTT + Zapier + Automate.io + Integromat* ...

Sure, there are some challenges... 😄

If you'll look at the code, you'll quickly notice the current implementation is 1 million years far away from how I present it... There's a huge amount of work to make that happen...

For this to become reality the way I see it, I roughly estimate it will take me alone 10+ years to implement 😅 ...
Considering I'm already working full time, so I have like 1-3 hours spare time to work on this everyday.
And of course, I would have to find the time to work everyday.

I already have a private blog for the Trinkets projects suite, like I have for all the major projects I was ever part of. I made the first record in April 10, 2016.

Now that the project is matured, I created this public blog to open my ideas around Trinkets suite to the general audience.

Pheeew! I finally explained what's this all about! I want to start writing here more often, I'm writing a lot of ideas in private alredy.

--------------------------------------------------------------------------------

## 2018-August-15 (Wednesday) | ⭐️ ⚙️

Now is the time to explain what's the purpose of Trinkets and why it exists.

Some of the things are not yet crystal clear in my mind, so it might take some time to put them in writing and I might come back to edit this text in the future.

I'm using a Github repository and not a normal blog post, both because I'm lazy and also because this is how I worked for years anyway. I kind of feel nervous when I post a public post, but writing to myself feels natural... Maybe I'll repost this text on Medium, or whatever, when I consider it finished.

## What is Trinkets

"Shiny Trinkets" or "Trinkets" is the name of a Github organization and is a place to create free & open applications and libraries.
I'm writing open source for 10 years now, but the Trinkets project has a unique history, that I'll write about later.

I have taken a lot from the open-source community, so this is my humble way of giving back.

Even if not the entire suite of applications is useful for someone, each application can be used separately and even more, parts of the apps can be hacked together to create new things, because the MIT license is very permissive.

So these are the goals of this organization:

## Constitution / Manifest / Philosophy

Our applications are created by humans and for humans. They are not created for machines. And not for IT companies, or for marketing companies.
The focus of the applications is not to make the creators of the apps empowered, or to make a huge profit. The focus is for the applications to be really useful and easy to use.

We believe that the tools should be totally out of our way and because of that, the software we build has special limitations and requirements.
The first thing is that a piece of software should enable good practices in the user, in such a way that if the software is eliminated, the user can still use the good practices in his daily life and all the data created and used by the software is still usable by the user.

User's data is **solely his own** and he must have absolute control over it.
By default, all data is stored on user's devices and can be easily seen by the user in its entirety.
The user might decide to store the data somewhere else (eg: cloud storage).
The user should know where that data is located and is free to change his own past data (eg: he might want to enrich past events, or redact sensitive data).

The conclusion that comes from the previous ideas is that it's highly preferable to store the data in human readable text files, than in a binary database, even with the risk of an acceptable performance loss.
A good compromise can be that the "the only source of truth" are still the readable text files, but a specialized converter translates the text into an efficient binary structure, from time to time and the application uses the optimized structure.

Our software must work offline just as normal as online, because we have no central servers that dictate the behaviour of our apps. But we understand that Cloud Services are important for specific usecases so the user should be able to use them without limitation.

All the libraries and dependencies we use are carefully selected to be the best quality. And we try to keep them to a minimum.

We like to call these concepts "Ethical software". Don't treat your customers like products. Just like ethical eating, that doesn't treat animals like products.

We understand that this kind of software cannot satisfy everybody, but that's OK. In the same way being straight is not for everybody. Or eating vegetarian food doesn't satisfy everybody's tastes. Choice and diversity are important.

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
