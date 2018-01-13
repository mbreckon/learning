
# Papers
# Introduction
I've recently decided to go back to the original sources on a range of software engineering and CS topics in order to deepen and strengthen my current practice. My current practice has come from a university degree, observing others, reading blog posts and books, and building various pieces of software over the past 25 years.

### Why bother reading all these old papers?

A lot of it comes from a realisation that it is possible to be a perfectly acceptable practicioner - writing clean code, thinking through designs, making sensible architecture choices etc. by reading all the current theories and listening to the latest talks, but to grow you need a strong conceptual model beyond just learnt practice (no matter how broad). Building that conceptual model generally means going beyond your teachers to their teachers. As Kevlin Henney has recently very clearly stated, there is much from the early days of computing that is still relevant. It is a constant surprise to see statements of problems that are still with us today (albeit generally on a different scale). 

### What to expect in this repository

Every week or two I'm going to be looking at a paper - long enough to read, re-read and mull over its contents and implications. Then I'll write a few notes up here. I can't gaurantee they'll be original or even interesting thoughts but if anybody actually ends up reading them then perhaps they'll go and read the original papers for themselves.

## Week 1
[SHAW96] Mary Shaw. Some Patterns for Software Architectures, Pattern Languages of Program Design, Vol 2, Addison-Wesley, 1996. pp 255-269

**Designers use imprecise and informal prose**

This paper actually extends an earlier paper by adding a pattern and filling out the descriptions (noting that Jim Coplien appears to have been an editor on the first paper). It observes that most software designers describe their designs using "box-and-line" diagrams supported by imprecise and informal prose that, almost surprisingly, does manage to communicate with some success. I note that whilst this imprecision and informality still exists I do see references in architecture documents these days to (often only one) patterns described in this paper (albeit without reference to the paper itself). 

**Critical dimensions of architectural patterns**

Four dimensions are identified that allow us differentiate the architectural patterns.

 1. System model (the underlying intuition behind the pattern)
 2. The kinds of component used
 3. The kinds of interactions amongst the components
 4. The control structure used
 
 **Matching architecture to properties of the problem**
 
There is an interesting statement that appears obvious at first reading... "Further, choosing the architecture for a system should include matching characteristics of the architecture to properties of the problem". 

This seems obvious and hardly worth stating, yet in reality I see little matching going on in real world practice:

1. Several of the architectural patterns are applied because "that is how you write applications" or based on familiarity or the last application an engineer worked on. I too have been guilty of this. 
2. The properties of the problem are rarely enumerated and recorded in a way that would allow any systematic matching to occur (e.g. using Tom Gilb's impact estimation tables)
3. When the understanding of the problem evolves the decisions are rarely re-visited.

**Why use patterns?**

There are some useful observations on the advantages of declaring patterns

"To impose an overall structure ... that:"
1. is appropriate to the problem
2. clarifies designers intentions
3. establishes internal consistency
4. maintains internal consistency
5. allows for checking and analysis
6. documents the system for maintainers

