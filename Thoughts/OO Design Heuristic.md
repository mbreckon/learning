# Object-Oriented Design Heuristic

1. Everywhere you see a "get", replace it with "I_am_grabbing_your_\<insert property name>" and everywhere you see a "set" with "I_am_replacing_your_\<insert property name>"
      e.g. (a bit hypothetical - needs replacing with a real example_
      
      ```
      var name = user.getName();
      var userName = name = "User : " + name;
      user.setName(userName);
     
 ... becomes ...
 
      ```
      var name equals "hey user, I am grabbing your name"
      "hey user, I am replacing your name" with string "User : " plus name
      
2. Read it aloud. Preferably role playing the different objects with another person -iIf not just different voices will do :-)
3. If it doesn't sound like something that makes any sense in real life or if you are doing all the work/talking then you've almost certainly got the design wrong

## Speculation
Why does the acting or roleplaying help? I'm not really sure but I wonder if there is something to do with an alignment between object thinking and our natural ability to cope with the world through the delegation of responsibility for details to others (i.e. collaboration). Those boundaries form naturally around specialisations and some vague concept of minimising information. This activity  we subconciously perform every day is utilised in object thinking to produce an essentially human way of designing systems. By acting and speaking the roles and collaborators we are utulising our human sensibiities to design systems. Why would we do that? Ultimately it is humans who have to maintain these systems and they too can use this inherent capability to reason about the system without understanding how everything is put together. 
