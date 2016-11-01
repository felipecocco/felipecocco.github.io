---
layout: post
title:  "Teacher Experience Prototype ready-ish!"
date:   2016-11-1 10:00:00
categories: [jekyll]
tags: [thesis]
---
The teacher classroom experience prototype is almost ready!!!

Seeing the experience come together.
====================


One of the key pieces of advice I was given throughout this entire process is to focus the design efforts on the aspects of my solution's experience that are unique to it; to focus on the key features of the design. As a software solution that purports to allow teachers to quickly look at their student's performance and create on-the-fly review groups, making sure that experience is quick and easy for teachers is the most important thing.

Looking at actual data is key
----------------

Despite having been told this many, many times by several people, I did not start using ACTUAL quizzes and tests in my design process nearly as early as I should. For one, it definitely helped to visualize the workflow coming together. As silly as it may be, I think my "designer juices" definitely started flowing more once I was looking at actual information, perhaps because it made it that much easier for me to inhabit that role of the teacher using this in their classroom.

Secondly, the other thing about actual data is that it could have easily led me to discard certain ideas. I have noticed that I have a penchant for designing more and more complexity and losing sight of user goals. One idea that surfaced time and time again in talking to advisors and teachers was to "tag" questions so that my sorting algorithm could see if students were missing questions that had related content or that required the same sort of concepts. While this sounded great in theory -- and I spent a few days trying different ideas about how to add tagging -- once I looked at actual quizzes and tests that my own school used, it quickly fell by the wayside.

First, the volume of questions is never enough to justify such a system -- a typical homework quiz that is given at Escola Móbile may have anywhere between 10-15 questions. But, more importantly, homework assignments follow two typical patterns: Review or formative assignments. If the HW assignment is a review, there is likely several different types of content that is requested in it, and very few overlap; conversely, when students just learned a specfic content, homework assignments often consits of drills that deal with the same piece of material over and over again. In reality, therefore, the tagging system would either have questions that all have a different tag or questions that all share the same tag. While this would make sense if you are thinking of broader interventions, since the point of this tool (for now) is to simply help teachers review A SINGLE assignment, it is for now an unnecessary feature that just complicates the design.


A deep dive
---------------

The following is a short video showing the teacher experience as it is prototyped right now. I am especially proud of the interface that allows teachers to change groups once they are seated. Teachers can simply drag students to other tables, and the groups are automatically re-shuffled.

<div style="width: 100%; height: 0px; position: relative; padding-bottom: 60.912%;"><iframe src="https://streamable.com/9mmm" frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen scrolling="no" style="width: 100%; height: 100%; position: absolute;"></iframe></div>


The big question I have now is when it comes to discoverability. When it comes to interface elements that we all know, we can rely on the fact that users have some knowledge about how to navigate it. With the dragging interface -- or the fact that teachers can change the question's rating -- these are design features that are unique to my platform. How do I properly convey to users that they can do that?



Next steps
----------

The design as it stands now is very close to being functional on the part of the teacher. There is maybe two, three days of work left to make it fully clickable and explorable by someone pretending to be a faculty member, and perhaps another day left to simulate real-time student input. Therefore, I'll turn my attention now to tightning my paper together and then devote my attention back to polishing the prototype!





