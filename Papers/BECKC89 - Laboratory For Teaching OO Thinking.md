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

* "Responsibilities identify problems to be solved"

* "Searching for just the right words is a valuable use of time while designing"

* At this point the paper only suggests a wider role in software engineering rather than just as a method for **teaching** OO design


** Key points in the technique **
* Use 4" x 6" index cards
* Use physical placement of cards to indicate supervision and close collaboration
* Physical interaction with the cards has real value 
* This is a collaborative/team sport
* Drive the design towards completion using "execution scenarios"
* Role play as the objects
* Picking up cards as each role is assumed can help adopt the anthropomorphic perspective necessary for good OO design
* Only create objects based on current demands - this stops the design taking on complexity prematurely


**Other notes**
* In "Lean Architecture for Agile Software Development, Section 8.6", Coplien and Bjornvig tell the history of CRC cards:
    * Rebecca Wirfs-Brock (who worked in the same company as Ward Cunningham) popularised them through her book "Responsibility-driven design"
    * The concept "class" had been used for other concepts such as abstract classes and subsystems.
    * When Rebecca wrote her second book (Object Oriented Design : Roles, Responsibilites and Collaborations") she wanted to rename "class" to "role". 
    * CRC was too "sticky" so she left the acronym as "CRC" but remonikered the "C" to "Candidate object"
    * Therefore today "CRC" really stands for "Candidate Objects, Responsibilities and Collaborations"

* "One of the **distinguishing features** of object design is that no object is an island. All objects stand in relationship to others, on whom they rely for services and control". I'm not sure I understand why this needed to be pointed out nor what it is distinguishing from.

* It strikes me that there are connections with user story cards here. Object Oriented design and the early XP approaches were part of the same mindset. I wonder whether there are deeper connections. 

* It is interesting to see a responsibility of the Model object in the example being "broadcast change notification". There seems to be a debate in certain places on whether INotifyPropertyChanged should be implemented in Model objects in WPF applications. Certainly there was no hint that this was unexpected from these programmers who are using MVC (in fact they do describe it as "much misunderstood" even in 1988)

* "The need to retain the value of physical interaction points to the need for a new kind of user interface and programming environment as **far beyond** what we have to today as our current systems are beyond the tool-oriented environments of the past.". This reminded me of Bret Victor's dynamicland (although I've yet to spend any time really understanding how it works)

**Things to look into in more depth**
* Why are CRC cards not used? Why do we learn by looking at SOLID, GRASP, pillars of OO and other things? Why don't people like Uncle Bob, who are clearly passionate about trying to correct some of the worst tendancies of procedural thinking being applied to OO, use this technique. What has happened?
    * I glimpsed one possible reason in Micheal Feather's "Working with legacy code" where he hints that the reason CRC cards fell by the wayside was that they were swept up in a movement to combine all the different ways of recording OO designs - something that ultimately became UML. Whilst that might be right, it seems tragic that something that teaches and shapes OO designs would get replaced with something that is used primarily to record design.