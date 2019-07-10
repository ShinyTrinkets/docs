---
title: "Elixir v1.9 🧪"
date: "2019-06-27"
author: CroQ
---

I was really really silent (publicly), for such a long time, wow...

I was quite busy actually, on all the projects. More details will follow.

What I wanted to write today is: WOOOW, [Elixir-lang](https://elixir-lang.org) implemented "build release" in their latest version !!

The official blog post: [Elixir v1-9-0 released](https://elixir-lang.org/blog/2019/06/24/elixir-v1-9-0-released/). TL;DR; from the article:

> Releases allow developers to precompile and package all of their code and the runtime into a single unit.<br/>
> A release is a self-contained directory that consists of your application code, all of its dependencies, plus the whole Erlang Virtual Machine (VM) and runtime.<br/>
> Code preloading, configuration and customisation, Self-contained, multiple releases, management scripts...

I made a small test with a basic "Hello world" app in Elixir 1.9. After that, I executed:<br/>
`$ MIX_ENV=prod mix release`

In the folder "_build/prod/rel/", the production app is only **8MB** !! 😱

I uninstalled Elixir and Erlang after compiling the app and I executed:<br/>
`$ _build/prod/rel/kv/bin/kv version` and some commands to run the "hello" function and it worked perfectly. That's why I'm so excited about it!

Because one of the most important reasons I stopped using [Elixir](https://elixir-lang.org) a few years ago, was that I couldn't find any way to export my app in a portable way, like they just implemented. And the smallest container with Elixir was a few hundred MB. Well, the second reason was the ecosystem was too small, so I had to write a lot of code just to make simple automation stuff, so I switched to Python.

Many things have happened since then... But I don't regret my decision, now that I'm using Go-lang.<br/>
Even if Go syntax is horrible and Elixir syntax is *for sure*, the most beautiful thing you could possible write, as a programmer. In my opinion.
