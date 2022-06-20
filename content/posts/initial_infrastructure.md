+++
title = "Discovering a New World"
date = "2022-06-19"
author = "Mai-Nguyen"
authorTwitter = "" #do not include @
cover = ""
tags = ["introduction","student","process"]
keywords = ["", ""]
description = "How another student came to join the term-world team, and their early efforts to build out the platform's infrastructure."
showFullContent = false
readingTime = true
hideComments = false
+++


Before attending Allegheny College, I did not expect that I would end up pursuing a Computer Science major; my mom would never allow me to do so, and I had always been an obedient daughter...well, until my first encounter with the discipline. I still remember that my very first practical lesson was constructed as a scavenger hunt game, where students had to use newly learned syntax to hop to different directories on the computer to find pictures of Ulysses - Professor Luman’s beloved cat. After the class, I couldn’t stop telling my friends how fun the lesson was (until they stopped me because I talked too much).

After the first semester, I decided that Computer Science was going to be my major - my first rebellious act against my mom!

Up until last semester, I had a chance to become a Technical Leader for Professor Luman's Computer Science 100 class. That class had a magnificent number of enrollments---45 students---which is probably the biggest class offered at Allegheny in this decade. Such an incredible figure wound up raising a couple questions for the Professor and my fellow Technical leaders: 1) how do you keep such a big class going without freezing the server (something that happened frequently with Jupyter Notebook, the platform being used at the time) and 2) how do you keep such a large body of students engaged throughout the course?

Unlike Danny and Jeff, I was not really looped into `term-world` from the beginning. Sometime in March (two months after the concept was first being discussed) in one of my meetings with Professor Luman, he introduced the idea of “gamifying” the curriculum. The idea immediately had its hooks in me; I knew that this approach had the potential to keep the fire of engagement burning in most---if not every---student in CMPSC 100 class.

## The First Two Weeks

In order to realize `term-world`, a persistent and immersive digital environment for students, infrastructure is one of the first things we have to construct. In the first week, I was introduced to the concept of managing a `docker container`, where each student is bound to a distinct container once they log in to the server. One of the big questions was how to ensure that every student could retrieve a container and access VS Code---a code editing platform, or IDE for those in the know---right after the authentication process. 

Since this was my first time working with NodeJS, JavaScript, and multiple back-end tasks, I was overwhelmed at first. However, after two weeks of work, we now have `term-hub`: a repository that handles the construction of servers and containers. The discussion gets a bit technical at this point, but now we've successfully tackled the following objectives:

1. The container is opened successfully once a user logs in through OAuth2 authentication and only if their GitHub username is affiliated with the `Term-world` organization.

2. The user is successfully directed to their own VS Code hub upon logging in

3. The containers are named under the user’s GitHub username

4. The containers are stopped and removed successfully on `SIGINT`, `SIGTERM`, `exit`, and when the socket closes on the user’s end.

The biggest obstacle last week was figuring out how to stop and remove containers once an interrupting or kill signal is requested. This task shouldn't have been too difficult with a `prune` process in mind. For Docker containers, if the developer only stops and removes the container itself without pruning it, two problems will occur: 

- Users won’t be able to reopen their container as the username is already set under their GitHub username, and Docker won’t allow two containers with the same name to work simultaneously.

- The host device which operates the server will suffer from the heavy consumption of memory from `stopped` but `unpruned` containers, as one of these containers may take `300+ GB. 

Unfortunately, Docker's documentation wasn't particularly helpful in determining how to `pruneContainer`; it was quite troublesome to find a solution to do so (especially noting that prune processes always take time---if the process exits before the container is pruned successfully, the system crashes if users try to log in again).

However, we then decided to use the `async` approach, a function in JavaScript that allows developers to govern the synchronization of commands. `await` command is the striker in this case, as we can make sure that each container is pruned before exiting from the process on `SIGINT`, `SIGTERM`, `exit`, and when the socket closes on the user’s end.

## Coming Soon...

There's still a *lot* of work ahead of us; however, we will begin working on curriculum next week. One of the tasks I'm particularly looking forward to is thinking of a way---an extension, a plugin, or an existing tool---to automatically evaluate the quality of students’ submissions, focusing on their code and documentation. In this way, each student will be rewarded accordingly, which will not only create a fair grading environment but also incentivize and encourage students to contribute frequently to group or individual projects.

All that having been said...stay tuned for future developments in `term-world`!




