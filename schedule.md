---
layout: single
classes: wide
---

_Slides will be uploaded the day after class_

_Schedule is tentative and topics may change depending on interest and discussions_

### Module 1: Parsing Overview/Refresher

| Date             | Topic                                | Slides                 |   Reading       |  Notes 
|------------------|--------------------------------------|------------------------|-----------------|-
| Fri, Sept. 28    |  introduction                        |                        | EAC Chapter 1   | 
| Mon, Oct. 2      |  tokenizing                          |                        | EAC Chapter 2   |
| Wed, Oct. 4      |  parsing                             |                        | EAC Chapter 2   |
| Fri, Oct. 6      |  parse trees                         |                        | EAC Chapter 3   | 
| Mon, Oct. 9      |  Abstract syntax trees               |                        | EAC Chapter 5.1 | 
| Wed, Oct. 11     |  parser generators                   |                        | [PLY docs](https://www.dabeaz.com/ply/)                | homework 1 assigned
| Fri, Oct. 13     |  parsing with derivatives            |                        | parsing with derivatives [paper](https://www.ccs.neu.edu/home/turon/re-deriv.pdf) (first 7 pages) |
| Mon, Oct. 16     |  symbol tables                       |                        | slides          |



### Module 2: Analysis and optimization

_dates will be modified to adjust for extra time spent on earlier modules._

| Date             | Topic                              | Slides | Reading                                   | Notes
|------------------|------------------------------------|--------|-------------------------------------------|-
| Wed, Oct. 18     | local value numbering 1            |        | EAC Chapter 8 (up to 8.5)                 | 
| Fri, Oct. 20     | local value numbering 2            |        |                                           |
| Mon, Oct. 23     | regional optimizations             |        | EAC Chapter 8.5 and Chapter 9 (up to 9.3) | 
| Wed, Oct. 25     | global optimizations 1             |        |                                           | homework 1 due. homework 2 assigned
| Fri, Oct. 27     | global optimizations 2             |        |                                           | 
| Mon, Oct. 30     | MIDTERM                            |        |                                           |
| Wed, Nov. 1      | static single-assignment SSA) form |        | EAC Chapter 9.3 (through end)             | 
| Fri, Nov. 3      | SSA optimizations 1                |        | EAC Chapter 9.3 - 9.5                     | 
| Mon, Nov. 6      | SSA optimizations 2                |        | EAC Chapter 9.3 - 9.5                     | 


### Module 3: Parallelization and DSLs

| Date             | Topic    | Slides |  Readings | Notes
|------------------|----------|--------|----------------|-
| Thurs, Oct. 27   | Instruction level parallelism |  [slides](lectures/CSE211Oct27_fa2022.pdf) | slides
| Tues, Nov. 1     | parallel for loops                       |   [slides](lectures/CSE211Nov1_fa2022.pdf)    | slides | 
| Thurs, Nov. 3    | implementing parallel for loops           |    [slides](lectures/CSE211Nov3_fa2022.pdf)                | slides |
| Tues, Nov. 8     | parallel loop restructuring and Halide        |  [slides](lectures/CSE211Nov8_fa2022.pdf)                  | [Halide](http://people.csail.mit.edu/jrk/halide-pldi13.pdf) | Homework 3 assigned (Nov. 7) |  
| Thurs, Nov. 10     | Halide          |    [slides](lectures/CSE211Nov10_fa2022.pdf)                  | slides |  
| Tues, Nov. 15    | graph DSLs                                   |   [slides](lectures/irgl.pdf)                 | [irgl](https://cs.rochester.edu/~sree/papers/sree-oopsla2016.pdf)       | 
| Thurs, Nov. 17   | compiling relaxed memory models        |      [slides](lectures/CSE211Nov17_fa2022.pdf)                 | slides| 
| Tues, Nov. 22   | decoupled access/execute        |   [slides](lectures/CSE211Nov22_fa2022.pdf)                   | [DAE paper](https://courses.cs.washington.edu/courses/cse590g/04sp/Smith-1982-Decoupled-Access-Execute-Computer-Architectures.pdf) | 



## Module 4: Advanced topics

| Date             | Topic    | Slides  | Readings | Notes
|------------------|----------|--------|----------------|- 
| Tues. Nov. 29   | guest lecture (TBD)          |      |  | 
| Thurs. Dec. 1   | final project presentations  |      |  | 


## Final


| Date             | Official time    | Provided time | Notes
|------------------|----------|--------|----------------
| Thursday Dec. 8     | 12 - 3 PM    | 8 AM - 8 PM      | Final project report due, paper review due


# Paper Assignments and Final Projects

Please see [here](overview.html#paper-assignment) for an overview of the paper assignment

Please see [here](overview.html#final-project) for a description of the optional final project

## Dates Summary:

Paper/Project proposals submitted (latest possible, preferably earlier): Nov. 15

Paper/Projects need to be approved by Nov. 17

Project presentation should be ready by due Dec. 1

Paper review due Dec. 8

Project report due Dec. 8


## Dates Explained

All paper assignments and final projects must be approved 2 weeks before the last day of class: Nov. 17.

Please make sure you have submitted your proposal by Nov. 15.

For a paper assignment, a proposal is the paper title and a few sentences about why it is interesting for this class. Another option is to ask for a paper. In that case, please provide a few sentences about what you have found interesting in the class so far.

For a final project, it is a two paragraphs describing the compiler element to the project and how it relates to what we are learning. You can submit this on Piazza.

It is not guaranteed that your proposal will be approved! Please submit your proposals as early as possible so that we can ensure they get approved!

For projects: a presentation will be due on Dec 1, so that we can schedule the presentation.

For paper reviews and projects: the report is due the day of the final: Dec. 8.
