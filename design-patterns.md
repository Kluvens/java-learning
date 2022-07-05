# Design patterns

Design patterns categories
- behavioural patterns
- structural patterns
- creational patterns

## Strategy pattern
Strategy pattern: uses, benefits, liabilities
- applicability
    - many related classes differ in their behaviour
    - a context class can benefit from different variants of an algorithm
    - a class difines maany behaviours, and these apeears as multiple conditional statements. Instead, move each conditional branch into their own concrete strategy class.
- benefits
    - uses composition over inheritence which allows better decoupling between the behaviour and context class that uses the behaviour
- drawbacks
    - increases the number of objects
    - client must be aware of different strategies

## State pattern
State machine: terminology
- a state is a description of the status of a system that is waiting to execute a transition
- a transition is a set of actions to be executed when a condition is fulfilled or when an event is received
- identical stimuli trigger different actions depending on the current state

Important information:
- the state pattern allows an object to have many different behaviours that are based on its internal state
- unlike a procedural state machine, the state pattern represents state as a full-blown class
- the context gets its behaviour by delegating to the current state object it is composed with
- by encapsulating each state into a class, we localize any changes that will need to be made
- the state and strategy patterns have the same class diagram, but they differ in intent
- strategy pattern typically configures context classes with a behavior or algorithm
- state pattern allows a context to change its behavior as the state of the context changes
- state transitions can be controlled by the state classes or by the context class
- using the state pattern will typically result in a greater number of classes in your design
- state classes may be shared among context instances

## Observer pattern
The observer pattern is used to implement distributed event handling systems, in "event driven" programming

In the observer pattern:
- an object, called the subject(or observable or publisher), maintains a list of its dependents, called observers(or subscribers)
- and notifies the observers automatically of any state changes in the subject, usually by calling one of their methods

The ovserver pattern defines a one-to-many dependency between objects so that when one object(subject) changes state, all of its dependents(observers) are notified and updated automatically

The aim should be to,
- define a one-to-many dependency between objects without making the objects tightly coupled
- automatically notify/update an open-ended number of observers(dependent objects) when the subject changes state
- be able to dynamically add and remove observers
