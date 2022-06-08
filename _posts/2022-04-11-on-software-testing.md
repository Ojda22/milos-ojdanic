---
layout: post
title: Let's start with Software Testing
subtitle: Why do we test software?
thumbnail-img: /assets/posts/testing.png
tags: [fundamentals, software testing]
---

```The true subject matter of the tester is not testing, but the design of test cases. by Paul Ammann and Jeff Offutt```

It is well known that software affects our behaviour, movement, health, relationships, etc. Overall, it influences our lives. With staggering advances in the medical sector, transport industry, power grids, communications, trading, financial sectors... we rely upon the systems in control to be reliable and high quality assuring. And they are, most of the time, repeat: most of the time. 
Software took control, and it is the driving force of the world. If someone finds this arguable, I will remind its role during the last 3 years, when the world was in chains of the pandemic.
Thanks to the software industry, and staggering human intellect, we managed to save lives and economies. This is a sign of how large the software industry has become and how complex are the systems providing us with the services.

However, not many users know that the software can fail to deliver. It is not visible to daily users that there is a set of well-crafted procedures behind every software unit that deals with software design, development management, and software testing as an evaluation guardian standing between users and unreliable software.

Although many factors influence the reliability of the software, the factors that can be both certain and uncertain, this guardian has been staying straight and refuses to give in to the waves of innovations without assurance of testing thoroughness.

Fortunately, or unfortunately for the guardian, it currently deals with a new wave. New software development continuous integration processes have put the most potent pressure on testing so far as they balance thorough testing and tight delivery schedule. 

Yes, it is hard to balance. Yet, these two factors are mutually dependent. Think about it, if the system does not satisfy high-quality expectations, it will neglect rapid delivery, and if there is no rapid delivery, it will neglect high-quality expectations. Thus, besides investing all the efforts in rapid delivery, synergy is required between stressing the units of complex systems and the interaction of different software components heavily.
This combination in test-driven development makes the key to functional requirements and hides the key to the success of software products now and in the future.

### How does it comes that software can be unreliable? My social apps never let me down?

Let's be clear that software development is an engineering discipline. Like all other disciplines, engineering products are ofter diverse. 
As in civil engineering, when we build from house to bridge, in the software industry, also, the scope is quite broad. It goes from the social app where we can exchange with our friends from the cosy sofa, from the exchange with a NASA rover from Mars, asking him if there is a cosy chair up there? or down there? :) 
This software spectrum goes to the control rooms of nuclear reactors, aerospace vehicles, CT and MRI scans, and many more.

Even with our guardian (software testing practices), disasters in software occur and often have severe consequences for health, environment and economy, which usually results in severe disasters. 

Before you depart and start investigating severe disasters related to the software (you will find some references at the bottom), you need to know that not all the problems related to the software end up with consequences.
That's why you need to learn about software faults, errors and failures (and yes, remember, don't be judgmental, remember all the lives saved by software, increased well being and what it brought to science).

Before discussing these 3 major concerns of each software practitioner, it is essential to emphasize that each defines its definition of fault, error, and failure based on the area (remember engineering area).
It is justifiable, right? The fault occurring in your social media app is not the same concern when the fault occurs in a critical safety system that can cause someone to lose their life.

Nevertheless, let's try to describe them as broadly as possible:

The fault is a defect in the software's internal state. You know that the software is a set of instructions that we indicate a computer to execute.
During the execution, everything that happens in the program (variables, counters, memory, i/o, etc., you don't need to know about this) considers a program state, leading to an output.
Therefore, a fault is a design mistake occurring inside the program state and relates to those instructions. It occurs as a product of a constrained (far from flawless) human decision-making process.
And as long as the human nature of thoughts is not perfect, and as a human is the one that writes the software, at least for some time yet, we will never be able to eliminate all possible faults of the software.

```The faults are easy to make, but difficult to catch``` by MIT mathematician Edelman

As soon as the fault manifests and makes an incorrect internal program state, we are dealing with errors in the system. Errors are okay, as long as they are handled tho.
Think about it, have you ever tried to fill a form field with a date format that is not quite the one that particular software prefers (or at least the software engineer that wrote it)? And usually, it tells you what kind of format it prefers? 
What happens is that your input is about to produce the incorrect internal program state, but the engineer anticipated the scenario, leaving you the note.

In an alternative scenario, if the engineer didn't care much about how you interact with the system for another field (it didn't consider the broad spectrum of scenarios), it left you the possibility of making a software fail to deliver you what you want. More formally, Software Failure occurs as the incorrect external behaviour of the system concerning the expected behaviour (software requirements or another means of describing software behaviour)

Over history, there have been many failures, some more known than others, related to CT scans, providing extensive radiation. Examples include rocket lunches, processor chips, and automotive faults, causing recalls of millions of products and causing massive economic damage in favour of safety.
Besides the significant threat of having software not functionally assured, it is also essential to know that the software faults do not propagate only to functional failures.
Many security vulnerabilities of the system are the product of faulty software. Such a system leaves the door open for not ethical practitioners to exploit the software of their own will.
Many areas, if not all, are acceptable to this threat. Examples are cryptography, database, cloud, network security, etc.

Overall, the software is available to many users all over the world. The Web makes software being distributed worldwide, adding additional complexity.

And it is more crucial now than ever before to stress the systems with accumulated knowledge and gained experience in software testing to reach a reasonable level of testing thoroughness, derive high-quality tests, and test rationally while often. 



  