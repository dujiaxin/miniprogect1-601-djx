# Additional Terms in Mini-project 2
definitions and examples of the following terms:

* [How Python uses Indentation to control Flow](#how-python-uses-indentation-to-control-flow)
* [Don't Repeat Yourself](#Home) 
* [Design Patterns from Gang of Four](#ls)
* [Class](#cd)
* [Object](#mkdir)
* [Static](#cp)
* [Property/Attribute](#mv)
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

## Don't Repeat Yourself

## Design Patterns from Gang of Four

## Class

## Object

## Static

## Property/Attribute

## Method

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

