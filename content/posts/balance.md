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
kinds of disassembly. 

<style>
p img {
  text-align: center;
}
</style>

![Triangle showing "magical", "intuitive", and "technical" at the vertices](/img/term-angle-diagram.png)
