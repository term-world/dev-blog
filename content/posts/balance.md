+++
title = "A whole new world"
date = "2022-07-11"
author = "Douglas Luman"
authorTwitter = "" #do not include @
cover = ""
tags = ["pedagogy","design"]
keywords = ["", ""]
description = "A look at how we make decisions in building assignments and interfaces for our contemporary notions of a \"teaching machine.\""
showFullContent = false
readingTime = true
hideComments = false
+++

Writing about our work this summer, we've been weaving our way through topics 
which verge on technical detail; verbally illustrating the balancing act that
this work requires seems to mean that we work out some of our own thoughts on
the blog. We thank you for your patience as we think aloud in public. I (partly)
come from the world of composition theory, so here I name-check Janet Emig's
["Writing as a Mode of Learning"](https://www.jstor.org/stable/356095). (At
Allegheny, we often don't distinguish "code" writing (formal language) from what
most folks would call writing (natural language), so here I mean Emig's essay to
work in many senses.)

(Tangent, and probably interesting for a later blog post, you should see all of the
sheets of paper containing drawings and other scrawl that we've created to explain
our ideas to each other.)

This post zooms out a bit, returning to thinking about _how_ one might build a teaching
machine at a time of significant technical advance (since B.F. Skinner and others' early
work on the topic) coupled with our need to build a system that teaches technical topics.

My first shot at using a collaborative cloud platform, an implementation of 
[JupyterHub](https://jupyter.org/hub) found major support in Barba, et al.'s digital text 
[_Teaching and Learning with Jupyter_](https://jupyter4edu.github.io/jupyter-edu-book/). In
the text, the authors highlighted a key tension that pertains to computer science in some
special ways, namely that our systems and assignments have to balance the exchange between
the "technical" (too much detail) and the "magical" (not enough detail). 

The continuum describes a dilemma that many CS professors have to manage in an introductory class.
For example: students learning about programming need to -- to some extent -- have a basic grasp
of _how_ the Python interpreter runs scripts. Here, we could go a number of ways that describe
transpiling, the way a computer processor works, and many other topics. But, we typically don't go 
very far into any of that or into any of those topics at all. We think to ourselves "what level
of abstraction (removal from technical 'guts') gives students what they need _right now_?" 

Typically the answer to the above answer is to say that every line in a program is an instruction and
that the Python interpreter processes each of these one at a time from the top down according to "Flow
of Control." We create a kind of parallel construct -- "Flow of Control" -- to describe all of this.
Reduction -- or, in this case what really amounts to packaging and vocabulary -- gives our students 
enough techincal detail to understand what they need to know about the order of operations while still
maintaining some level of the "magic" of what happens in the "black box" of the processor.

The above example illustrates the kind of thinking which lead our team to make the binary continuum 
("techical" vs. "magical") into something that depicts _three_ forces. After all, if we think about
computer code like writing, we can think about "reading" it (this idea, of course, borrows substantively
from Annette Vee's work on coding-qua-literacy; see [_Coding Literacy_](https://mitpress.mit.edu/books/coding-literacy).

![Triangle showing "magical", "intuitive", and "technical" at the vertices](/img/term-angle-diagram.png)