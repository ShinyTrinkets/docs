---
title: "High level diagrams"
icon: <i class="fas fa-project-diagram"></i>
date: "2019-07-03"
publishDate: "2019-07-10"
tags: ["spinal"]
author: CroQ
---

Procrastination and delay are both forms of lazyness.
I'm fighting my own laziness daily.<br/>
Sometimes I actually win...

In one of my previous posts, I promised to publish some diagrams of the Trinkets architecture.

What I care about at the highest level is the data flow. Inputs and Outputs.
All the implementation details are intentionally ignored, so Trinkets is just a "black box" that you can interact with.

A User can interact with Trinkets via command line, or via a browser user interface.
For every interaction, the User will see a log, an event and/or some data being generated as a response.<br/>


![Diagram 1](/images/posts/trinkets-diag1.svg)

{{< collapse >}}
View diagram 1 source
{{< /collapse >}}


{{< collapsible >}}
{{< highlight nomnoml >}}
#spacing: 70
#edgeMargin: 6
#arrowSize: 0.4
#.actor: visual=actor stroke=#33f

[<actor>User] input-> [CLI]
[User] -> [HTTP]
[CLI] -> [Trinkets⚙️]
[HTTP] -> [Trinkets⚙️]

[Trinkets⚙️] -> [logs]
[Trinkets⚙️] output-> [events]
[Trinkets⚙️] -> [data]
{{< /highlight >}}
{{< /collapse >}}


![Diagram 2](/images/posts/trinkets-diag2.svg)<br/>

{{< collapse >}}
View diagram 2 source
{{< /collapse >}}


{{< collapsible >}}
{{< highlight nomnoml >}}
#spacing: 40
#edgeMargin: 5
#arrowSize: 0.5
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
{{< /highlight >}}
{{< /collapse >}}
<br/>

And this is the list of the components and their role:

* Command (manager, glue) - used by cmd line at startup to register all the scripts;
  its role is to join together some of the other components like Overseer with the State and the RPC with the State
* Config (r&w) - reads and writes global configs (JSON and YAML)
* Parser - used by the Manager to parse files and folders and send the procs to the Overseer
* Overseer (process manager) - used by the Manager and the HTTP server to control processes
* Events (flux) - syns things happening within the system to the state, and glue events together
* State (tree) - a view of the source files, procs and sub-procs for the user to see as raw JSON, or maybe in a GUI
* HTTP server - for the user to read the state and to remote control procs (stop, start)
* Database (data) - used for saving stats about source files, procs, sub-procs, also for storing vars and logs?
