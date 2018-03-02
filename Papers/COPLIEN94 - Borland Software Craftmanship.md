## [COPLIEN94] Borland Software Craftsmanship: A New Look at Process, Quality and Productivity

**Key Points**

Summary (these are mine rather than the direct conclusions from the paper)
* By daily collaborating on interfaces and individually working on implementations a group can keep a coherent OO design
* Using a small team and prototyping allows a stable core to be developed before expanding the team
* The impact of changing interfaces in an OO system is **expected** to be worse than in a procedural one
* As anthropomorphism is at the core of object thinking (see CRC cards) then these techniques can be used to analyse organisations
* There is some (perhaps worrying for most orgs) indication that this form of iterative development requires experienced and very productive individuals (rather than it arising from the approach itself)

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
