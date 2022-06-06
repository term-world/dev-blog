+++
title = "How to Build a World that Doesn't Fall Apart"
date = "2022-06-01T11:36:51-04:00"
author = "Douglas Luman"
authorTwitter = "douglasjluman" #do not include @
cover = ""
tags = ["process", "progress"]
keywords = ["world", "building"]
description = ""
showFullContent = false
readingTime = true
hideComments = false
+++

When the core group behind this project began developing this idea, it came at a bit of an unforunate time -- February 2022. As fellow academic 
folk know, once the fall semester starts, it's pretty much a bullet train to May. The academic year exists as an express line; few stops, and 
it's pretty much a one-way subterranean affair.

But, now we _actually_ get to start. So what have we been up to?

Writing about the process of making a "world" happen isn't without it's clear implication in self-deification and call to all-consuming power. 
In many ways, we're setting about crafting a _reality_ more than anything, one that exists within _and_ parallel to the one we all commonly
accept. Here, I think of an address given by the author Philip K. Dick entitled "How to Build a Universe That Doesn't Fall Apart Two Days Later"
in which, prompted to define "reality" he claims that:

> It was always my hope, in writing novels and stories which asked the question “What is reality?”, to someday get an answer. This was the hope 
> of most of my readers, too. Years passed. I wrote over thirty novels and over a hundred stories, and still I could not figure out what was real.
> One day a girl college student in Canada asked me to define reality for her, for a paper she was writing for her philosophy class. 
> She wanted a one-sentence answer. I thought about it and finally said, “Reality is that which, when you stop believing in it, doesn’t go away.” 
> That’s all I could come up with. That was back in 1972. Since then I haven’t been able to define reality any more lucidly.
 
Of course, we don't have any pretention that we're creating something so immersive that students will get "lost" in it. While there are platforms
that probably could do this, the days of being completely lost in the "system" so typical of narratives like those found in Steven Levy's _Hackers_
are long-past. And, if we were set out to do this, I am sure we'd reflect on the recent cultural criticism of social media sites whose major goals
include on-platform retention. Addictiveness is not the name of the `term-world` game.

However, a great responsibility rests on us to create something stable and responsive -- even before we start developing curricular content. Meeting
with Mai a couple of days ago cemented this. I recalled the early incorporation of the Jupyter platform in class only a couple of years ago and the
intense system demand issues that caused the platform to be less-than-responsive. Bad student experience with a "world" constructs a barrier between
_this_ and _that_ dimension. So, our early efforts are meant to build a parallel reality that doesn't go away. Then, we can build the immersive
engagement that we want through `term-world`.

This proposes another frustrating "hurry up and wait" feeling. However, thanks to having 4 folks staffed to the project, we can start a couple
of things in parallel.

## `term-hub`

First up in our summary of work is `term-hub`, a software that will allow us to create a shared experience for all students in the course.

### History

The Allegheny CS department has, since its release, adopted [VS Code](https://code.visualstudio.com/) as the default editor of choice. Surprisingly, 
this was less of a top-down than bottom-up solution; students were already using it, and our department credo to meet the students where they are 
actually at seemed to make the conclusion to move to the platform a natural one. Even beyond its status as "free" software, it's a generously-featured
program for coding.

(Here, I -- the professor -- must stand up to defend `nano` and `Notepad++` as my editors of choice; though it's more a mark of my status as a
computational "old head" than anything else).

The clear implication that COVID-19 would force schools to conduct their work remotely posed challenges for every discipline -- especially for folks
teaching introductory courses that rely a great deal on setting good abstract habits before necessarily addressing technical environments. In order to
give both students, my teaching assistants (TLs), and I a uniform experience, I adopted a somewhat hotwired implementation of JupyterHub to to begin
the evolution of the course toward a shared, community experience.

But, this was a trade-off. I wanted to use [Coder's "code-server"](https://github.com/coder/code-serverhttps://github.com/coder/code-server) for the reason
that opened this section (it's essentially, as billed, "VS Code in the browser"). Given the pull toward curricular uniformity, it'd be a win to introduce
the platform as a form of computational "first contact." Of course, however, there was a bit of a problem.

### The problem

By default, `code-server` really only caters to one user at a time -- at least in its freely-available version. (Coder, the company that develops the 
solution has a hosted service, though it's really meant for enterprise applications which -- of course -- means enterprise dollars.) I _could_ give
each student their own "virtual machine" (think: personal computer in the "cloud), but that seemed hard to manage and to demand _a lot_ of resources.

After a good run with Jupyter, I thought I might take the space and support to address the issue of making `code-server` _multi-tenant_. This approach
means that _all_ of the students in the class should have their own editors _and_ a constant connection to our community resource -- the shared world.

### The present

This is where we feature our work on the `term-hub` project. Our novel solution is based on one developed a couple of years ago by a developer named
Rafael Ketsetsides ([@rafket](https://github.com/rafket)), called [vscode-hub](https://github.com/rafket/vscode-hub), relying on a series of software packages including the virtual "containerization" platform
[Docker](https://docker.io), `code-server`, and a few other small programs to make sure the _right_ folks are logging in.

This work is captured in our [repository for the term-hub project](https://github.com/term-world/term-hubhttps://github.com/term-world/term-hub), an elaboration
on `@rafket`'s original work to make each students "world in a world" available from anywhere in the world at any time with real-time "logging" (i.e. recording
what's going on, good and bad) and management (i.e. "God mode" for course administrators).

Here, we're writing our own software to manage a _very_ complex process. And that demands, as this post asserts, that our world doesn't fall apart so easily.
This requires rigorous security so that only students in the course can "get in"; testing to be sure that we're not surprised on a regular basis by critical
errors; and finally starting to work in the environment on our own consistently -- using our own platform to further develop the platform.

We're all responsible for various levels of this infrastructure. If you follow along in our posts and repositories, you'll likely see a few of the same
names concentrate their time on this particular project -- at least very early on. The tl;dr here: if we can't get this to work, we've got a few
larger challenges to address via shared space.

## Curricular content

At the same time that we're developing the infrastructure supporting interaction with the world, the real "software" here is the curriculum itself -- the
lessons that, with the right access assumed, make the community go from possibility to reality. 

Prior engagements with developing the course work never felt quite "right" before we arrived at what we're calling the class' "persistent metaphor." With
somewhat equal weight, we have a significant responsibility to make the layer that students interact with to be as rigorously tested and tried as the 
technical solutions "running" it. If education is at all comparable to being a "software of the mind," our programming here has to be careful.

In the previous post, Jeff outlined his engagement with the course and, being a student so recently engaged in both taking and assisting in the course, he's
done a large amount of the work of documenting the outcomes from various conversations about what students will actually _do_ in the course. Moreso than
anyone else involved in the project, Jeff worked consistently on the project as the semester wore on. From week to week, it was common for him to check in
with his progress and ask for feedback on this next iteration.

Perhaps above the technical allure, the outlines of the pedagogical ("teaching") part of the work really made this project a candidate for the opportunity we 
have through the school to work on our quasi-reality with reasonable support.

As we make the platform workable, Jeff is largely dedicated to expanding and building the practical side of the course. Like everything else with this project, 
it's also visible via our [world-building wiki](https://github.com/term-world/world-building/wiki).

There are really two tricky bits here: ensuring correct "scaffolding" (that lessons build on one another in a reasonably well-paced way) and understanding what
further technical support we have to build, including an in-world economy, self-hosted infrastructure (i.e. power, a postal service, et al.), and governance. As
we hope to prove witht his class, these are as much problems of "meatspace" as they are of a digital world. Design and implementation concerning these layers
are answerable to the students we have yet to teach.

If history is any guide, that's a tough crowd.

## A benediction, of sorts

We're at the point of disembarkation, the release of our time and talents on what is the most massive project we could have proposed with even a shade of
possibility. Though I feel like we stand on the edge of something, I wonder what kind of edge it is. One thing I'm certain of, though, is that its slope is
decidedly downward at a steep grade. All we have to spend here is time, and it's already going by incredibly fast. Recounting how I feel about this project:
we're building the proverbial pirate ship as it sails, maintaining some illusion fo relative stability.

Returning to Philip Dick for a bit of unsettling (as it's always good to remain a bit tentative):

> However, I will reveal a secret to you: I like to build universes which do fall apart. I like to see them come unglued, and I like to see how the characters 
> in the novels cope with this problem. I have a secret love of chaos. There should be more of it. Do not believe — and I am dead serious when I say this — do 
> not assume that order and stability are always good, in a society or in a universe.

While I don't _like_ the idea of my technical universe falling apart, I _do_ like remaining just on the edge of it.
