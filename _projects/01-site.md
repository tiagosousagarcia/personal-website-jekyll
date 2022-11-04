---
title: This Site
blurb: A static personal website, written from scratch in HTML and CSS.
layout: page
---

It's been a long time since I created a website from scratch. The year was (probably) 1999, [tables and frames were all the rage](https://thehistoryoftheweb.com/tables-layout-absurd/), and I was 11 with a passion for garish clipart and comic sans. Luckily for everyone, I didn't actually have an internet connection at the time: my first and, until now, only custom-build page was a local affair.

Then the early 2000s came, the social web revolution, [myspace](https://en.wikipedia.org/wiki/Myspace), blogs, wordpress: I didn't need to write any HTML, and I learned CSS only by trying to make simple tweaks on the free templates of early blogging services (first with blogspot, later with a custom install of wordpress). Again, luckily, all those things are lost to the ether (or, at least, very hard to find).

So, in mid-2021, why would I want to go back to the ides of 1999? Surely it would be easier to just use any of the myriad CMS available?

Well, yes and no.

I've had this domain since 2018. All that time, I had an instantiation of wordpress, a title page, and a couple of headings. No content other than the stereotypical Lorem Ipsum. CMs are lazy. I am lazy. The result was a boring, ugly, dead page that still showed up when people googled my name.

A few weeks ago I also decided it was time to brush up on my coding skills: I have kept them up haphazardly, on a "learn-only-what-you-need-to-know" basis, which has been great for breadth of knowledge, but less brilliant on actually getting anything done. I've signed up for [freeCodeCamp](https://www.freecodecamp.org/) in which the first block of lessons was on web development. The last test in that block was to build a personal portfolio. I phoned it in for the test, doing only the bare minimum, but decided it was time to do it for real. That was the moment when this version of [tiagosousagarcia.co.uk]() was born.

## Concept

The concept for this site was relatively simple: it is mostly modelled on typical academic pages (with sections on [research interests]({{site.baseurl}}#Research), [publications]({{site.baseurl}}#Publications)), mixed with a [professional portfolio]({{site.baseurl}}#Projects) borrowed from the personal spaces of frontend devs, and a chunky section dedicated to my [photography]({{ site.baseurl }}{% link portfolio.md %}). I wanted the site to be static, partly for longevity reasons (in the spirit of [endings compliance](https://endings.uvic.ca/compliance.html), though this site is not fully compliant yet), partly to keep it light and quick(ish), mostly to allow me to dive deep into all aspects of its creation. For the most part, I wanted a single-page site, with more detailed information on projects and the photography portfolio relegated to their own single-page minisite.

Migrating from the world of digital textual editing and the [Text Encoding Initiative](https://tei-c.org/) (itself an XML based language), I knew I wanted to keep my HTML as semantic as possible. The base HTML should make perfect sense in itself (at least that's the hope): the `<main>` content of the website is divided into `<section>`s, each of which might have one or more `<article>`s, each with potential for further nested `<section>`s and `<article>`s. A specialist in semantic HTML might balk at my liberal interpretation of the standard, but for a textual editor this structure should make sense: each top-level `<section>` akin to a chapter, each second-level `<section>` a subsection of that chapter. The result is that, with the exception of the photography portfolio which is mostly a visual medium, there is no meaningless `<div>` anywhere to be seen in the code. Whether that is a good or a bad thing is another story.

## Design

Having settled on a one page structure (for the most part), then came the hardest bit: the design of the page. I knew, from the start, a few things that I wanted for the basic page:

* A strong but minimalistic, full page header;
* Simple, nearly monochromatic, colour-scheme;
* A fixed navigation bar.

All of these were imminently doable, but things got more complicated when my ultimate goal of **responsiveness** came into play: I had never designed anything responsive in my life -- that was one of the joys of using CMS in the past. That's when I started to learn about `flexbox` and the joys (and pains) of mobile-first design. That experience came too late for the bulk of the main page -- which is now a rather messy affair in desperate need of a re-write -- but proved invaluable when I tackled the design of the photography portfolio for the second time.

The (nearly) monochromatic colour-scheme is indebted to my photography as well: I shoot mostly film, mostly in black and white, so it seemed reasonable that my site would follow the same visual language. There are only two accent colours to break the monotony: the <span class="blue-highlight">blue of the headings</span> and <span class="red-highlight">the red of the graphical flourishes</span> -- everything else appears in shades of white or black.

Typography was kept as simple as possible (some might call it boring). As the vast majority of the web, this site makes use of [Google Fonts](https://fonts.google.com/), specifically three sans-serif font families: <span class="raleway-highlight">page titles are in Raleway</span>, <span class="montserrat-highlight">headings, navigation menu, and other higher-level textual elements are in Montserrat</span>, and everything else uses 'Poppins.' The differences between each are minimal, but that's the point.

## Designing the photography portfolio
![wireframe]({{site.baseurl}}assets/img/project_background_site.jpg)
<span class="image-legend">Handrawn wireframe for the photography portfolio</span>

At the risk of sounding immodest, I am very proud of the design of the [photography portfolio]({{ site.baseurl }}{% link portfolio.md %}). I had one of those rare moments of inspiration one night when I couldn't sleep. Its concept is quite simple: it borrows the language of a photography book. With widescreens (or basically, anything larger than a smartphone), each viewport is a page-opening, with each photograph occupying roughly half the screen, and as tall as possible without affecting its native ratio. On a desktop, I wanted each scroll motion to be like a page-turn. The challenging bit was, again, to make this vision mobile-friendly: I knew *how* I wanted the design to transfer to a smaller screen (a straight column, with each screen having the full image and the accompanying text), but I had no idea how to *do it*.

The first draft of the portfolio was a nightmare to transfer to a mobile site: nothing worked, my carefully considered layout kept breaking at different, and apparently random, points. I scrapped the whole thing and started again, using `flexbox` for everything, and eschewing the problematic mandatory scroll points.

The final result is not perfect, but it is faithful to my initial idea, with only a handful of concessions.

## Final thoughts

Would I do this whole thing again?

Yes, I would. Designing this website has been fun, challenging, and rewarding. There was a time in which I might have given up at the first hurdle, but I am much more knowledgeable now than I was when I did this sort of thing for a living. I had too much fun figuring out how to create animated cards (as you can probably see from the main page), and am way too proud about how the photography portfolio looks. It might not be perfect, but it is a good-looking place. I made a point of using only my own photography to illustrate it, and whenever that wasn't possible, I created simple graphics to illustrate certain sections.

Everything in this website (with the exception of the photographs themselves) is free to reuse, offered under a [CC-By license](https://creativecommons.org/licenses/by/4.0/) -- though I doubt anyone would find any particular use for my rough CSS. The photos are under copyright but if you see anything you like (here or on my [instagram](https://www.instagram.com/tiagosousagarcia/)) get in touch, I'm sure we can sort something out.

Not that it matters at all, but in case you are curious, the entire website was developed using [Atom](https://atom.io/), and only too late in its development have I discovered the magic of [Emmet](https://docs.emmet.io/).