# SOLID - Liskov Substitution Principle

The aim of this is to make some sense of the varied material on LSP and to assess some of the criticism surrounding SOLID. 

## Source material

* Bob Martin - Liskov Substitution Princple http://condor.depaul.edu/dmumaugh/OOT/Design-Principles/lsp.pdf
  * Some thoughts on similarity to Design by Contract
  * Three examples
    1) Simple violation (switching on type in client code to adjust behaviour)
    2) More subtle violation (rectangle/square)
         * note: mutability critical problem
    3) Real world example using sets and persistent sets
* SOLID Deconstructed - Kevlin Henney https://www.youtube.com/watch?v=tMW08JkFrBA
    - Not principles, not universal, at best they are contextual...
    - "If you regard yourself as a competent developer and are still using the SOLID principles you need to start giving them up"
    - Example: (32mins) RecentlyUsedList derived from List< string >
    - Go back to what Barbara Liskov actually wrote...
    - It's not as useful as people expected...
    - It is really strict because it is not about object orientation but particular type relationships. Abstract data-types are not the same thing (39mins)
* Tom Dalling
  https://www.tomdalling.com/blog/software-design/solid-class-design-the-liskov-substitution-principle/
  * Example : Penguin (note: also mutable classes)
* liskov substitution principle violations https://stackoverflow.com/questions/35582996/liskov-substitution-principle-violations
* What is an example of the Liskov Substitution Principle?
https://stackoverflow.com/questions/56860/what-is-an-example-of-the-liskov-substitution-principle/8279878#8279878
* Liskov Substitute Principle (LSP) with Code example https://stackoverflow.com/questions/31154356/liskov-substitute-principle-lsp-with-code-example
* Does Liskov Substitution Principle also apply to classes implementing an interface? https://softwareengineering.stackexchange.com/questions/170925/does-liskov-substitution-principle-also-apply-to-classes-implementing-an-interfa
* LSP vs OCP / Liskov Substitution VS Open Close https://softwareengineering.stackexchange.com/questions/178488/lsp-vs-ocp-liskov-substitution-vs-open-close
* Hidden Liskov Violations https://medium.com/bluebear-tech/hidden-liskov-violations-e607ed528117
* Is Liskov Substitution Principle a practical concept? https://www.quora.com/Is-Liskov-Substitution-Principle-a-practical-concept
* Is this a violation of the Liskov Substitution Principle? https://softwareengineering.stackexchange.com/questions/170138/is-this-a-violation-of-the-liskov-substitution-principle
* Can anyone provide an example of the Liskov Substitution Principle (LSP) using Vehicles? https://stackoverflow.com/questions/20861107/can-anyone-provide-an-example-of-the-liskov-substitution-principle-lsp-using-v
* Does the wrong interface implementation violate Liskov Substitution Principle? https://stackoverflow.com/questions/49310981/does-the-wrong-interface-implementation-violate-liskov-substitution-principle
* A Good Example of Liskov Substitution Principle https://lassala.net/2010/11/04/a-good-example-of-liskov-substitution-principle/
* What can go wrong if the Liskov substitution principle is violated? https://softwareengineering.stackexchange.com/questions/170222/what-can-go-wrong-if-the-liskov-substitution-principle-is-violated
* Liskov Substitution Principle Violation Spotted in the Wild https://www.codelord.net/2010/11/24/liskov-substitution-principle-violation-spotted-in-the-wild/
* What can go wrong if the Liskov substitution principle is violated? https://softwareengineering.stackexchange.com/questions/170222/what-can-go-wrong-if-the-liskov-substitution-principle-is-violated
* Real World - Liskov Substitution Principle https://softwareengineering.stackexchange.com/questions/336759/real-world-liskov-substitution-principle
* Do changes in performance violate the Liskov Substitution Principle? https://softwareengineering.stackexchange.com/questions/186511/do-changes-in-performance-violate-the-liskov-substitution-principle
* Does this Decorator implementation violate the Liskov Substitution Principle? https://softwareengineering.stackexchange.com/questions/240980/does-this-decorator-implementation-violate-the-liskov-substitution-principle