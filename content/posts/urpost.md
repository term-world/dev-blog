+++
title = "Introduction, or 'In a World...'"
date = "2022-05-23T10:21:55-04:00"
author = "Doug Luman"
authorTwitter = "douglasjluman" #do not include @
cover = ""
tags = ["process","pedagogy","introduction"]
keywords = ["brian dear","jupyter","education","pedagogy","terminal","B.F Skinner", "teaching machines", "PLATO"]
description = "The temptation to see innovation or new ways of thinking (or, in our case, teaching) as springing fully-formed from nowhere in particular exists as a particularly pervasive mindset in technology-adjacent fields -- in this instance, the popular canon of computer science. Here, we document our beginnings as a project and how this responds to prior work on teaching machines."
showFullContent = false
readingTime = true
hideComments = false
+++

## Introduction

Having just graduated the 2022 class, the 200-something<sup>th</sup> in the long history of Allegheny College, I once again realize that the undergraduate team behind the project you're reading
about shares something with the past weekend's newly-minted alumni: the sense that we build on and through a sense of history. The temptation to see innovation or new ways of thinking
(or, in our case, teaching) as springing fully-formed from nowhere in particular exists as a particularly pervasive mindset in technology-adjacent fields -- in this instance, the popular
canon of computer science.

I started my nascent career as a CS professor without a full appreciation of deep history of teaching "moves" in the discipline. Though I consider myself someone who is preternaturally 
skeptical of the so-called "awe of implementation," I found myself feeling particularly clever about how I'd just taught a subject without realizing that this self-satisfied 
apprehension existed in a vacuum. Spoiler: I _was_ living in a vacuum. 

Modern computer science education has its own litany of innovators and teachers who have set and reset the course of CS education. We benefit from the fact that much of this work 
is taking place in real-time. I set about reading dense Twitter threads about whether or not `while` statements are introductory material or how students have difficulty 
with what folks as old as I am consider traditional ideas about "folders" and file organization. This community likes to talk. A lot.

In the midst of that effort, I started reading books on computer history and came across Brian Dear's _The Friendly Orange Glow_. By now, reader, you've intuited that I'm about
to tell you that the book changed everything. It did. I recall pulling to the side of the road on my drive to campus during the summer of 2021 to take notes -- I experienced it as
an audiobook -- on the little-known history of BF Skinner's obsessive mid- to late-career focus on "teaching machines" and, of course, the history behind even that "move." As
expected, the thinking behind what Skinner was up to post-"Skinner box" relied heavily on writing that predated his work by decades, and Dear's work explores how these sources
made it into a later system called "PLATO," which was the last of the great "teaching machine" experiments that I've come across in reading since.

If you're following along with `term-world` at home, it's fair to say that Dear's book is essential reading.

But, how does that all relate to _this_ project? It's more than obvious to say that the on-going COVID-19 pandemic has changed nearly everything about education. It seems a bit
cheap to assert that fact, but `term-world` owes its beginning to decisions made to respond to the emergencies of the moment: somehow I had to teach the 2019-2020 academic
season remotely and in such a way that I didn't have to troubleshoot students coming from vastly different backgrounds with equally differing computer setups. This was compounded
by the fact that we'd just made the decision to transition our introductory course from Java to Python.

Enter: [JupyterLab](https://jupyter.org/), a platform that, among its many features, includes live "terminal" (i.e. command prompt) access to a single, shared machine -- one that
I could control and use to constrain the possibilities of things going truly awry. The last thing I wanted was a remote mutiny.

I've taught through this platform for the last two years using resources like [Teaching and Learning with Jupyter](https://jupyter4edu.github.io/jupyter-edu-book/) (special thanks
to Barba, et al.) and other ways that I put together to make the experience a bit more "game"-like. However, most of the work I did to pivot the class relied on ideas of
"asynchronous" learning, which supported students beyond my class sessions so that they could complete the work in as self-directed/self-supported a way as possible.

And, then, Dear's book "happened" to me. In Skinner and the work that informed his experiments with teaching machines, I knew something could be different. Of course, realizing
this in late July, with the semester almost upon me, made it less possible to fully realize the change that this narrative started. Talking with students over the course
of the semester and into late January of 2022, I discussed how I was still looking for the right metaphor -- a way to structure the class around a framework that could function
something like a teaching machine.

One thing remains true, however, from this experience: the classroom is a fundamentally changed place. I started making decisions to fully "flip" the classroom and given some
level of conceptual control and responsibility for knowledge formation back to the students. Especially as pertains to education, the "Zoom" era has, for many "applied" subjects,
made lecture obsolete. Students voiced a desire to come back to campus not, I feel, for the chance to come to class, but to be part of a class community, a peer space
which enables learning. In the best cases, the professor's role here, though significant, is invisible as such. Realizing this, I returned to bell hooks more than anything 
related to Bell Labs.

What has been a radical pivot for me results in the project you're reading about now.

## What is `term-world`?

In short, we're building an immersive world game that serves as the platform for the Allegheny College introductory computer science course, CMPSC 100: Computational Expression.

It's no surprise that the students working with me on this summer research project (generously supported by the [Allegheny College Undergraduate Research, Scholarship, and Creative
Activities (URSCA) office](https://sites.allegheny.edu/research/examples-of-ursca-at-allegheny/)) are the same students with which I've been talking. Professors at Allegheny
rely on their students to push them, to test ideas, and to be co-creators in the learning process. Conversations with Danny, Jeff, and Mai have (over the years) often resulted
in me understanding my practice better. Here, we're turning that motivation into a physical reality.

So, why `term-world`? In my undergraduate days, [Second Life](https://secondlife.com/) was a _big_ thing. (Side note: the rise of the "metaverse" is pretty much an echo
of this time.) Without a vocabulary for it, educational institutions were going "all-in" on immersive education, mostly centered around asset creation -- buildings, items in-game,
etc. -- without approaching it as "systems thinking." It was creation for creation's sake or -- at worst -- the "awe of implementation" all over again. Our approach to developing 
`term-world` contemplates these contemporary references alongside the historical ideas of "multi-user dungeons" (MUDs) and, of course, lessons learned from systems like PLATO, 
games like "Space War" and "Adventure" (from the early Digital Equipment Corporation PDP hacker era), wrapped in the kinds of student-directed/community learning the work by Dear and
hooks surface, with particular intellectual debt to bell hooks.

Being that this work is housed at a liberal arts institution, we take up a multi-faceted interest in "community" in that we aim to establish a digital community that thinks about
governance, economy, infrastructure, and norms or ethics. In many ways, this project aims to be as ultimate a sandbox as we can make it, one that develops class by class over time.
If one class thinks that ranked-choice voting is the best governance structure, it's entirely likely that the next could develop something wholly different. Equally, it's
inevitable that a class 10 years from now might have very different ideas about how to structure in-world reward for labor. 

Tackling questions that result in software/digital interventions aims to demonstrate how computational work supports so much in "real-world" goings-on, from voting machines to
the influence of digital currencies and payments. Considering the variety of students we see in the CS department and how their careers will be shaped by technical knowledge, the
`term-world` team maintains a sincere interest in how students will respond to these challenges as prompts.

This means that we're also interested in asking questions around "systems thinking" and the interdisciplinary status of computer science as a subject. While I'll let the students write about the
"what" of the worldscape, I see this project as a chance to repair and advance my (and others') thinking about immersive world education and what happens when you let students
determine the contents of their world. As a department, we know that we retain some number of students who come through the introductory CS course, but also that 
we send a greater number to all of the other disciplines represented on campus. 

With `term-world` as a tool, we hope to introduce the technical aspects of those subjects that students -- once engaged as professional practitioners -- will encounter, work
that inspires questions about how voting systems work; ideas about new technologies in economics; thoughts about how, if given the chance, one would redesign social infrastructure
to enhance human experience.

These are big goals; they're practically unattainable. In many senses, they're also probably impractical. The questions inherent are, by nature, without a fixed answer. But, we
believe in the transformation brought on by the attempt. The artist [Douglas Kearney](https://www.douglaskearney.com/) once wrote that writing (here, I substitute _all_ expression) is a "danger room." And, for me, the idea of a 
"teaching machine" feels like it could essentially be a sparring partner, an environment to "train up" or "try out." The virtual space is a place that we can use to simulate
this danger room, allowing students to gain confidence in an expression method which has come to not only dominate, but characterize daily life. We provide `term-world` as a sandbox
to do both of these things, and allow our students and ourselves room to practice and spread the computer science adage to "fail hard, and fail fast."

As much as we're also trying things out, Danny, Jeff, Mai, and I invite you to our world: 
[project GitHub](https://github.com/term-worldhttps://github.com/term-world)!
