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

**Other notes**
* In "Lean Architecture for Agile Software Development, Section 8.6", Coplien and Bjornvig tell the history of CRC cards:
    * Rebecca Wirfs-Brock (who worked in the same company as Ward Cunningham) popularised them through her book "Responsibility-driven design"
    * The concept "class" had been used for other concepts such as abstract classes and subsystems.
    * When Rebecca wrote her second book (Object Oriented Design : Roles, Responsibilites and Collaborations") she wanted to rename "class" to "role". 
    * CRC was too "sticky" so she left the acronym as "CRC" but remonikered the "C" to "Candidate object"
    * Therefore today "CRC" really stands for "Candidate Objects, Responsibilities and Collaborations"

**Things to look into in more depth**
* Why are CRC cards not used? Why do we learn by looking at SOLID, GRASP, pillars of OO and other things? Why don't people like Uncle Bob, who are clearly passionate about trying to correct some of the worst tendancies of procedural thinking being applied to OO, use this technique. What has happened?
    * I glimpsed one possible reason in Micheal Feather's "Working with legacy code" where he hints that the reason CRC cards fell by the wayside was that they were swept up in a movement to combine all the different ways of recording OO designs - something that ultimately became UML. Whilst that might be right, it seems tragic that something that teaches and shapes OO designs would get replaced with something that is used primarily to record design.