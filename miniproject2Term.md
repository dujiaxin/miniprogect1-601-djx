# Additional Terms in Mini-project 2
definitions and examples of the following terms:

* [How Python uses Indentation to control Flow](#how-python-uses-indentation-to-control-flow)
* [Don't Repeat Yourself](#dont-repeat-yourself) 
* [Design Patterns from Gang of Four](#design-patterns-from-gang-of-four)
* [Class](#class)
* [Object](#object)
* [Static](#static)
* [Property/Attribute](#propertyattribute)
* [Method](#rm)
* [Exception](#history)
* [Unit Test](#tab)
* [Constructor](#arrow)
* [Factory](#arrow)
* [Decorator](#arrow)
* [Extend Class](#arrow)
* [CSV Files](#arrow)
* [Reading Files](#arrow)

## How Python uses Indentation to control Flow

While the concepts of function definitions, loops, and conditional statements are shared across the majority of modern programming languages, the languages often differ in their syntax for delimiting the bodies of these constructs. For example, where C++ uses “curly braces” as delimiters, e.g.:
```cpp
// example showing that C++ uses curly braces to delimit scope
int x = 1;

if (x > 10)
    {
    // we are inside the if-block, as delimited by the curly-brackets
    x = x + 1;
    }
// we are outside of the if-block
x = x + 3;
```
Python uses whitespace (i.e. indentation) to delimit scope:
```python
# example showing that Python uses whitespace to delimit scope
x = 1

if x > 10:
    # we are inside the if-block; this line starts with four blank spaces
    x = x + 1
# we are outside of the if-block; there are no leading whitespace characters
x = x + 3
```
Look to the example at the beginning of this section to see the bodies of the function definition, the for-loop, and the subsequent `if-else` block were all separated by increasing levels of indentation.

Python’s syntax is quite flexible in terms of what it defines as a **whitespace delimiter**. Its rules are that:

One or more whitespace characters (spaces or tabs) is sufficient to serve as indentation.
A given indented block must use a uniform level of indentation. E.g. if the first line of an indented block has two leading spaces, all subsequent lines in that block must lead with exactly two white spaces.
While Python’s syntax is relatively forgiving, I am not: the [standard style](https://www.python.org/dev/peps/pep-0008/#indentation) for indenting in Python is to use four space characters for each level of indentation. It is strongly advised that you adhere to this standard. Most IDEs and consoles (including Jupyter notebooks) will automatically add a four-space indentation for you when you enter into the body of one of the aforementioned constructs.

## Don't Repeat Yourself
**Don't repeat yourself** is a principle of software development aimed at reducing repetition of software patterns, replacing it with abstractions or using data normalization to avoid redundancy.

The **DRY** principle is stated as "Every piece of knowledge must have a single, unambiguous, authoritative representation within a system". When the DRY principle is applied successfully, a modification of any single element of a system does not require a change in other logically unrelated elements. Additionally, elements that are logically related all change predictably and uniformly, and are thus kept in sync. Besides using methods and subroutines in their code, Thomas and Hunt rely on code generators, automatic build systems, and scripting languages to observe the DRY principle across layers.

## Design Patterns from Gang of Four

The Gang of Four are the four authors of the book, "Design Patterns: Elements of Reusable Object-Oriented Software". In this article their twenty-three design patterns are described with links to UML diagrams, source code and real-world examples for each.

### What are Design Patterns?
Design patterns provide solutions to common software design problems. In the case of object-oriented programming, design patterns are generally aimed at solving the problems of object generation and interaction, rather than the larger scale problems of overall software architecture. They give generalised solutions in the form of templates that may be applied to real-world problems.

Design patterns are a powerful tool for software developers. However, they should not be seen as prescriptive specifications for software. It is more important to understand the concepts that design patterns describe, rather than memorising their exact classes, methods and properties. It is also important to apply patterns appropriately. Using the incorrect pattern for a situation or applying a design pattern to a trivial solution can overcomplicate your code and lead to maintainability issues.

### Creational Patterns

The first type of design pattern is the creational pattern. Creational patterns provide ways to instantiate single objects or groups of related objects. There are five such patterns:

#### Abstract Factory. 
The abstract factory pattern is used to provide a client with a set of related or dependant objects. The "family" of objects created by the factory are determined at run-time.

#### Builder. 
The builder pattern is used to create complex objects with constituent parts that must be created in the same order or using a specific algorithm. An external class controls the construction algorithm.

#### Factory Method. 
The factory pattern is used to replace class constructors, abstracting the process of object generation so that the type of the object instantiated can be determined at run-time.

#### Prototype. 
The prototype pattern is used to instantiate a new object by copying all of the properties of an existing object, creating an independent clone. This practise is particularly useful when the construction of a new object is inefficient.

#### Singleton. 
The singleton pattern ensures that only one object of a particular class is ever created. All further references to objects of the singleton class refer to the same underlying instance.

### Structural Patterns
The second type of design pattern is the structural pattern. Structural patterns provide a manner to define relationships between classes or objects.

#### Adapter. 
The adapter pattern is used to provide a link between two otherwise incompatible types by wrapping the "adaptee" with a class that supports the interface required by the client.
#### Bridge. 
The bridge pattern is used to separate the abstract elements of a class from the implementation details, providing the means to replace the implementation details without modifying the abstraction.
#### Composite.
The composite pattern is used to create hierarchical, recursive tree structures of related objects where any element of the structure may be accessed and utilised in a standard manner.
#### Decorator. 
The decorator pattern is used to extend or alter the functionality of objects at run-time by wrapping them in an object of a decorator class. This provides a flexible alternative to using inheritance to modify behaviour.
#### Facade. 
The facade pattern is used to define a simplified interface to a more complex subsystem.
#### Flyweight. 
The flyweight pattern is used to reduce the memory and resource usage for complex models containing many hundreds, thousands or hundreds of thousands of similar objects.
#### Proxy. 
The proxy pattern is used to provide a surrogate or placeholder object, which references an underlying object. The proxy provides the same public interface as the underlying subject class, adding a level of indirection by accepting requests from a client object and passing these to the real subject object as necessary.

### Behavioural Patterns
The final type of design pattern is the behavioural pattern. Behavioural patterns define manners of communication between classes and objects.

#### Chain of Responsibility. 
The chain of responsibility pattern is used to process varied requests, each of which may be dealt with by a different handler.
#### Command. 
The command pattern is used to express a request, including the call to be made and all of its required parameters, in a command object. The command may then be executed immediately or held for later use.
#### Interpreter. 
The interpreter pattern is used to define the grammar for instructions that form part of a language or notation, whilst allowing the grammar to be easily extended.
#### Iterator. 
The iterator pattern is used to provide a standard interface for traversing a collection of items in an aggregate object without the need to understand its underlying structure.
#### Mediator. 
The mediator pattern is used to reduce coupling between classes that communicate with each other. Instead of classes communicating directly, and thus requiring knowledge of their implementation, the classes send messages via a mediator object.
#### Memento. 
The memento pattern is used to capture the current state of an object and store it in such a manner that it can be restored at a later time without breaking the rules of encapsulation.
#### Observer. 
The observer pattern is used to allow an object to publish changes to its state. Other objects subscribe to be immediately notified of any changes.
#### State. 
The state pattern is used to alter the behaviour of an object as its internal state changes. The pattern allows the class for an object to apparently change at run-time.
#### Strategy. 
The strategy pattern is used to create an interchangeable family of algorithms from which the required process is chosen at run-time.
#### Template Method. 
The template method pattern is used to define the basic steps of an algorithm and allow the implementation of the individual steps to be changed.
#### Visitor. 
The visitor pattern is used to separate a relatively complex set of structured data classes from the functionality that may be performed upon the data that they hold.
## Class
A class is an extensible program-code-template for creating objects, providing initial values for state (member variables) and implementations of behavior (member functions or methods).In many languages, the class name is used as the name for the class (the template itself), the name for the default constructor of the class (a subroutine that creates objects), and as the type of objects generated by instantiating the class; these distinct concepts are easily conflated.

Instance attributes are owned by the specific instances of a class. This means for two different instances the instance attributes are usually different. We can also define attributes at the class level. Class attributes are attributes which are owned by the class itself. They will be shared by all the instances of the class. Therefore they have the same value for every instance. We define class attributes outside of all the methods, usually they are placed at the top, right below the class header.
## Object

## Static

## Property / Attribute

## Method

## Exception

## Unit Test

## Constructor

## Factory

## Decorator

## Extend Class

## CSV Files

## Reading Files
