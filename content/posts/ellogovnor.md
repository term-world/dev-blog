+++
title = "To Rule a World"
date = "2022-06-22T11:15:26-04:00"
author = "Jeff Normile"
authorTwitter = "" #do not include @
cover = ""
tags = ["student","progress","governance"]
keywords = ["", ""]
description = "An examination of the steps taken to begin implementing a form of governance in term-world."
showFullContent = false
readingTime = true
hideComments = false
+++


If you peek at our [about page](https://blog.theterm.world/about/) you'll see that one of the primary goals of `term-world` is to:

> [. . .] provide both a playground and persistent digital metaphor through which to consider
> real-world ethical and civil questions regarding governance, justice, equity, and other social
> infrastructures not typically included in computer science education.

In order to create conversations around many (if not all) of those social infrastructure questions within the context of `term-world`, there's one thing that the experience *has* to provide: some formal means of collecting and gauging public (student) opinion.

Thus, my work over the first couple weeks of development for `term-world` has largely consisted of building and implementing a (relatively) simple means of governance within the world: the `governordesk`.

## Ello, Gov'nor

The `governordesk` is the first thing to actually *inhabit* the otherwise empty world being created by our team. While Mai & Luman were tirelessly working to essentially build the canvas on which we build our world, I had the (arguably more entertaining) task of actually putting something *on* that canvas.

"Governance" as it currently exists is relatively simplistic in its execution. A user with some measure of authority (e.g., a class instructor or one of its teaching assistants) issues a poll with predefined options to other users, and a simple majority response for any of those options results in that option "winning". Within development these polls have been such high-stakes questions as "Puzzles or boardgames?" or "Pizza or tacos?" though we envision a time when questions like "Do we spend class time reviewing for loops or move on to new content?" might be tackled by the polling system, or a time when the system will be used to select elected student officials. (Students will be assigned groups at the start of the course, and we currently imagine that elections will be held to grant one member in each group the status of "elected official", enabling that student to engage with the `governordesk` in a meaningful way and more directly shape the governance of `term-world`.)

The `governordesk` and its functionality allows any of this to take place. When a user engages with the `governordesk`, they're presented with a few options, namely: creating polls, closing polls, and viewing prior poll results. In order to accomplish *any* of this, the `governordesk` uses a database hosted on CouchDB (an open-source platform that allows for the management of databases free of charge) to store polls, votes, and poll results. 

Much of my time was spent coming to grips with the technical back-end work to get `term-world` to communicate with the database hosting our poll data--having written my first line of code less than a year ago, there were *quite* a few knowledge gaps that required filling in. But with more than a little help from our project advisor, I was able to fill at least enough of those gaps to cobble together *a* solution. (Though we've already identified numerous ways that the current implementation can be improved upon should time allow this summer.)

## So, How's It Work?

At its most basic level, when generating a poll, the `governordesk` writes a document that is then stored to the database. This file contains such information as a polling question, the defined response options, a timestamp for when the poll was created (for recency sorting within the database), and a flag that indicates whether the poll is open or closed. A separate extension (that also had to be developed, though much of that work was performed by Luman)sends this information out to users connected to the `term-world` platform, and each time a user answers the poll their response is stored as a separate document within the database. These other documents contain an id referencing the original polling question, the selected response, and data pertaining to the user that submitted the vote (to track and ensure that each user only has the opportunity to respond to each poll once).

Then, when a user decides that it's time to count the votes for a poll and close it out, they can use the `governordesk` to do just that. After selecting a specific poll to close, the program sifts through the database and pulls out each vote with an id matching the polling question being closed. Votes are tallied, and a relatively simplistic text display identifies how many votes each response received. A user has to look at the output and manually determine who the winner is (a trivial, though potentially annoying task)--with the idea being that eventually students will be asked to improve the functionality of `governordesk` to correctly determine the winner and display information regarding the percentage of votes each response received.

## Building `term-world` *for students*

That's actually been an important but significant developmental challenge in creating `term-world`: making it sophisticated enough to accomplish the task at hand, but intentionally leaving open space for its basic functions to be improved upon. The goal is to provide students opportunities to contribute to `term-world` meaningfully, building on the basic infrastructures we provide to bring the platform's functionality to the next level.

Part of leaving that space open for students also means creating as many of the building blocks of `term-world` in as non-complicated a fashion as possible--if you're going to add a new gear to the machine, you really have to be able to understand how the rest of the machine works in order to ensure your new addition fits in as expected.

In many ways, because my computer science education is the least developed out of any of the project contributors, that's given me a bit of an edge in creating code that's more "readable" to the average CMPSC100 student--a student that will have never read a line of code before. Many of the optimizations that might be automatic for more experienced developers--ones that make programs faster, more efficient, or more resilient (in terms of handling errors)--would never occur to me, and that's potentially beneficial when those optimizations might "clutter" a program's basic function or intent.

This will be a key understanding our team will need to keep in mind as we start to fill the blank canvas we have now with more *things*: we get a baked-in educational "win" for every one of those *things* that can be understood by the students we're aiming to teach. The whole point of `term-world` is to provide a playground that our students actually join us in building--if we provide the swingset and ask the student to build the swing, we need to be mindful that they can readily see where and how their product attaches to what we've already built.