+++
title = "A whole new world"
date = "2022-07-11"
author = "Douglas Luman"
authorTwitter = "douglasjluman" #do not include @
cover = ""
tags = ["pedagogy","design"]
keywords = ["", ""]
description = "A look at how we make decisions in building assignments and interfaces for our contemporary notions of a \"teaching machine.\""
showFullContent = false
readingTime = true
hideComments = false
+++

## Talking to ourselves

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

## "Inside Baseball"

My first shot at using a collaborative cloud platform, an implementation of 
[JupyterHub](https://jupyter.org/hub) found major support in Barba, et al.'s digital text 
[_Teaching and Learning with Jupyter_](https://jupyter4edu.github.io/jupyter-edu-book/). In
the text, the authors highlighted a key tension that pertains to computer science in some
special ways, namely that our systems and assignments have to balance the exchange between
the "technical" (too much detail) and the "magical" (not enough detail). 

Many folks may recongize this as the struggle of what many folks call going "inside baseball" 
-- descending to such a technical level that only true "insiders" would understand.

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

## Beyond the binary

The above example illustrates the kind of thinking which lead our team to make the binary continuum 
("techical" vs. "magical") into something that depicts _three_ forces. After all, if we think about
computer code like writing, we can think about "reading" it (this idea, of course, borrows substantively
from Annette Vee's work on coding-qua-literacy; see [_Coding Literacy_](https://mitpress.mit.edu/books/coding-literacy)).
Formal language (code) looks somewhat _like_ natural language (writing/speaking), so we can rely on
student _intuition_ to understand what we mean when we propose the order in which code interprets or,
in some cases, compiles.

Add to this the fact that we've occupied ourselves with making a simulacra of an actual _world_ -- one
in which doors push open in ways that we can easily predict, we have ["deep structures"](https://en.wikipedia.org/wiki/Deep_structure_and_surface_structure)
in language which allow us to organize our written and spoken language in ways that demonstrate an inherent
understanding of word order or, at least, the ways in which to interpret it. (For a real mind-bender, review
the [order of adjectives](https://owl.excelsior.edu/grammar-essentials/parts-of-speech/adjectives/order-of-adjectives/),
which you -- magically -- probably already know without learning them.)

But, to our world: sometimes a toaster should work like a toaster. You use it, and it produces toast. (Yes,
there are toasters in `term-world`.) If we make a dust-cleaning automated robot, it should (in an automated fashion)
clean up dust. Consequently, there should be..._dust_.

Many CS professors teach in such a way that (much to many a student's frustration), they pose questions to students
about what _should_ happen in a given situation given what the student knows. Assuming a student's understanding
of the concept of the sentient house-cleaning robot, we might expect, then, that a student could pop open the 
code behind the robot and observe how it works and read the code with some level of understanding, even if
they don't know _everything_ that it does or how it accomplishes these functions, technically. (Spolier: it's _very far_ from sentient.)

### Do you believe in magic?

The push-pull relationship between technical function and intuition is clear enough: nearly every one navigates it
every day. But, what is this about _magic_? 

At the simplest level, I've always seen my job as an introductory-level CS professor to be one of a kind of marketer: essentially
a "hype" person. While some students opt for a deep understanding of the techincal aspects of CS based on a prior interest in
kinds of disassembly. Though that profile doesn't describe every student, nearly every introductory student has or will experience
the ["programmer's high"](https://slate.com/technology/2014/06/coders-high-the-intense-feeling-of-absorption-exclusive-to-programmers.html),
a kind of quasi-magical/spiritual experience that transforms most of those who undergo it, giving them some form of a computational
mission for the remainder of their lives (whether or not they "major" in the discipline).

That phenomena withstanding, the folks working on `term-world` recognize its power. For many, the engagement with a magical phenomena
can (and _should_) extend to folks who, for the first time, can directly translate a computational activity to their lived experience.
In our building, we've refactored this binary into a..._trinary_.

<style>
p img {
  position: relative;
  margin: 0 auto;
}
</style>

![Triangle showing "magical", "intuitive", and "technical" at the vertices](/img/term-angle-diagram.png)

At the risk of having made you read too long, dear reader: how does one balance creating assignments and experiences that aspire to the
"sweet spot" (the middle of the three-force system guiding our build): by creating assignments that mimic real-world objectives, achieve
solutions authored by students, and _still_ have an impact in _what they do_.

Here, I introduce the assignment sequence that best typifies our building principles: one that occurs roughly halfway through the semester,
and thinks about survelliance, data-gathering, and the consequences of student actions.

## There's something rotten in the state of `term-world`...

(For the sake of giving technical back-end for these:

* [`term-world` Week 5](https://github.com/term-world/activity-week-5)

The curtain opens on `term-world` city hall in disarray, meaning: data is strewn about _everywhere_, and students have to do some manual
analysis to keep the governance structure running. We need new processing systems because we can't get the old ones back online.

We start by giving students what essentially amount to very basic spreadsheets about `term-world` residents (i.e. everyone involved in the
class). Programmers gain experience looking at data, recalling basic lessons on data types, and create very basic data analytics engines
to tell the mayor (i.e. the professor) various things about the citizens of `term-world`. Hopefully, everyone feels very office-worker-y.
Much cubicle; very bore.

The next week, given that city hall is more-or-less OK now, students operate on data about _themselves_ -- average work time, productivity, 
et al. -- and get a sense that _they've been watched_. The goal here is to continue a surveillance program that had been underway in order
to set a bar for the "ideal" `term-world` worker. From there, students will need to make decisions based on the data that _may_ constitute
adverse action.

Of course, the data is synthetic. But, the experience is real and begins to focus their thinking on experiences and impacts of technical
systems they author. This small nod to _magic_ based on the technical and intuitive understandings they both come to class with and develop
while in `term-world` should lead to what we hope to be a pivtoal moment in the class, only a week or two before they embark on the free-form
course project.

## All's well that...ends?

A major feature of the above activity is unscripted. Will students realize what they're doing? Will they opt to, instead of completing the project,
resist? These are built into the assignments as ways to understand and articulate the technical workings and impact of the "system" we're fictionalizing
for them. But, for us, the outcome is indeterminate.

However, the primary objective here is to create an _experience_, something that we aim to do in whimsical ways with toasters and cleaning robots and
serious ways like our world-altering proposition at the mid-term mark. If, then, by magic we mean to create a kind of enchantment by leveraging
fully-aware learners entering into a kind of fog of the uncertain, we trust that they can engineer their way to the other side or -- at least -- find
a way to demystify the environment in which they find themselves.

But, not without going through some tricks first.
