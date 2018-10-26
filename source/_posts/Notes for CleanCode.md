---
title: Notes for CleanCode
date: 2018-10-24 21:07:41
tags:
	- notes
	- code
---

# Notes for CleanCode


# Meaningful name
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
* add meaningful context

#   Functions
>  The first rule of functions is that they should be small. The second rule of functions is that they should be smaller than that.

### Function should do one thing, they should do it well. they should do it only.
## One level of abstraction per function

#  Comments
> Don’t comment bad code. re-write it

1. Comments don’t make up for bad code
2. Explain in the code instead of writing comments
3. Comments can be use the warn other programmers such as this function takes long time to run 
4. TODO comments is good
5. Amplification, A comment maybe used to amplify the importance of something that may otherwise seem inconsequential

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

### Rules for a good tests
#### Fast: Test should be fast. They should run quickly when test run slow, you won’t want to run them frequently 
#### Independent: Tests should not depend on each other, One test should not set up the conditions for the next Test
#### Repeatable: Tests should be repeatable in any environment. So that there is no excuse when test is failing
#### Self-Validation: The tests should have a boolean output, either pass or fail
#### Timely: The tests need to be written in timely fashion, Unit tests should be written just before the production code that makes them pass. If you write tests after the production code, them you may find the production code to be hard to test


# Classes
## Class should be Small
* how small the class should be? should be around 5 methods
* how to name is the first rule of helping determine class size. 
* class name should not have *Processor* or *Manager* or *Super* often hint at unfortunate aggression of responsibilities
 
## The Single Responsibility Principle
> class or module should have one and only one /reason to change
> A class should only have one responsibility
> 

### ways to make class smaller => limit the number of in class variable 
### each variables should be sued by most of the methods inside class

When a class contains more than 5 variables break it down

Isolate class less dependents are good for changes in the future
