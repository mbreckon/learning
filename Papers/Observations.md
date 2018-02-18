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

**Evaluating patterns**
The paper defines a set of sections to describe each pattern: Problem, Context, Solution, Diagram, Significant Variants, Examples. The rest of the papers fills these in for eight different patterns. 

**The Pipeline architectural pattern**
Whilst being aware of this pattern already having worked a little with UNIX systems, I almost had a chance to use this pattern in a real world application the day after I'd read this. The goal of the application changed meaning a different architectural pattern was a better fit but it was interesting to see this in the wild. It is also interesting to see the connection to LINQ, IEnumerable and it's counterpart IObservable.

**The implicit invocation architectural pattern**
I've seen this used for a desktop application that didn't need to be reconfigurable on the fly. The cost associated with losing the ease of reasoning about the system (as stated in the paper "Reasoning about the corectness of the sytem depends very heavily on reasoning about the kinds of events, the collection of components, and their collective effect; this is trickier than reasoning about correctness when the execution order is known") is not worth paying if the system doesn't need to be dynamically reconfigurable. 

**The repository architectural pattern**
Having come across the blackboard version of this pattern in my first ever job, for some reason I had never seen it as a variation of the same pattern as databases and compilers. The control structure varies for each. In "databases" the control structure is defined externally as the calling application makes queries. In "compilers" the control structure is fixed as it queries in a predictable pattern. In "blackboard" the control structure proceeds based on the contents of the data store. 

**The interpreter architectural pattern**
A legacy application I'm working on currently is suffering because the fundamental model of the system changed from one that matched this pattern easily to one where this pattern may have a place but is no longer the fundamental model.

**The main program and subroutines architectural pattern**
RPC is an abstraction on single-threaded procedure calls.

**The layered architectural pattern**
I'm used to the idea of layers but the way in which this is described here hints at a slightly different understanding. I need to dig a bit deeper to see the similarities to how this is typically used today.


#### [BECK/CHAM89] Kent Beck & Ward Cunningham. A Laboratory For Teaching Object-Oriented Thinking, OOPSLA'89 Conference Proceedings, October 1989. 

**Key points**

* An anthropomorphic perspective is **necessary** for object-oriented design. Not "optional", not "a helpful guide" but "necessary". 

* Novices in object-oriented programming struggle with regressing back to the sort of "global knowledge" that is possible in procedural programs. This results in their programs being characterised by "gratuitous global variables", "unncessary pointers", and "inappropriate reliance on the implementation of other objects". 

* Learning OO requires a shift in overall approach. I don't think I'd ever recognised quite how big a shift was necessary. They deliberately chose this approach to differentiate OO design from procedural design, hinting that typically OO design is taught in terms of procedural design. This is still likely to be the case as we start people off with the mechanics of programming in terms of if/while/for etc. In many ways this is like starting teaching people assembler. 

* Procedural designs can be characterised at an abstract level as having...
    1. Processes
    2. Data
    3. Data stores

* OO designs can be characterised (as determined by Beck and Cunningham) at an abstract level as having... 
    1. Class name
    2. Responsibilities
    3. Collaborators

... More to come here...

**Things to look into in more depth**

* Why are CRC cards not used? Why do we learn by looking at SOLID, GRASP, pillars of OO and other things? Why don't people like Uncle Bob, who are clearly passionate about trying to correct some of the worst tendancies of procedural thinking being applied to OO, use this technique. What has happened?

