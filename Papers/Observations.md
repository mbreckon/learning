# Observations
* [Some Patterns for Software Architectures](#shaw96-mary-shaw-some-patterns-for-software-architectures-pattern-languages-of-program-design-vol-2-addison-wesley-1996-pp-255-269)
* [A Laboratory For Teaching Object-Oriented Thinking](#beckcham89-kent-beck--ward-cunningham-a-laboratory-for-teaching-object-oriented-thinking-oopsla89-conference-proceedings-october-1989)
* [Object-Oriented Programming: An Objective Sense of Style](#liebetal88-object-oriented-programming-an-objective-sense-of-style-oopsla88-conference-proceedings-september-1988)

## [SHAW96] Mary Shaw. Some Patterns for Software Architectures, Pattern Languages of Program Design, Vol 2, Addison-Wesley, 1996. pp 255-269

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


## [BECK/CHAM89] Kent Beck & Ward Cunningham. A Laboratory For Teaching Object-Oriented Thinking, OOPSLA'89 Conference Proceedings, October 1989. 

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

## [LIEBetal88] Object-Oriented Programming: An Objective Sense of Style, OOPSLA'88 Conference Proceedings, September 1988.

**Key Points** 

The central claim appears to be...

If you **simultaneously minimise**:
1. Code duplication
2. Number of method arguments
3. Number of methods per class

**...whilst following the Law of Demeter**... 

You will see...
1. Less coupling between methods
2. Better information hiding
3. Narrower interfaces
4. Methods that are easier to re-use
5. Easier correctness proofs using structural induction
6. Easier software maintenance

... More to come here...

**Things to look into in more depth**

* What is a "correctness proof using structural induction"? 

## [COPLIEN94] Borland Software Craftsmanship: A New Look at Process, Quality and Productivity

**Key Points**

Organisational

* "Quality assurance and project management roles were central to the development sociology, in constrast to the developer-centric software production most often observed in our studes of AT&T telecommunications software"
* The team started off as four core developers who spent six months prototyping and building a stable core product. They were then joined by others up to a total of eight.
* The core team were brought together because of their recognised expertise in domains central to the project: spreadsheet engines, graphics, databases etc. 
* "The methodology was iterative. Modulo the architectural dialogue, the core developers worked independently."
* "Early code can be viewed as a series of prototypes that led to architectural decisions, and drove the overall structure of the final system"
* The analysis of the organisation was carried out using the same analysis as you would perform in understanding an OO design - specifically CRC cards. There is a reference here to the "class" part being commonly referred to as "role". They used the analysis to build a process graph.
* The process had a higher communication saturation than most (89%) of processes they'd looked at. They also mention it having some of the highest "coupling per role". "This is a small, intensely interactive organisation".
* "There is a more even distribution of effort across roles than in most other processes we've looked at". "Most other processes comprise more roles that are loosely coupled to the process than we find in QPW". They offer some possible reasons for this. 
* Using a simplistic measure of productivity - lines of code - this team produced a million lines in 31 months excluding code for prototypes. This results in something around 1000 lines per person per week. This is one or two orders of magnitude larger than is observed across industry. 
* "There will always be debate about how much of the phenomenal productivity of QPW owes to its culture, how much to its choice of staff and how much to other factors"
* "Do one thing and do it well". Applies to functions, objects and perhaps to team roles too. They observe that this is how the group is organised - one person for databases, one person for human interfaces etc. "... they are not expected to take responsibility for domains not related to their specialisation. Instead of working in these domains, they work with these domains. One good example is documentation". This seems to apply to internal documentation as much as external documentation.

Development 
* "In spite of the intense meeting-oriented development culture the project built around its architectural development, class implementations were fleshed out in private. Individuals were trusted with doing a good job of implementation: after all, project members were acknowledged experts in their domains. Code reviews were rare. The trust engendered by this domain expertise made it possible to focus meetings on system-level issues"

* "Three project principles worth noting about the QPW organisation's communication architecture" (this section is mostly quoted verbatim)
   1. Meetings are not a bad thing. 
      Project communication, a shared vision, and meetings are important and productive if meetings are properly conducted.
   2. Development takes place on two levels: architecture and implementation
      There is an architectural thread and a development thread, both ongoing, and they interact with each other strongly. These interactions were discussed at daily meetings. 
   3. The development interaction style is a good match for the implementation technology the group had selected. 
      **Object-oriented development leads to abstractions whose identity and structure are largely consistent across analysis, design and implementation.**
      Mapping C++ classes and people close together made it possible for developers to reason about the implementation off-line, away from meetings that dealt with interface issues

* The commonly presumed model is that the object paradigm "makes it possible for an individual to own a class, interface and all, with a minimum of interaction with other class owners in the organisation". This is not how it worked - interfaces were discussed as a group, class implementations built individually. As the implementation fed back into the interface, the impact was discussed as a group, which would in turn lead to changes in implementations of other collaborating classes. 
    **"It should be emphasised that classes are good at hiding implementation ... but they are not good at reducing the ripple effect of interface changes. In fact, because interactions in OO systems form an intricate graph, and interactions in structured procedural systems usually form a tree, the ripple effect of interface changes in an OO system can be worse than in a block-structured procedural design**

Process
* Roles were clear without being formally defined. "The organisation knew itself well, and was conscious of how people interacted with each other at an abstract level". 
* In CMM Level 3 organisations should become self-directing. "Borland clearly appears to be in this latter category - though it may not register a Level 3 rating according to commonly accepted criteria"

Observations
* The resulting collaboration graph looks visually quite cluttered (something I find annoying as someone who likes data viz), but this hints at another of Jim Coplien's points that objects have to be coupled to other objects in order to get anything done. This perhaps means that the study of a system of objects could almost be described as "sociology" rather than debugging :-)
* It is interesting to contrast the views on specialisation with the "full stack" developer mindset that appears to have evolved over the past number of years into the "DevOps" thing. I vaguely recall Jim Coplien making comments about "DevOps" at some point. Perhaps there is a connection, or perhaps his views have evolved too.
* There is some suggestion in section 7, that it is the incredible productivity of the team that enables iterative development to take place. One wonders what would happen without that in such an iterative approach. 
* I see many people trying to get the benefits of this approach without the strong object-oriented design understanding. The points in section 7 seem to be critical to our understanding of how this interaction model worked. What happens when the design is not object-oriented? Reasoning in isolation in the manner described is likely not possible? What is the impact of that on the rest of the communication? 
* It is interesting to observe the mapping of OO concepts onto an organisational structure that feels different to modern approaches. Have we lost something? 
* The idea that interface changes in an OO design might cause wider ripples is fascinating - we often structure our "OO" designs to minimise these changes - almost certainly that is the wrong approach... how tied together is the organisational structure with OO design? Perhaps that is a factor in poorly designed systems and slow development schedules? 
* The management had an internal delivery schedule and an external one that was kept from the developers. They also expected a classic test and fix cycle - something that has again become viewed as not necessary due to TDD and other approaches (how true this is remains to be seen)
* There are comments about having a "documentation team". That triggered a thought - imagine how much an apprentice or a graduate might pick up about software design by simply sitting in on the daily design meetings and recording and distributing the resulting system diagrams for the next day. 

**Things to look into in more depth**
* Can you do OO design cleanly and efficiently using other development models? (they seem tightly integrated here)
