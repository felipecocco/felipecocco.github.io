---
layout: post
title:  "Start of Second Semester"
date:   2016-09-19 21:00:00
categories: [jekyll]
tags: [thesis]
---
As I begin the second semester of thesis, the focus now has shifted from exploring possible project ideas to narrowing in on the proposed idea and successfully interating on designs. Over the summer, several features of the core idea where validated, and a key use-case (and the one I have decided to focus) emerged.

Refining the idea
====================


Initially I meant to tackle an assessment problem that I perceived that some schools faced: Despite a growing interest and demand for collaboration amongst students, assessment tools often required students to work individually. By designing a tool which allowed students to take exams in groups, I saw the possibility to reward students for working together to solve problems while at the same time working to correct misconceptions in their mental models.

To that end, I implemented a naive algorithm which took student answers to quizzes in my school's learning management system and created groups (of a size determined by the teacher) seeking to maximize the heterogeneity of student answer vectors -- in other words, it tried as best as it could to make groups with students who had picked different answers to problems. Over the summer, I recruited a HS biology and HS physics teacher to run through an exercise where they did an in-class activity using the method that I had proposed last semester [https://docs.google.com/presentation/d/1cRU6Z460d_untzJcINx8pAJOi7yvKxqG0boYL2vjSJg/edit?usp=sharing]

While the test runs were fine, a few issues quickly emerged. 

The most important issue was that I clearly gravely overestimated the receptivity of this kind of tool for a formal assessment. These two teachers -- as well as the wider group of HS teachers which were polled at a faculty meeting -- seemed incredibly reticent to assign any weight to a group component of an assessment. They (I think rightfully) questioned the legitimacy in giving an actual weight to a group discussion if part of the appeal of separating kids into groups would be that the make-up of the groups would necessarily be different. How could I prevent, for instance, from making it so that the "smart" kid in a group would simply monopolize the discussion and essentially "give" a grade to students who otherwise may not have had strong command of the material?

At the same time, a very different use-case also emerged from those conversations. I had already imagined that grouping students to go over homework problems could be promising, but the teachers seemed pretty convinced that this was a the most compelling use-case. As a designer, thinking outside of a formal assessment situation has many benefits, since it confers a lot more freedom on how to deal with the student and teacher interaction. Whereas in a formal assessment situation it would be extremely important to make sure all students answered all questions all the time, in a formative, non-graded situation, it would be perfectly plausible to just have students revisiting questions for which they necessarily had some difficulty. Needless to say, I was very warm to the idea of exploring this potential use-case and use it to narrow the focus of my project!

... and so we have a new problem!
----------------

According to the National Council of Teachers of Mathematics, 30% of classroom time across middle-school and high-schools is devoted to set-up and going over homework. And, according to the same research, the most common method of going over homework is talking about individual problems, where students request specific problems to go over and the teacher does the problems on the whiteboard.

There are numerous issues with this approach, and it is troubling to learn that it is the dominant way by which teachers give feedback to students on their assignments. 

To begin with, going over homework in this manner is incredibly inefficient. Not only can the teacher only tackle one problem at a time, but it is likely that only a subset of the class can take advantage of his/her explanation. After all, some students will have done the problem correctly, so they may choose not to pay attention -- they will be bored. Then, there will also be a set of students who have more systemic and deeper issues beyond the particular problem being covered, and for those students the quick class-wide explanation will also be insufficient. Therefore, by going over them as a group, the teacher is in all likelihood addressing the needs of only a subset of his/her students.

Also, this kind of review heavily skews the problems that are discussed in favor of students who are more vocal and more eager to volunteer their concerns in the middle of class. Students who are shy or embarassed to ask questions may find that their questions are less likely to be brought up before the class.

Naturally, the question then becomes: If this is such an inefficient method, why is it so popular? The National Council of Mathematics itself mentions that "going over homework can be an activity that helps achieve learning goals because students enter the process already having had an opportunity to engage with problems on their own without a specific time limit. Thus, the discourse can build on that work and do much more than just be a review of answers and a time to reiterate suggested solution strategies." A naive answer would perhaps suggest that teachers are simply unaware of other possbile approaches, and that professional development around this topic could significantly contribute to a change in teacher practice. In reality, however, it is pretty clear to me that the key issue is that this strategy, while perhaps inefficient with respect to student outcomes, is actually very easy for teachers to implement. 

By speaking with one of our teachers who implemented a richer protocol for going over homework, it was clear just how much of an effort that required on his part. First, he collected the answers from students electronically using a custom-made Google Form. He then looked at the student answers the night before and tried to find patterns in their mistakes. On class day, he told students to get in groups that he had selected based on their answers, and asked them to go over the problems as he paced around in class.

If we contrast this with the effort required to simply show up in class and ask students what they should go over, it is no surprise why talking about individual problems as a class is the predominant pattern that is observed.

... and we have a new solution: PeerHW!
---------------

PeerHW is a platform designed ot facilitate the process of going over homework by leveraging a peers in that process. Students input their homework answers in the platform, using it like an answersheet. The platform automatically analyzes the student's answers to separate questions into three categories: Questions that the class should not go over (correct % is really high), questions that the teacher should go over as a class (correct % is really low), and questions that students should answer in groups (correct % is roughly even). Based on student's answers, the platform will suggest how students should be placed into groups so as to maximize the likelihood that they will have meaningful discussions about the problems (guaranteeing that students didn't all answers the problems in exactly the same way, for example). The teacher can then follow along in his dashboard in real-time as students go over and re-submit these problems, and he/she is then free to roam around the classroom to address individual questions.



Where the work is now
---------

Over the summer, I implemented a basic version of the grouping algorithm which simply took a set of answers and created groups of a predetermined size based on student answers. Since the focus then was on more formal asessments, the algorithm took into account all questions instead of simply those that would merit groups discussion, as porposed above. 

With respect to the interface, what is clear is that there are a few core interactions that are unique to this platform, and those are the ones that I am focusing on first. What makes this platform different from other solutions that exist right now is the emphasis on the group element. Therefore, the interactions around communicating group membership and showing group progress are the most important. Below you can see the beginning of a prototype of what the teacher could be seeing as students discuss their homework in groups.

![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Next steps
----------

The platform will necessarily be used by both teachers and students. However, the interaction with teachers is much richer -- they will have to creat assignments, look at results, and administer a "group discussion" session in it, whereas students need only use it to submit their answers. Therefore, I think the focus should be on the teacher side, and especially on aspects of the design that are particular to this solution, such as allowing teachers to move students around in groups, or communicating to teachers what problems should be discussed in a clear way. For the next week, my goal will be to put "classroom" interaction and the "hw summary" interaction in a place where they could be presented to teachers for an interview.






