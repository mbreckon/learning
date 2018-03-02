
## The Dehumamisation of Agile and Objects - Jim Coplien
[YouTube Link](https://youtu.be/ZrBQmIDdls4)

With many talks from industry veterans over the years, I've found that you often miss a huge amount on first hearing. You often aren't even in the same contextual ballpark as the one in which they are arguing their points. Sometimes the points they make seem shocking, or slightly crazy. They come across as a raving old fool. Yet I have learnt some of the most important things from these so called raving old fools. Tom Gilb especially - someone who won't let you get away with sloppy thinking, who has spent a lifetime thinking about the process of building systems and has got the sort of clarity of thinking and approach that can only arise from that effort.

I think this talk fits in that category. There are many things I have glimpsed about object design, through my exposure to Yegor and Dave West, to see that there is something different to the class-oriented design as practised by the majority of software engineers using the "object-oriented languages" of Java, C#, C++ etc. Yet, there are many comments and observations from Jim Coplien, that seem baffling and missing most of the context required to understand truly where he is coming from. 

It is only possible to hint at deeper things in a talk of this length to an audience to whom at least some level of shared context must be built from scratch.

**Quotes**
* **"The interface is the product"** - Jef Raskin
* **"Product owners should have UX experience"**
* **"The machine should be thinking what the user is thinking"** I take this to be that the mental model of the user should be directly represented in the computer. That OO thinking has this at it's core. It is fundamentally tied with UX. 
* **"OO is behavioural psychology"** - this follows from the obsevation that OO thinking is about users' mental models

**Things that need to be considered further**
* **"Microservices could be kind of right except everyone is looking at the wrong end"** - offerred up without much further explanation.
* **"TDD will kill you"** - referencing coupling and cohesion (see Abrahamsson's studies). The implication here is that TDD forces you to do bottom-up design and as classes don't "run" you end up testing methods. This presumes a particular type of TDD of course but certainly one that is widely practiced and espoused by the likes of Bob Martin. 
* A discussion in the questions at the end seemed to suggest that in your domain model you would typically have classes but that you need something more to represent use cases. And it is use cases that we sell as software engineers.
* **"Polymorphism is GOTO's on steroids"** As part of the discussion about object graphs and use cases he seems to espouse this view without much further explanation, seeming to go as far as to say that encapsulation isn't a thing in object thinking either. 
* **"We TDD because we can't understand our code** - this idea that if you have the right language to describe your use cases you will be able to understand your code in such a way that 
* **"Most people don't understand MVC. Controllers aren't the only place where input goes to. Controllers are creators and coordinators of views"** - Until I read Trygve's original paper it is fair to say I thought I understood MVC but clearly didn't. With Jim's explanation I felt there was further to go. He knows Trygve (is creating a language with him) so should know what he is talking about. This again hints that I need to go back to the paper and re-read it keeping that view of controllers more firmly in mind. 

**Stuff to research**
* OOPSLA - the conference that in the late 1980s and early 1990s drove a lot of the innovation in OOP. 
* C. Alexander's 1977 book "A pattern language"
* Jim Coplien himself wrote some papers on Organisational Patterns (at Bell Labs) that later fed into the Scrum process.
* "The New New Product Development Guide" was one of the building blocks on which Scrum was built
* Reminder to look up CRC cards again
* Alan Kay's paper "A personal computer for children of all ages"
* Abrahamsson's emprical studies into TDD
