---
title: "TwoFold WIP ✂︎"
date: "2018-09-29"
author: CroQ
---

Wow man, where has this week gone ?! It's already Thursday...

I'm still working on [TwoFold (2✂︎f)](https://github.com/ShinyTrinkets/twofold.js) v0.2, because v0.1 is not that usable and friendly...

I added the option to define you own tag start and end characters to create fancy tags like `{{ whatever ? }}`, or double tags like `[[ whatever >]] ... [[< whatever ]]`.

I'm passing the parameters that could come from the tags, into the transformer functions. So that works, but I'm blocked at parsing those options from the template tags. So if I would have a tag like `{{ foo bar=true qaz=1 qwerty="yes please" }}`, I can't parse that so easily with a simple Regex ...

So I'm looking at a flexible enough XML / HTML parser. I checked [Parse5](https://github.com/inikulin/parse5) (used by [Reshape](https://github.com/reshape/reshape)), [HtmlParser2](https://github.com/fb55/htmlparser2) (used by [Cheerio](https://github.com/cheeriojs/cheerio)) and [HtmlJs-Parser](https://github.com/marko-js/htmljs-parser) (used by [Marko](https://github.com/marko-js/marko)). And [Snapdragon](https://github.com/here-be/snapdragon) (used by [Breakdance](https://github.com/breakdance/breakdance)). I kind of worked with all of them one way or the other, but not directly 😁

So I have to evaluate and decide if I'll use one of them, or something else, or implement my own thing.
