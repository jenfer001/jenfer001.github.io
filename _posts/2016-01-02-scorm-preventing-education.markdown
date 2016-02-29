---
layout: post
title: Does SCORM prevent good education?
author: Mark Gibson
tag: [scorm, tracking]
image: ../img/scorm01.jpg
---
![Alt text](../../../../img/scorm01.jpg)

A couple of weeks ago I went to the Learning and Skills Group Conference in London and attended Megan Bowe’s lecture on the new Tin Can API [1].
The Tin Can API is a new protocol designed to record a student’s learning experiences and is set to replace the current standard, SCORM, which is used to report learner scores to a Learning Mangement System. Tin Can 1.0 was released on 26th April 2013 and was designed to change the way we record education. Megan Bowe is a strategist with Rustici software, the company who was awarded a grant by ADL [2] to develop the Tin Can API specification.
Before getting into “Tin Can - the Experience API”, Megan started her lecture by outlining the limitations of SCORM, a topic I am more than familiar with!

#### Roll Your Own

I have been working with eLearning development and learning management systems for a large part of my career, and when it came time to choose a new LMS a couple of years ago, I was unable to find one that both met our immediate needs and was also flexible enough to develop new features quickly as we needed them. I also took the decision that the license fees which we would pay to a company for a suitable LMS could be better spent on a full-time developer who could build exactly what we needed.
So we decided to build our own.
One of the early design discussions was what role SCORM would play in our new LMS. We quickly came to the decision that all content would be created by our team and we wouldn’t ever be purchasing any off-the-shelf content. We also realised that the SCORM standard severely limited our possibilities with regards to interactivity and didn’t really give us the level of feedback we needed.
So we decided that we wouldn’t use it. So instead we built a SCORM-free LMS that handled rich media and could give the type of feedback we wanted to both to the delegate and the company.

#### What is SCORM?

SCORM stands for the Sharable Content Object Reference Model, and is currently the most widely used e-learning protocol in the world. SCORM content is elearning which can communicate with a SCORM Learning Management System.
If an LMS is compliant with the SCORM standard, then it can play most SCORM content, and most SCORM content can be played in any SCORM-compliant LMS. This interoperability allows for good communications between the elearning courses and the LMS so that reports can be produced on how a student is doing.

#### Why is that not good enough?

The problem for most organisations was stated simply by Megan Bowe at the start of her workshop: that there are only four things that SCORM can tell us…

* Completion - did the student finish the course
* Duration - how long did it take them
* Pass/Fail - did they meet the pass mark
* Score - what score did they get

This means that while we can track course completion and report on the score, any learning methodology that isn’t facilitated through testing cannot be tracked or reported on using SCORM. If we want to track education and we do not want to do it manually we need to have a system that supports our education methodology of choice and few educators today think that getting a student to achieve a pass rate in an online course is the only learner interaction that is important. If we are designing a standard for the future we need a means of supporting multiple learning methods across multiple platforms to gain wide adoption.
In education today there are more learning methods we need to support that can’t be tracked with the four basic SCORM functions:

* Blended Learning
* Social learning
* Informal Learning
* Off-line learning
* Team learning
* Adaptive learning
* Simulations
* Serious games
* Mobile applications
* Transitions from device to device

Many of these learning methods our team wanted to support, simulations being the first on the list for me, and specifically using simulations for testing. At the time we had recently completed development of a series of simulations for a customer and had to make them SCORM compliant to host on their LMS. We found it difficult to create effective multi-branching simulations where the user can navigate through an application, with just a pass/fail option to measure a students ability.
The SCORM API supports only the following messages between an learning course and an LMS

* Initialize( “” )
* Terminate( “” )
* GetValue()
* SetValue()
* Commit( “” )
* GetLastError()
* GetErrorString()
* GetDiagnostic()

This essentially means that outside of the communications protocol messages we can only “get” and “set” specific predefined values.
If we look at the available interactions within the standard we can start to see why elearning tests are all the same as we can only support the following:
cmi.interactions.n.type ()
true-false
multi-choice
fill-in
long-fill-in
matching
performance
sequencing
likert
numeric
As educators do we think that these as the only interactions possible are effective, and are these actually effective means of testing?
Additional complaints

SCORM is a very complex format and notoriously difficult to implement. It is a lot of work for LMS vendors to build into their systems and is far too complex for many courseware developers to use. 10 years after the release of SCORM 2004, 75% of all learning is still published at the earlier SCORM 1.2 version. SCORM 2004 had some great improvements over 1.2, like knowing which questions went with which response, but was too complex to fully implement.
It is  difficult to edit the content once published and will need to be re-authored and redeployed.
Shared Content Objects are not so easily “sharable”, so if the same content is to used in more than one course you need to have multiple copies of the files.
As SCORM needs JavaScript in a web browser to function so it is Inherently insecure and relatively easy to hack, someone with a simple script can trick an LMS into thinking that a course has been completed.
SCORM stores the learning interaction data, including the answers, in the web browser cache.

#### Summary

A browser only technology gives severe limitations to today’s student in an interconnected world. Multiple platforms, new learning methods, a greater realisation of the importance of informal learning, social learning and the growth of gamification means we need a simpler more flexible platform to support education into the 21st century
Is the new Tin Can standard the answer to these problems? I’ll cover that in my next article.

#### Further Reading

* Rustici Software’s [page](http://tincanapi.com/scorm-vs-the-tin-can-api/) on SCORM vs Tin Can
* Why SCORM 2004 Failed & what that means for [Tin Can 3](http://www.efrontlearning.net/blog/2013/04/why-scorm-2004-failed-what-that-means-for-tin-can.html)
* Rustici SCORM Stats: Then and Now [article](http://scorm.com/blog/2011/08/scorm-stats-then-and-now/)
* Rustici SCORM Stats [article](http://scorm.com/scorm-stats/)

---
<div class="post-meta">
<br />
<ol>
<li>An API is an application programming interface which allows computer applications to communicate with each other.  ↩</li>
<li>Advanced Distributed Learning (ADL) is the product of the ADL Initiative, established in 1997 by the “US Department of Defense (DoD) Office of the Under Secretary of Defense for Personnel and Readiness” (OUSD P&R) to standardize and modernize training and education management and delivery</li>
</div>