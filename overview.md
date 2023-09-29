---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: "Overview"
layout: single
classes: wide
---

## Class Description

Welcome to CSE 211: Compiler Design! In this class we will explore one of the most import tools in computer science: the compiler. In particular, we will explore how compiler techniques transform high level languages into low-level languages, i.e. closer to the instructions that processors can actually execute. We will study how compilers can automatically make code more efficient and safe on modern processors. When you leave this class you should be comfortable with: specifying programming language grammars, performing flow analysis on intermediate languages, and understanding advanced optimization techniques, such as automatically transforming sequential code into parallel code. 

Given the influx in domain-specific languages, and the explosion of architectural diversity occuring in computing today, these are valuable skills.

## Required Background

This class has a prerequisite of an introductory compiler course. However, because this is a graduate course, we will have students from many different undergrad programs. It is difficult to rely on very specific backgrounds. Because of this, I have been lenient with prerequisites and I hope we can cover a variety of topics that are interesting and accessible to everyone.

Because this is a graduate level class, I do expect a general strong CS foundation. In particular, you should be:

- comfortable using a linux command-line (this is how your assignments will be submitted).
- programming in a high-level language (e.g. Python)
- programming in a low-level language (e.g. C)
- a high-level understanding of basic parsing (i.e. regular expressions and context-free grammars)
- a high-level understanding computer architecture, (i.e. basic processor design and how ISA instructions are executed)

## Class Modules

This class will be split into 5 modules, each of which are roughly two weeks. The first two modules will follow a typical course structure. The third will start to transition into more of a reading group structure where we discuss important papers in the area.

* **Module 1: Parsing Overview:** We will discuss the components of a parser: including tokenizing, grammar specification, and parser generators. 

* **Module 2: Analysis and Optimization:** We will discuss different optimizations and flow analysis (aka static analysis). This includes AST traversals, SSA form, and applications such as finding potential uses of uninitialized variables. 

* **Module 3:  Parallelization and DSLs:** We will discuss how compilers can be used to transform sequential code blocks into equivalent forms that can be executed in parallel. We will explore domain specific languages that further facilitate this automatic translation. 

* **Module 4: Advanced Topics:** We will read impactful papers in the area and discuss them. We will adjust based on class interest, but topics may include optimization evaluation and synthesis.

* **Module 5: Final Project Presentation and Guest Lecture:** The last few classes will have presentations from final projects and a guest lecture (if there is time).

## Class Format

Each class is 65 minutes. I plan to stay after class for roughly 10 minutes to answer questions. 

_Non-protected materials_ will be hosted on this website. This includes the schedule, lecture slides, and references, etc.

_Protected materials_ will be hosted on a Canvas website that you will need your university credentials to access. These materials include homeworks, lecture recordings, tests, grades, etc.

We plan to host a class forum, likely in Piazza. If you organize other forums outside of the class Piazza, please adhere to academic integrity.

_A few classes will be asynchronous due to travel, see the schedule. I will provide Zoom links on Canvas_

## Discussion

Each class will start with a set of discussion points. Please come prepared to partipate. This is often the most exciting part of class and I hope it can continue to be!

## Accessibility

UC Santa Cruz is committed to creating an academic environment that supports its diverse student body. If you are a student with a disability who requires accommodations to achieve equal access in this course, please submit your Accommodation Authorization Letter from the Disability Resource Center (DRC) to me by email, preferably within the first two weeks of the quarter. I would also like us to discuss ways we can ensure your full participation in the course. I encourage all students who may benefit from learning more about DRC services to contact DRC by phone at 831-459-2089 or by email at drc@ucsc.edu.

## Office Hours:

I will provide 2 office hours per week: the time will be set soon.

My office hours can be remote or in-person. My physical office is E2-233 (I finally got a nameplate!). I will provide a Zoom link on canvas. I manage the office hours through a Google doc sign-up sheet. I will reset the list around noon on Wednesday and notify with a canvas announcement. Any name on the list before then will be erased.

Please sign up for only 1 slot at a time. If there is no other student waiting at the end of your slot, you are welcome to stay. If you want to discuss an issue that you think others might also be interested in, please add the issue to the spreadsheet. If you see your issue listed, please add your name and we add more people to the discussion. 

The sign-up sheet is meant to provide fairness; as such I will be strict about keeping to the schedule. Please forgive any abruptness.

## TA:

We have one TA this quarter: [Rithik Sharma](https://sharmarithik.github.io/rithiksharma/). He will help with grading, office hours, and the overall wellbeing of the class. Please meet with him!

Office hours: TBD

## Asynchronous Communication

For any questions outside of office hours: Please post to the class forum (Piazza). If these are sensitive questions, please make the post private. If it is more general, make it visible to the rest of class. If it isn't clear if it is a sensitive question or not, please start out by making the question private and I will advise on making it public or not. Feel free to answer questions that your classmates post or freely participate in discussions there!

Please do not message me directly about class issues. Those emails get buried and you may not get a response.

I will strive to reply to homework questions and discussions within 24 hours. Do not plan on, or expect help, outside of regular business hours (after 5 pm or weekends)

## Homework:

There will be four assignments corresponding to each module.

I will host a docker container that includes the necessary environment (compilers, libraries) for the homeworks. You are free to run this docker from your local machine. It is required that your homeworks execute successfully inside the docker. The homeworks will also specify a submission format (e.g. a directory structure). Please strictly adhere to this, as it helps with grading.

Homeworks are due at midnight on their due date, but do not plan on help after 5 pm (as mentioned above). Homework will be submitted on canvas.

Please help each other with infastructure questions! I cannot help you with anything outside of emacs and the command line! Many people like to use VSCode or PyCharm but I do not know these frameworks and I cannot officially support them for the homework/grading. 

## Tests:

There will be two synchronous tests in this course: a midterm and a final. The midterm will roughly be worth as much as a single homework assignment (~10%). The final will be worth 30%.

The midterm will be given halfway through the class: TODO

The final will be given on TODO

You are allowed up to 3 pages of notes for both tests

## Late Policy:

There are no late assignments excepted. Please get things done early if you are worried about time. 

## Paper Assignment

Scientific literacy is a key skill that every grad student should learn. Towards that goal, this class will require two paper assignments. This consists of finding a conference or journal paper that has a strong compiler component and writing a short review for the paper. 

The review should roughly be 4 pages double spaced. Please organize it as follows:

- **Motivation:** what is the problem and why is it important?
- **Compiler component:** what is the compiler component and how does it relate to what we have learned?
- **Illustrative example:** find a small example that you can clearly explain, especially related to the compiler component. This might be a small program and a description of how the compiler transforms the program.
- **Key results:** what are the important results of this paper and how did the compiler enable them?

Please pre-approve the paper with me. Additionally, I can suggest papers. You will need to have your paper approved two weeks before the quarter ends. The report will be due on the day of the final. Dates for the paper assignment are summarized [here](schedule.html#paper-assignments-and-final-projects).

A list of papers can be found [here](https://docs.google.com/spreadsheets/d/1C5zMXC_RC94EmgmJVOliwYLylEyDUmK9KCO8oixaC3k/edit?usp=sharing). Please feel free to propose new papers. Even if you select from the list, you will still need to get the paper approved. 

## Final Project

You can substitute the final exam for a final project. The project will need to be pre-approved by me no later than 2 weeks before the end of the semester (preferably earlier). To propose a project, please write a two or three paragraphs clearly describing the compiler element to the project and how it relates to what we are learning. 

You will need to get your project approved two weeks before the last day of class. Because of that, you will need to submit your proposal at least 2 days before then. However, I encourage you to discuss your final project ideas with me starting as early as possible.

Your final project deliverable will be a 5 page double spaced report detailing your project with an emphasis on the compiler aspects of your project. Think of it like a mini conference paper, with a required "compiler design and implementation" section. I expect this section will be roughly 2 pages of your report. You will also be required to give a 15 minute presentation about your final project on the last day of class. Dates for the final project are summarized [here](schedule.html#paper-assignments-and-final-projects).

Instead of the paper, if you'd like to publicly show off your project, you can instead choose to submit a website report (in markdown). I will host the projects on the website and brag about them on twitter :) It is completely optional to host your final project publicly, but if you do not host your project publicly then you will need to submit a pdf report (i.e. the website report is not available). 

You can see some examples of final projects [here](https://sorensenucsc.github.io/CSE211-fa2022/projects.html).

If you are a PhD student, I strongly recommend thinking about a final project related to your thesis.


## Grade Breakdown

- Homeworks: 40% (10% each)
- Paper Assignment: 20% (10% each)
- Midterm: 10%
- Final Exam or Project: 30%

If you want to discuss a grade, please contact me no later than 1 week after the grades are posted.

## Academic Integrity

One of the joys of university life is socializing and working with your classmates. I want you to make friends with each other and discuss the material. 

**That said, I expect all assignments (code, write-ups, and tests) to be your own original work.**

If you work together with a classmate on an assignment, please mention this, e.g. in the comments of your code. If you use a figure you didn't create in a write-up, then it needs a citation. Please review the [universities policy on plagiarism](https://guides.library.ucsc.edu/citesources/plagiarism)

This class has a zero tolerance policy on cheating. Please don't do it. I would much rather get a hundred emails asking for help than have to refer anyone for academic misconduct.

## COVID Policy

COVID continues to effect us in many ways. This quarter will surely have challenges related to this. I imagine people will continue to get sick, whether it is us, or people that we love. I hope we can all approach our interactions with empathy and understanding. I will do my best to accommodate the various individual challenges that may arise. Please communicate with me early and often! 

Currently, this is designated as an _in-person_ class. It is **not** a hybrid class. As explained in the [attendance](#attendance) section, I do expect you to plan on primarily attending in person. If you cannot attend in person for reasons related to COVID (e.g. if you or someone close to you gets sick), let me ASAP to discuss accommodations. You will not lose attendance points in these cases and I will do my best to provide lecture materials to you.

If I am unable to attend (e.g. if I get COVID), then I will aim to teach remotely as long as I am feeling well enough.

## Related Seminar

Lindsey Kuper and I are co-organizing the [Language, Systems, and Data (LSD) seminar](https://lsd-ucsc.github.io/lsd-seminar/2022fa/). I highly recommend attending that course (either for credit or for personal interest). The seminar will be hybrid: if you would like to join in person, we are planning on meeting in room E2-398. If you would like to join remote, let me know and I can get you zoom links.

## Privacy

We may need to have remote lectures in case enough of us get sick. I plan to record in-person lectures as well. You should be aware that:

- Things you do or say will be recorded. I doubt that this will be an issue, but if you want me to remove any part of the recording, please just let me know.
- Many forums (e.g. zoom chats, Piazza posts, etc.) chats are not private. Please be respectful and kind and assume everyone can see what you are typing.

## Acknowledgements

This page is based off of Professor [Lindsey Kuper](https://users.soe.ucsc.edu/~lkuper/)'s CSE232, Fall 2020 website
