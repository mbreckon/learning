#### [SHAW96] Mary Shaw. Some Patterns for Software Architectures, Pattern Languages of Program Design, Vol 2, Addison-Wesley, 1996. pp 255-269

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

