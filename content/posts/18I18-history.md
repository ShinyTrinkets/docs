---
title: "The history of Trinkets ⭐️ ⚙️"
date: "2018-09-18"
author: CroQ
---

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
