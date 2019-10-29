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
* [Exception](#Exception)
* [Unit Test](#Unit-Test)
* [Constructor](#Constructor)
* [Factory](#Factory)
* [Decorator](#Decorator)
* [Extend Class](#Extend-Class)
* [CSV Files](#CSV-Files)
* [Reading File](#Reading-File)

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
An object can be a variable, a data structure, a function, or a method, and as such, is a value in memory referenced by an identifier.

In the class-based object-oriented programming paradigm, object refers to a particular instance of a class, where the object can be a combination of variables, functions, and data structures.
## Static
A static variable is a variable that has been allocated "statically", meaning that its lifetime (or "extent") is the entire run of the program. This is in contrast to shorter-lived automatic variables, whose storage is stack allocated and deallocated on the call stack; and in contrast to objects, whose storage is dynamically allocated and deallocated in heap memory.
## Property / Attribute
In python, everything is an object. And every object has attributes and methods or functions. Attributes are described by data variables for example like name, age, height etc.

Properties are special kind of attributes which have getter, setter and delete methods like __get__, __set__ and __delete__ methods.

However, there is a property decorator in Python which provides getter/setter access to an attribute Properties are a special kind of attributes. Basically, when Python encounters the following code:
```python
foo = SomeObject()
print(foo.bar)
```
it looks up bar in foo, and then examines bar to see if it has a __get__, __set__, or __delete__ method and if it does, it's a property. If it is a property, instead of just returning the bar object, it will call the __get__ method and return whatever that method returns.

In Python, you can define getters, setters, and delete methods with the property function. If you just want the read property, there is also a `@property` decorator you can add above your method.
```python
class C(object):
    def __init__(self):
        self._x = None
#C._x is an attribute
@property
    def x(self):
        """I'm the 'x' property."""
        return self._x
# C._x is a property   This is the getter method
@x.setter # This is the setter method
    def x(self, value):
        self._x = value
@x.deleter # This is the delete method
    def x(self):
        del self._x
```
## Method
A method is a function that takes a class instance as its first parameter. Methods are members of classes.

## Exception
## What are exceptions in Python?
Python has many built-in exceptions which forces your program to output an error when something in it goes wrong.
When these exceptions occur, it causes the current process to stop and passes it to the calling process until it is handled. If not handled, our program will crash.
For example, if function A calls function B which in turn calls function C and an exception occurs in function C. If it is not handled in C, the exception passes to B and then to A.
If never handled, an error message is spit out and our program come to a sudden, unexpected halt.

## Unit Test
## goal of unit Test
The goal of unit testing is to segregate each part of the program and test that the individual parts are working correctly. It isolates the smallest piece of testable software from the remainder of the code and determines whether it behaves exactly as you expect. Unit testing has proven its value in that a large percentage of defects are identified during its use. It allows automation of the testing process, reduces difficulties of discovering errors contained in more complex pieces of the application, and enhances test coverage because attention is given to each unit.

## Basic example of unit Test
The unittest module provides a rich set of tools for constructing and running tests. This section demonstrates that a small subset of the tools suffice to meet the needs of most users.

Here is a short script to test three string methods:
 
![unitTest](/images/unitTest.PNG)

## Constructor
Constructors are generally used for instantiating an object.The task of constructors is to initialize(assign values) to the data members of the class when an object of class is created.In Python the __init__() method is called the constructor and is always called when an object is created.

    def __init__(self):
        #body of the constructor

## Factory
## Introducting Factor Method
Factory Method is a creational design pattern used to create concrete implementations of a common interface.

It separates the process of creating an object from the code that depends on the interface of the object.

For example, an application requires an object with a specific interface to perform its tasks. The concrete implementation of the interface is identified by some parameter.

Instead of using a complex if/elif/else conditional structure to determine the concrete implementation, the application delegates that decision to a separate component that creates the concrete object. With this approach, the application code is simplified, making it more reusable and easier to maintain.

Imagine an application that needs to convert a Song object into its string representation using a specified format. Converting an object to a different representation is often called serializing. You’ll often see these requirements implemented in a single function or method that contains all the logic and implementation, like in the following code:
![factory1](/images/factory1.PNG)
In the example above, you have a basic Song class to represent a song and a SongSerializer class that can convert a song object into its string representation according to the value of the format parameter.
The .serialize() method supports two different formats: JSON and XML. Any other format specified is not supported, so a ValueError exception is raised.
Let’s use the Python interactive shell to see how the code works:
![factory2](/images/factory2.PNG)
You create a song object and a serializer, and you convert the song to its string representation by using the .serialize() method. The method takes the song object as a parameter, as well as a string value representing the format you want. The last call uses YAML as the format, which is not supported by the serializer, so a ValueError exception is raised.

This example is short and simplified, but it still has a lot of complexity. There are three logical or execution paths depending on the value of the format parameter. This may not seem like a big deal, and you’ve probably seen code with more complexity than this, but the above example is still pretty hard to maintain.

## Decorator
Both functions and methods are called callables because they can all be executed.
In fact, any object that implements the __call__() method is a callable.
So, the Decorator is a callable that returns a callable.
Decorator uses a function as a parameter, adds some functionality to make a new function, and then returns it.
![decorator](/images/decorator1.PNG)
In the above example, make_pretty() is a Decorator.
Decorator is like a wrapper.
Decorator is like "decorate" the incoming function, then spit it out.

A simpler way to use decorator is in python, which is the @symbol:

    @make_pretty
    def ordinary():
        print("i am odinary")

Same with
 
    def ordinary():
        print("i am ordinary")
    ordinary = make_pretty(ordinary)

Note that in the following example, the reassigned ordinary is not an ordinary defined by def, but an ordinary modified by a decorator.
So in the above example, the @ symbol directly creates a modified ordinary, eliminating the intermediate form.

    
## Extend Class
## example of extend Class
Suppose we have an animal class Animal with two properties name, age, and two methods sleep() and eat().
![eclass](/images/eclass1.PNG)

Suppose we have a Dog class that also contains these two properties and the two methods, as well as its own unique properties (color) and methods (dark).
![eclass2](/images/eclass2.PNG)

When we write the dog class, we don't need to rewrite the two methods already in the Animal class. We can use it directly. The first line of code imports the Animal class for the inheritance of the Dog class. Import the class. Syntax: from module name import class name.
In the third line, we pass the Animal class into Dog(), indicating that Dog inherits Animal, and the fifth line's super() means that the parent class's __init__() method is called for initialization. Dog also has its own specific property color ( Color), because there is no color attribute in Animal, so we need to use the self.color=color statement to assign values. The Dog class has its own specific method, bark() shit method, so the 13th, 14th, and 15th lines of code You can either call a specific method in your own class or call all methods in the parent class Animal.
## CSV Files
## What is csv file
A CSV file (Comma Separated Values file) is a type of plain text file that uses specific structuring to arrange tabular data. Because it’s a plain text file, it can contain only actual text data—in other words, printable ASCII or Unicode characters.

The structure of a CSV file is given away by its name. Normally, CSV files use a comma to separate each specific data value. Here’s what that structure looks like:

![csv](/images/csv1.PNG)
Notice how each piece of data is separated by a comma. Normally, the first line identifies each piece of data—in other words, the name of a data column. Every subsequent line after that is actual data and is limited only by file size constraints.

In general, the separator character is called a delimiter, and the comma is not the only one used. Other popular delimiters include the tab (\t), colon (:) and semi-colon (;) characters. Properly parsing a CSV file requires us to know which delimiter is being used.
## Reading File
Reading CSV files with csv
Reading from a CSV file is done using the reader object. The CSV file is opened as a text file with Python’s built-in open() function, which returns a file object. This is then passed to the reader, which does the heavy lifting.

Here’s the employee_birthday.txt file:
![csv2](/images/csv2.PNG)

Here’s code to read it:

    import csv

    with open('employee_birthday.txt') as csv_file:
        csv_reader = csv.reader(csv_file, delimiter=',')
        line_count = 0
        for row in csv_reader:
            if line_count == 0:
                print(f'Column names are {", ".join(row)}')
                line_count += 1
            else:
                print(f'\t{row[0]} works in the {row[1]} department, and was born in {row[2]}.')
                line_count += 1
        print(f'Processed {line_count} lines.')

This results in the following output:

![csv4](/images/csv4.PNG)

Reading CSV Files Into a Dictionary With csv
Rather than deal with a list of individual String elements, you can read CSV data directly into a dictionary (technically, an Ordered Dictionary) as well.

Again, our input file, employee_birthday.txt is as follows:
![csv5](/images/csv5.PNG)

Here’s the code to read it in as a dictionary this time:

    import csv

    with open('employee_birthday.txt', mode='r') as csv_file:
        csv_reader = csv.DictReader(csv_file)
        line_count = 0
        for row in csv_reader:
            if line_count == 0:
                print(f'Column names are {", ".join(row)}')
                line_count += 1
            print(f'\t{row["name"]} works in the {row["department"]} department, and was born in {row["birthday month"]}.')
            line_count += 1
        print(f'Processed {line_count} lines.')

This results in the same output as before:
![csv6](/images/csv6.PNG)

Where did the dictionary keys come from? The first line of the CSV file is assumed to contain the keys to use to build the dictionary. If you don’t have these in your CSV file, you should specify your own keys by setting the fieldnames optional parameter to a list containing them.

