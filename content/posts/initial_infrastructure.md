+++
title = "The tale of Computer Science 100"
date = "2022-06-19"
author = "Mai-Nguyen"
authorTwitter = "" #do not include @
cover = ""
tags = ["introduction","student","process"]
keywords = ["", ""]
description = "This is a story of a student who later joined the team and the introduction to the initial construction of infrastructure."
showFullContent = false
readingTime = true
hideComments = false
+++


## The tale of Computer Science 100:

Once upon a time (well.. it was 3 years ago), there was a group of students, some with, some without any prior computational knowledge; they were directed by a very fresh face in the land of Allegheny at the time - Commander Luman. Together, with the tremendous support from His Highness Ulysse, they successfully conquered the fundamental wisdom of computer science, then proceeded on their own greatest journeys. 

While the first odyssey was phenomenal, the rapid growth of technological advancement then inspired the Commander to come up with various approaches to overcome the complicated quests, starting with changing the language from Java to Python, then adjusting the coding medium from Atom to Jupyter Notebook. However, the Commander and fellow Captains (aka Technical Leaders) remain unsettled with the current procedures, until they decide that they should create a “mansion”, which is a collaborative virtual battlefield where students can contribute their thoughts and ideas, in the form of digitally tangible commodity, through resolving hypothetical issues. 

Such an approach has a fancy term: “gamification”! And from there, a new expedition began …

## A few words on how I joined this wonderful odyssey: 

Before attending Allegheny College, I did not expect that I would end up pursuing a Computer Science major. The firm reason behind this thought is my mom will never allow me to do so, and I had always been an obedient daughter … until my very first encounter with Computer Science. I still remember that my very first practical lesson was constructed as a scavenger hunt game, where students have to use learned syntax to hop to different directories on the computer to find the pictures of Ulysse - Professor Luman’s beloved cat. After the class, I couldn’t stop telling my friends how fun the lesson was until they stopped me because I talked too much :cry: .

After the first semester, I decided that Computer Science will be my major, marking the first rebellious act I have against my mom!

Up until last semester, I had a chance to become a Technical Leader for Professor Luman's Computer Science 100 class. That class has a magnificent number of enrollments - 45 students - which is probably the biggest class offered at Allegheny in this decade. Such an increment indicates the rising interest of students in fundamental Computer Science classes regardless of their majors or minors; and in return create a potential issue for Professor and fellow Technical leaders, which is how to govern such a big class without freezing the server, which happen frequently with Jupyter Notebook, and how to keep the will of studying of every student throughout the semester.
Unlike Danny and Jeff, I was not involved in the loop from the beginning. Two months after the dawn of the concept, in one of my meetings with Professor Luman, I was literally dumbfounded when he introduced his idea of “gamifying” the curriculum. I was immediately hooked by this idea, as I know that this approach if operated successfully, will be able to keep the fire in most, if not every, student in CMPSC 100 class. From that moment, I have stepped on the boat of a marvelous expenditure, which is full of uncertainty waiting for us ahead.

## The first week into the construction of infrastructure:

With the birth of `term-world`, the home ground of our project, where we aim to provide a persistent and immersive digital environment for students, infrastructure is one of the first things we have to construct. In the first week, I was introduced to the concept of managing a `docker container`, where each student is bound to a distinct container once they log in to the server. One of the big questions was how to ensure that every student can retrieve a container and access VS Code right after the authentication process. 

Since this is my first time working with NodeJS, JavaScript, and multiple back-end tasks, I was overwhelmed at first. However, after the first two weeks, with the main work from Professor Luman, `term-hub`, a repository that focuses on the construction of servers and containers, has successfully tackled the following checkmarks:

1. The container is opened successfully once a user logs in through OAuth2 authentication and only if their GitHub username is affiliated with the `Term-world` organization.

2. The user is successfully directed to their own VS Code hub upon logging in

3. The containers are named under the user’s GitHub username

4. The containers are stopped and removed successfully on `SIGINT`, `SIGTERM`, `exit`, and when the socket closes on the user’s end.

The biggest quest during last week was how to stop and remove containers once an interrupting or kill signal is requested. This task should not be too hard, if `prune` process is not involved in the conversation. For Docker container, if the developer only stops and removes the container itself without pruning it, two problems will occur: 

- Users won’t be able to reopen their container as the username is already set under their GitHub username, and Docker won’t allow two containers with the same name to work simultaneously.

- The host device which operates the server will suffer from the heavy consumption of memory from `stopped` but `unpruned` containers, as one of these containers may take `300+ GB. 

With the lack of direction on how to use `pruneContainer` on Docker’s main documentation site, it was quite troublesome to arrive at a solution to do so, especially when prune processes always take time, making the process exit before the container is pruned successfully, which then crash the system when user try to log in again.

However, we then decided to use the `async` approach, a function in JavaScript that allows developers to govern the synchronization of commands. `await` command is the striker in this case, as we can make sure that each container is pruned before exiting from the process on `SIGINT`, `SIGTERM`, `exit`, and when the socket closes on the user’s end.

## Then…. What’s next:

The task is still piled up in front of us; however, we will emerge to the curriculum stage next week. One of the big tasks I am very much looking forward to is to think of a way - an extension, a plugin, or an existing tool - to automatically evaluate the quality of students’ submissions, focusing on their code and documentation. In this way, each student will be rewarded accordingly, which will not only create a fair grading environment but also incentivize and encourage students to contribute frequently to group or individual projects.

So…. Please stay tuned for our next expedition!!!!




