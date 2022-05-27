+++
title = "Blueprint for A World"
date = "2022-05-27T12:44:34-04:00"
author = "Jeff Normile"
authorTwitter = "" #do not include @
cover = ""
tags = ["", ""]
keywords = ["", ""]
description = "Here we explore a student's perspective on the origins of `term-world`, and the experiences that have contributed to his understanding of what the project represents and aims to accomplish."
showFullContent = false
readingTime = true
hideComments = false
+++

## Luman's `mansion`

Of the student collaborators involved with the `term-world` project, I'm the one that has most recently been exposed to Professor Doug Luman's Computational Expression course (CMPSC 100). I took it as an incoming Allegheny student in the fall of 2021, and the course was my first formal exposure to computer programming.

One of the first activities we took on as a class was focused on teaching the basics of file navigation, using a terminal to get from one directory to another (if you're unfamiliar, think of opening up a file in your computer's file explorer, double-clicking into one folder and then another to locate the exact file you're looking for). This easily could've been nothing more than a cut-and-dry explanation of a few different terminal commands, and I don't think anyone would have faulted our instructor for demoing the commands in a terminal window and then moving on, ultimately leaving it up to us (the students) to get a firmer handle on the actual *use* of these commands by practicing them firsthand over the course of the semester.

*Instead*, what we got was this:

```
***********       <DRACULA VOICE>      ************
*********** YOU'VE ENTERED THE MANSION ************
***********     THE SPOOKY MANSION     ************
```

Our terminals had transformed before our very eyes! This wasn't just some window to enter commands in, like we had been told--no, this was the `mansion`. A tree of file folders had been constructed to represent the floorplan of a mansion (er, a *spooky* mansion) and it was our task to use the few navigational commands that had just been given to us to locate a treasure in the depths of the `mansion`. Each folder--or room--had been outfitted with a single line of descriptive text (upon entering the `coatroom` you would be told that it was `Just a room for coats. A coat room.`) and a selection of options for rooms that could be navigated into from your new position in the `mansion`.

Beyond this, the `mansion` had been outfitted with secret passages that had to be actively sought for, and there was the promise of a secret password that would take you to an optional prize, one that was even *better* than the treasure that was our primary goal.

The classroom lit up that afternoon. Students were excitedly chattering with each other about the secrets they had unearthed, some were stuck after taking a one-way secret passage and needed the assistance of their peers to figure out how to clamber out of their predicament. There was an unspoken sense of competition between those looking for the password, hushed whispers to the instructor indicating they had found the prize--the extra special super hidden one, that is.

From that very first introductory activity, I was *hooked*.

## Stepping Outside the `mansion`...

I was fixated with the presentation of the course--a series of games--as much as I was fixated with its subject matter. I've grown up *very* much in the realm of video games, and am intimately familiar with the feelings of exploration and achievement that they invariably provide, as well as the opportunities for collaboration and competition they frequently foster. Luman's mansion was the first of many activities that gave students a chance to meaningfully engage with course content in a way that was as playful as it was instructive. Of the CS courses I've taken at this point, CMPSC 100 is the one that has kept me the most engaged as a student, in spite of the learning objectives being somewhat less interesting than the more specialized subject matter presented in higher-level courses.

Luman has told me on more than one occasion that his role in Allegheny's Department of Computer Science is that of "hype man"--he endeavors to get students *excited* about computer science to drive up major/minor enrollment, and his approach to curriculum is one of the most obvious manifestations of that role. He's also told me on as many occasions that he's rarely ever fully satisfied with his efforts in this regard: case in point, over the course of CMPSC 100 he was constantly crowdsourcing feedback on the latest activity--was it instructive, did you see the connection to the latest learning objective, was it *enjoyable*? It was clear that he was responding to this feedback in the moment, occasionally pivoting the direction of a week's planned content in the middle of said week. It seemed as though the class was as instructive to him as it was to us, as he continued to pursue iterations of CMPSC that were more exciting, more engaging, and hopefully more educationally useful than the last.

Inasmuch as I was obsessed with his approach to CMPSC 100, I became obsessed with the *experiment* that the entire class was. I often found myself in conversations with him regarding the reasons he did this or that in class as well as what he would do differently next time, and it wasn't long before I knew I just *had* to see how this course continued to evolve, ultimately volunteering my services (or perhaps more accurately, persistently requesting my services be accepted) as a student Technical Leader (TL) for the winter section of CMPSC 100.

During this winter section I already saw some evolutions from the CMPSC 100 that I had experienced just the semester prior. The games contained in the course were always metaphors for computing principles, but they had previously been separate, distinct metaphors. There was no through-line that carried students from one lesson to the next, apart from the skills they had picked up along the way. This time there was *some* persistence as multiple lessons dealt with manipulating virtual playing cards.

The other student collaborators now involved with `term-world` were all TL's for this particular section of the course as well, and many of our conversations after class dealt with the rather abstract pursuit of a persistent metaphor--a single continuous experience--that could be used as the platform to deliver learning objectives, rather than a series of isolated, distinct platforms that students had to mentally leap to and from themselves.

Near the end of the course, I received the following message from Luman: "Imagine `mansion`, but with a town that students have to build and add on to."

That night I went back to the `mansion` activity, and I started to imagine. I imagined that each room of the `mansion` was a broader space, say a `house` or a `field` or a `library`, and that each of those spaces had been filled with things to interact with, tasks to complete, or half-built objects to finish building. The entire thing would be a `town` filled with space for students to explore, achieve, build, collaborate, and compete.

I was eager to hear more about this vision, and after the next class I found myself in a conversation with Danny and Luman, asking dozens of questions about the `town`. I was amazed by the ideas I was presented with--in my own conception of the `town` it was little more than a virtual space littered with things to do; but those guys, they were talking about forms of governance, economy, power grids, weather, the works! I couldn't imagine how it all could be implemented, how such a thing could take form in a terminal window.

It was clear that this was more than just a `town`--the idea encompassed so much more than that word represented.

Thus `term-world` was born.

## ...And Into the `world`

I was more than a little skeptical of the lofty ambitions being thrown around during that first unofficial meeting for the `term-world` project. But I was curious, and at this point more than a little invested in the way that Luman was tackling the task of teaching CMPSC 100--I *had* to be involved with this, even if I didn't understand how it could possibly work.

There was talk about immediately jumping in and just starting to build things, to see what would and wouldn't work. It was clear that the work being discussed was still a bit beyond my technical capabilities (having only one semester under my belt) but like I already said, I just *had* to be involved in some capacity, so I offered up some time to draft up a curricular blueprint of sorts.

I spent the next couple months dreaming up one week's worth of instructional activity after the other, imagining ways to translate the learning objectives from CMPSC 100 into activities that could be contained within (and contribute to) the infrastructure of `term-world`. I was able to hash out a rough plan that saw students starting by interacting with the space in their `home` folder (literally, a virtual space for each of them to call their own) and gradually contribute to the greater infrastructure of `term-world`, at first in trivial and novel ways, then eventually in more impactful ways.

From my time dreaming about the project and mapping out possible instructional activities, one key aspect of `term-world` that I didn't initially understand has become more concrete to me: `term-world` is meant to be a persistent metaphor in absolutely every sense of the word *persistent*. In the same way that programmers often build on the code and programs that came before them, one of the draws of `term-world` is that it can have the capability to persist from one semester to the next, with the creations and contributions of students standing tall in digital space long after those students have passed the course.

Some day we hope to look out over the virtual landscape of `term-world` and see the numerous creations from the students that have inhabited its digital space; we hope to see the cumulative result of generations of students grappling with philosophical questions like "how do we best govern ourselves" made manifest in code; we hope to see a narrative of lessons learned and preserved for posterity.

In just a few short days the formal period of time funded by Allegheny's URSCA office to create `term-world` will officially begin. For now, we have little more than a blank canvas and a blueprint.

But soon, we break ground and begin to build a *world*.