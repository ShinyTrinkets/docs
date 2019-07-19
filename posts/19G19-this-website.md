---
title: "How this website is built"
icon: <i class="fas fa-globe"></i>
date: "2019-07-19"
tags: ["website", "internet"]
author: CroQ
draft: true
---

A week ago I published all the old blog posts (not that many) on this website.

Before that, they were only available in the [github.com/ShinyTrinkets/docs](https://github.com/ShinyTrinkets/docs/) repository.<br/>
The repository is still there and you can see the history of all the changes.

Initially I just wanted to (eventually) publish some documentation, specs, ideas about the project, but I decided to focus more of the "blog posts".

### Technical details about the website

The website is powered by the [Hugo](https://gohugo.io/) site generator. Its role is to convert the Markdown files that I'm using to write these posts, inject them in some HTML templates and generate a ton of HTML.

The website source code available in the [github.com/ShinyTrinkets/shinyTrinkets](https://github.com/ShinyTrinkets/shinyTrinkets/) repository.

💡IDEA :: *I think I should rename the repositories, to represent more of what they actually do*...

I use 2 branches to organize the source templates and the actual generated HTML. The `master` branch contains the source and the `gh-pages` contain the HTML. This is due to a "feature"? or "limitation"? of Github.<br/>
But I can't complain. The hosting is free, so thank you [<i class="fab fa-github"></i> Github](https://github.com/)!

The current theme is a fork of [Charaka theme](https://github.com/natarajmb/charaka-hugo-theme). I liked the initial look & feel, but my code is now pretty different and I'll change it even more.

I'm pretty happy with the stack so far. I used Jekyll in the past, but Hugo seems to be a little more flexible. Plus I like that I don't have to update the Ruby dependencies that Jekyll uses, because Hugo is just a single executable.

### TODOs

There's still a ton of things to do to make this website nicer.

* find a nice and readable font for the posts. I think the current one is not that readable (I think it's "Domine")
* .....
* .....
