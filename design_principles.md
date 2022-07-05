# Design Principles
**Building Good Software is all about:**
1. making sure your software does what the custormer wants it to do - use-case diagram, feature list, prioritise them
2. applying OO design principles to:
    1. to ensure the system is flexible and extensible to accomodate changes in requirements
    2. to strive for a maintainable, reusable, extensible design
3. a change in requirements sometimes reveals problems with your system that you did not even know that they existed
4. remember change is constant and your system should continually improve when you add these changes... else software rots

## Design smells
A design smell
- is a symptom of poor design
- often caused by violation of key design principles
- has structures in software that suggest refactoring

Design smells:
1. rigidity
    - tendency of the software being too difficult to change even in simple ways
    - a single change causes a cascade of changes to other dependent modules
2. fragility
    - tendency of the software to break in many places when a single change is made
    - rigidity and fragility complement each other - aim towards minimal impact, when a new feature or change is needed
3. immobility
    - design is hard to reuse
    - design has parts that could be useful to other systems, but the effort needed and risk in  disentangling the system is too high
4. viscosity
    - software viscosity - changes are easier to implement through 'hacks' over 'design preserving methods'
    - environment viscosity - development envrionment is slow and inefficient
5. opacity
    - tendency of a module to be difficult to understand
    - code must be written in a clear and expressive manner
6. needless complexity
    - contains constructs that are not currently useful
    - developers ahead of requirements
7. needless repretition 
    - design contains repeated structures that could potentially be unified under a single abstraction
    - bugs found in repeated units have to be fixed in every repetition

## Good design
Characteristics of good design
- coupling
- cohesion

Good software aims for building a system with loose coupling and high cohesion among its components so that software entities are:
- extensive
- reusable
- maintainable
- understandable
- testable

### Coupling
Coupling:
- is defined as the degree of interdependence between components or classes
- high coupling occurs when one component A depends on the internal workings of another component B and is affected by internal changes to component B
- high coupling leads to a complex system with difficulties in maintainance and extension... eventual software rot
- aim for loosely coupled classes - allows components to be used and modified independently of each other
- but 'zero-coupled' classes are not usable - strking a blance is an art

### Cohesion
Cohesion:
- the degree to whcih all elements of a component or class or module work together as a functional unit
- highly cohesive modules are much easier to maintain and less frequently changed and have higher probability of reusability
- thkink about
    - how well the lines of code in a method or function work together to create a sense of purpose
    - how well do the methods and properties of a class work together to define a class and its purpose
    - how well do the classes fit together to create modules
- just like zero-coupling, do not pull all the responsibility into a single class to avoid low cohesion

## Design principle
What is a design principle: A basic tool or technique that can be applied to designing or writing code to make software more maintainable, flexible and extensible

**SOLID**
- Single responsibility principle: a class should only have a single responsibility
- Open-closed principle: software entities should be open for extension, but closed for modification
- Liskov substitution principle: objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program
- interface segregation principle: many client-specific interface are better than one general-purpose interface
- dependency inversion principle: one should depend upon abstractions, not concretions

When to use design principles:
- design principles help eliminate design smells
- but, don't apply principles when there no design smells
- unconditionally comforming to a principle
- over-conformance leads to the design smell-needless complexity

**The principle of least knowledge (law of demeter) - talk only to your friends**
- classes should know about and interact with as few classes as possible
- reduce the interaction between objects to just a few close friends
- these friends are immediate friends or local objects
- helps us to design loosely coupled systems so that changes to one part of the system does not cascade to other parts of the system
- the principle limits interaction through a set of rules

**The principle of least knowledge (law of demeter) - **
A method in an object should only invoke methods of:
- the object itself
- the object passed in as a parameter to the method
- objects instantiated within the method
- any component objects
- and not those of objects returned by a method

**Principle of Least Knowledge**
- A method M is an object O can call on any other method within O itself
- A method M in an object O can call on any methods of parameters passed to the method M
- A method M can call a method N of antoher object, if that object is instantiated within the method M
- Any method M in an object O can call on any methods of any type of object that is a direct component of O

**LSP(Liskov Substitution principle):**
- if you favour delegation, composition over inheritance, your software will be more flexible, easier to maintain, extend

Rules for method overriding
- the argument list should be exactly the same as that of the overridden method
- the access level cannot be more restrictive than the overridden method's access level
- a method declared final cannot be overriden
- constructors cannot be overriden
- static methods can be defined in the sub-class with the same signature while this is not overriding, as there is no run-time polymorphoism
