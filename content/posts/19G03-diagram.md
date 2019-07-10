---
title: "High level diagrams 🔩"
date: "2019-07-03"
author: CroQ
draft: true
---

Procrastination and delay are both forms of lazyness.
I'm fighting my own laziness daily.<br/>
Sometimes I actually win...

In one of my previous posts I promised to publish some diagrams of the Trinkets architecture.

What I care about at the highest level is the data flow. Inputs and Outputs.
All the implementation details are intentionally ignored, so Trinkets is just a "black box" that you can interact with.

A User can interact with Trinkets via command line, or via a browser user interface.
For every interaction, the User will see a log, an event and/or some data being generated as a response.

![Diagram 1](/images/posts/trinkets-diag1.svg)

Diagram 1 source:

```nomnoml
#spacing: 70
#edgeMargin: 6
#arrowSize: 0.4
#bendSize: 0.5
#.actor: visual=actor stroke=#33f

[<actor>User] input-> [CLI]
[User] -> [HTTP]
[CLI] -> [Trinkets⚙️]
[HTTP] -> [Trinkets⚙️]

[Trinkets⚙️] -> [logs]
[Trinkets⚙️] output-> [events]
[Trinkets⚙️] -> [data]
```

![Diagram 2](/images/posts/trinkets-diag2.svg)

Diagram 2 source:

```nomnoml
#spacing: 40
#edgeMargin: 5
#arrowSize: 0.5
#bendSize: 0.5
#.cmd: visual=roundrect fill=#c0ffee
#.actor: visual=actor stroke=#33f

[<frame>Overseer|
 [Overseer] --> [cmd#1]
 [Overseer] --> [cmd#2]
 [Overseer] --> [cmd#3]
]

[<actor>User] input-> [<sender>HTTP]
[<actor>User] -> [<sender>CLI]

[HTTP] -> [HTTP server]
[CLI] -> [<cmd>Command]

[Command] <- [Parser]
[Command] <- [Config]
[Command] -> [Overseer]
[Command] -> [HTTP server]
[Command] -> [State]

[Overseer] -> [State]
[State] --> [events]

[HTTP server] --> [logs]
[Overseer] --> [logs]
[Overseer] output--> [data]
```
