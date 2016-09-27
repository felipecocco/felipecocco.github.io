---
layout: post
title:  "Setting Things Up for User Testing"
date:   2016-09-27 10:00:00
categories: [jekyll]
tags: [thesis]
---
This week I set-up my prototype to allow for Wizard-of-Oz style user testing!.

Why testing the interface is important
====================


Last week we discussed two different strands of user testing -- one which focused much more on core design fundamentals of a proposed solution, and the other which focused on testing specific design implementations which focused much more closely on user experience.

Over the summer, I managed to test out the basic premises of my solution, and the results seem promising. While I feel that the core design was validated and key assumptions "proved", the tests also revealed a number of potential considerations for the design, such as allowing teachers to re-group students, and, more importantly, the need to discriminate questions into those that were worth a group discussion and those that were not.

Part of the solution, however, requires that teachers be able to implement this solution with minimal effort. While it is pedagogically sound, it will have no impact if it requires a Herculean effort on the part of teachers to implement. Therefore, testing all of the interfaces -- particularly those facing the teachers -- is extremely important.

... there is just one problem: The teachers need to look at "actual" student input!
----------------

Let me explain: Part of my solution calls for teachers to be able to track student progress as they work through questions in class. When it comes to in-class tools, my experience has taught me that teachers are incredibly sensitive to anything that will distract them from their students, and simplicity and ease of use are incredibly important. The problem we run into in testing these interfaces is that we need to "simulate" student interactions. If the goal of the dashboard is to quickly and seamlessly communicate to the teacher student progress -- and to alert him/her that a student may need some help -- paper prototypes, or most mockups, become somewhat inefficient. There is a dynamism to having 20+ students answering questions at the same time that would be really hard to capture with any kind of static prototype. Part of the value user testing a dashboard is in finding out what questions it is or isn't answering, and ideally you would be able to simulate a diverse set of circumstances with your teacher (more/fewer students, smaller/larger groups, etc.)


Firebase to the Rescue
---------------

I am very fortunate to have implemented a small prototype in HTML, because there are a wealth of technologies available that can help me simulate the student input for testing. Ideally, the scenario that I pictured was that I could present a dashboard to a teacher, and in real-time simulate students answering questions in order to give the teacher the most authentic experience possible.

To that end, I decided to user this technology called Firebase in my prototype. Owned by google, firebase is an online database service, but with a twist that it supports real-time communication with clients, so that an update to the database gets immediately reflected on a website. Below I have a small gif that lets you see exactly how it works.

<div style="width: 100%; height: 0px; position: relative; padding-bottom: 60.912%;"><iframe src="https://streamable.com/e/1i6h" frameborder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen scrolling="no" style="width: 100%; height: 100%; position: absolute;"></iframe></div>


On the right, there is a simplified JSON object detailing all of the information that I have in the database. You can see that as soon as I add an answer to a student, the web-portal gets immediately updated. Using this set-up, it is incredibly easy to share my dashboard with teachers really far away, and update data for them while I'm having a conversation in real-time. Further, with this flexibility, it would also be possible to input ACTUAL student responses into the system, if that were the goal.



Next steps
----------

With this kind of infrastructure in place, it will be very easy to quickly iterate over designs of my classroom dashboard. As you can see in the panel on the right, the data is laid out such that it is totally agnostic about how it is presented in the prototype. Therefore, as a designer, I have the building blocks of the data that will make up the dashboard already in place, and that gives me the freedom to use it in the design as I see fit. Further, by using Firebase, I did not have to spend any amount of work at all into actually figuring out how to lay out a proper database in order to implement a "real" solution -- I could just use it to simulate the data that the interface needed to display!

For next week, I hope to have gone two rounds of user testing with classroom teachers so that I can iterate on the next version of the classroom design.






