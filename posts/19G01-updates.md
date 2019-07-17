---
title: "Start of July 2019 updates ⚙️"
date: "2019-07-01"
author: CroQ
---

I believe the [Overseer](https://github.com/ShinyTrinkets/overseer) project is quite stable now, I put a lot of effort into making it better. I had to re-write a lot of the code, because when I started working at it, my Go-lang skills were horrible.<br/>
I created a lot of tests, the coverage is [~94%](https://codecov.io/gh/ShinyTrinkets/overseer) now. Of course, that doesn't mean there are no bugs, but at least it's a good measure of how well the tests are hitting the code.<br/>
Overseer is very important, because it's the core of dealing with other processes, so it needs to be rock solid.

The next step for [Overseer](https://github.com/ShinyTrinkets/overseer) will be to organise the code a little better.<br/>
I asked the creator of [go-Cmd](https://github.com/go-cmd) (a very important dependency for Overseer) to let me maintain his library and he agreed. This will force me to deal with real people, actual issues in this code and to learn how to maintain a code that is not written by me.<br/>
But the most important is to give back to the community. I didn't have to do this, but I thought it's a nice thing to to and go-Cmd has a lot of potential.<br/>
If I'll have enough features in go-Cmd to remove the Cmd struct and logic from the Overseer, that will make me very happy.<br/>
If not, I'll just keep my own version of go-Cmd and I'll be happy anyway.

I also started thinking how to parse the infamous custom tags for [TwoFold (2✂︎f)](https://github.com/ShinyTrinkets/twofold.js). I don't think I'll be using [Nearley](https://nearley.js.org/), or any other JS library for parsing the tags. But... I never say never.

I also started another project that I think might be a part of Trinkets: [text-DB](https://github.com/croqaz/text-db). This might be the Database I could use to save the events and/or the Data generated from the scripts running with [Spinal 🌀](https://github.com/ShinyTrinkets/spinal).<br/>
It will not be good enough for large scale data, but it should easily handle a few millions of records. I tested it with 4 millions and they are loaded in 60 seconds on my Macbook Air.<br/>
I don't worry too much. This can be optimised by a lot. I just need to be flexible with the implementation.

I have a pretty good idea about the architecture of the Spinal app. I drew a few schemas. I feel a little lazy to convert them in digital format, because I know how hard it is to find a nice app to draw this kind of stuff... But I have to do this eventually 😅
