---
title: "Software ecosystems: XXIIVV"
date: "2019-07-12"
publishDate: "2019-07-13"
author: CroQ
---

I'm fascinated every time I discover an ecosystem of apps and tools that is similar with what I'm trying to build here, with Trinkets.<br/>
I feel excited like I've encountered an ancient civilization from another dimension, hidden for 1 million years.

It took me a week to study most of the interesting repositories when I could find some spare time.<br/>
At first I was totally overwhelmed by the number of weird names (eg: Arvelie, Heol, Indental, Tablatal, Neralie, Oscean) and I thought "Maybe it's in Finnish, or maybe Volapük". Now I think it's in [Lietal](https://wiki.xxiivv.com/lietal) - an experimental synthetic language - I might be wrong.

All the tools below are documented on [wiki.XXIIVV.com](https://wiki.xxiivv.com):

- [Nataniev](https://wiki.xxiivv.com/nataniev) is a collection of free and open-source software following a singular design philosophy, and aesthetic
- [Oscean](https://wiki.xxiivv.com/oscean) is a fully static publishing platform created to work in the P2P space
- [Horaire](https://wiki.xxiivv.com/horaire) is a time-tracking tool
- [Hundred Rabbits](https://100r.co/pages/about.html) interesting tools, games, blog posts and knowledge sharing.

Everything was designed to be simple, without external libraries, easy to debug and repair.<br/>
Also, I believe they were built because the creators are digital nomads that have intermitent access to internet; they were created in isolation and must work offline.
Which is absolutely amazing!

There are other ecosystems that I was also made me enthusiastic in the past, a few come to mind:

* https://github.com/ipfs/ and the whole system around it;
* https://github.com/urbit/ decentralized operating system;
* https://github.com/choojs/ small browser tools written in Javascript;
* https://github.com/mafintosh/hypercore and the whole stack build on top of that: hypertrie, hyperdb, hyperdrive, etc.

... But XXIIVV is a little closer to what I'm building.

I'm not entirely sure why it's so fascinating, but I have a few ideas:

* it's an incredibly diverse set of utilities (tools for date and time, for storing and parsing data, a flow-based event emitter, tools for blogs, for decentralized chat; a text editor, drawing tools, music composition, a programming language and mobile games!)
* the code is usually very simple (the [Neralie code](https://github.com/XXIIVV/Oscean/blob/master/scripts/lib/neralie.js) is only 15 lines)
* I love the community that was build around it
* almost everything is free, open source and with a permissive software license
* I feel inspired and motivated and I'm thinking of ways to contribute, and intersect some my work with that ecosystem
* all the projects seem so familiar that I think if my life would have turned a different way 10 years ago, I might have reached similar conclusions that could have made me build the same kind of tools.


Follow the creators on Twitter: [<i class="fab fa-twitter"></i> Devine](https://twitter.com/neauoire) and [<i class="fab fa-twitter"></i> Rekka](https://twitter.com/RekkaBell)
and on Github: [<i class="fab fa-github"></i> Devine](https://github.com/neauoire) and [<i class="fab fa-github"></i> Rekka](https://github.com/rekkabell).

I'm writing this post mostly for myself. But also in the hope that this info might be useful for somebody interested in similar stuff.

-----

**Extra lessons learned for me:

If I'm publishing any open-source software and the license is permisive, it is assumed I'm publishing it for other people to use.
So if I care about the users, it's my duty to try and explain to the best of my abilities what that piece of software is doing.<br/>
It's not an easy task, but I have to do the work, if I want the users to have a smooth experience.

This doesn't apply if the software is private, or the license is very restrictive, because no-one else will ever use it anyway.

So how can I know what to add in the README of the software?

The first thing that comes into mind is to answer "**The 5 W**": who, what, where, when, why.<br/>
Not all of them will be relevant for all the projects, but it's a good starting point...

For the "What" question, I think at least the "What problem is this trying to solve?" should be answered.<br/>
Also the "What other similar software is out there?" is pretty useful, for people to position this one in a familiar context.

Inspiration from other places:

* [Perl documentation perlmodstyle](https://perldoc.perl.org/5.30.0/perlmodstyle.html) - there's a ton of perls in there
* [Richard Litt - Standard README style](https://github.com/RichardLitt/standard-readme)
* [Noffle - Art of README](https://github.com/noffle/art-of-readme)
