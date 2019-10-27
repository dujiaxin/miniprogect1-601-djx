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
Look to the example at the beginning of this section to see the bodies of the function definition, the for-loop, and the subsequent if-else block were all separated by increasing levels of indentation.

Python’s syntax is quite flexible in terms of what it defines as a whitespace delimiter. Its rules are that:

One or more whitespace characters (spaces or tabs) is sufficient to serve as indentation.
A given indented block must use a uniform level of indentation. E.g. if the first line of an indented block has two leading spaces, all subsequent lines in that block must lead with exactly two white spaces.
While Python’s syntax is relatively forgiving, I am not: the standard style for indenting in Python is to use four space characters for each level of indentation. It is strongly advised that you adhere to this standard. Most IDEs and consoles (including Jupyter notebooks) will automatically add a four-space indentation for you when you enter into the body of one of the aforementioned constructs.
See this [Link](#https://www.python.org/dev/peps/pep-0008/#indentation)
## Don't Repeat Yourself

## Design Patterns from Gang of Four

## Class

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
