---
title: Reading Notes for CleanCode
date: 2019-8-10 21:07:41

---

> Writing clean code is what you must do in order to call yourself a professional. There is no reasonable excuse for doing anything less that you best

# Chapter 1 What is Clean Code?

**Bjarne Stroustrup**: elegent, bug no where to hide, performance close to optimal

**Grady Booch**: simple and direct

**Dave Thomas**: can be read and enhanced by a developer other than its original author

#Chapter 2 Meaningful name

* Use Intention-revealing Names
* Avoid Disinformation 
	* do not call it a list unless it’s actually a list
* Make Meaningful Distinctions
	* do not code for compiler or interpreter	
* 	Use Pronounceable Names
* Use Searchable Names
* Avoid Encoding
* Avoid Mental Mapping
* No pun or cute word
* Use solution/problem domain names
* Add meaningful context

# Chapter 3 Functions

>  The first rule of functions is that they should be small. The second rule of functions is that they should be smaller than that.

### Function should do one thing, they should do it well. they should do it only.

> No side effects. Function must promises to do one thing,and it does not do any other hidden things

### Command Query Separation

	> Function should either do something or answer something, but now both
	>
	> Either function change the state of an object or return some info about that object
	>
	> Do BOTH can lead confusion

### Use Expcetions to return error instead of error codes

#  Chapter 4 Comments
> Don’t comment bad code. re-write it

1. Comments don’t make up for bad code
2. Explain in the code instead of writing comments
3. Comments can be use the warn other programmers such as this function takes long time to run 
4. TODO comments is good
5. Amplification, A comment maybe used to amplify the importance of something that may otherwise seem inconsequential

# Chapter 5 Formatting

The purpose of formatting

> Code formatting is about communication, and communication is the professional developer's first order of business 

Number lines of code per file range from 0 to 200 (up to 500)

Vertical Density

- If openness separates concepts, then vertical density implies close association. So Lines of code that are tightly related should appear vertically dense
- USELESS comment block can separate close associated code

**Variable Declaration**: Should be declares as close to their usage as possible

**Instance variable**: Should be declared at the top of the class

**Depended Fucntions**: If one function calls another, they should be vertically close, and the caller should be above the callee

```python
def foo:
  if bar():
    return true
  else:
    return false
  
 def bar:
   return true
```

### Horizontal Formatting

How wide should a line be: 0 to120

**Horizontal Alignment**: is not very useful

# Object and Date Structures

## The Law of Demeter:
> A module should not know about the innards of the objects it manipulates.
> For example, A method f of a class C should only call the methods of these, C or An object created by f


# Boundaries
before using 3rd party code. write test case for their code and test their functionality — Learning Test

# Unit Tests
## The Tree Laws of TDD
1. You may not write production code until you have written a failing unit test
2. You may note write more of a unit test than is sufficient to fail and not compiling is failing
3. You may not write more production code than is sufficient to pass the currently failing test

## Keeping Tests clean
The test code should be same standard of the production code since tests must change as the production code evolves
Without a test suite developer lost the ability to make sure that changes to their codebase worked as expect 
Unit tests keep our code *flexible*, *maintainable* and *reusable*

#### What makes a clean test => Readability

## Rules for a good tests
- Fast: Test should be fast. They should run quickly when test run slow, you won’t want to run them frequently 
-  Independent: Tests should not depend on each other, One test should not set up the conditions for the next Test
-  Repeatable: Tests should be repeatable in any environment. So that there is no excuse when test is failing
- Self-Validation: The tests should have a boolean output, either pass or fail
-Timely: The tests need to be written in timely fashion, Unit tests should be written just before the production code that makes them pass. If you write tests after the production code, them you may find the production code to be hard to test


# Classes
## Class should be Small
* how small the class should be? should be around 5 methods
* how to name is the first rule of helping determine class size. 
* class name should not have *Processor* or *Manager* or *Super* often hint at unfortunate aggression of responsibilities

## The Single Responsibility Principle
> class or module should have one and only one /reason to change
> A class should only have one responsibility
> 

- Ways to make class smaller => limit the number of in class variable 

- Each variables should be sued by most of the methods inside class

- When a class contains more than 5 variables break it down

- Isolate class less dependents are good for changes in the future
