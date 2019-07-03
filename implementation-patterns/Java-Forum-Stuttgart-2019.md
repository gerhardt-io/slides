---
title: Implementation Patterns
separator: "^\n\n\n"
verticalSeparator: "^\n\n"
theme: blood
revealOptions:
    transition: fade
---
## Implementation Patterns
**Dr. Frank Gerhardt**

03.07.2019

![](gi-logo-white.svg)


<!-- .slide: data-background="./Implementation-Patterns-Korsika.jpg" -->


## About
- Smalltalker, LISP-Lover, Emacs
  - auch Java, Eclipse, neuerdings JS, Python
  - für Clojure gibt's leider weder Kunden noch Entwickler :-/
- Gründer und 1. Erster Vorsitzender der JUGS
  - erster JFS-Organisator 
- Software Experts Network Stuttgart e.V.
  - nachher am Stand
- Gerhardt Informatik, 10 Mitarbeiter
- we're not hiring, kein Gewinnspiel ;-)
- freie Kapa ab September

<!--
SW archaeology, Steinplatten

schools: formal spec+transformation, MDA, top down

TODO Foto

TODO use green

Words inspired by c2: YAGNI DSSTTCPW design carry, code smell

my holiday reading

TODO the art of writing is re-writing

-->


## Abstract

<p align="left" style="font-size:80%;" >
Implementation Patterns ist ein leider in Vergessenheit
geratenes Buch von Kent Beck aus dem Jahr 2007. Diese Patterns,
auch Idiome genannt, sind unterhalb von Design Patterns aber
oberhalb von Code-Formatierungsregeln angesiedelt. Bei den
Implementation Patterns geht es darum wie man einzelne Klassen und
Methoden gestaltet. In Code Reviews bin ich immer wieder auf Fälle
gestoßen, bei denen schlechter Code auf Unkenntnis der
Implemenation Patterns zurück geführt werden kann. Anfänger und
Fortgeschrittene können die Qualität ihres Codes wesentlich
verbessern, wenn sie die Implementation Pattern kennen und
anwenden.
</p>


## Why?
- there was no talk on YouTube
* I have two books
- people don't read
- I read a lot more code nowadays
- reviewing is coaching
- I do it because
- most projects don't



## About Kent Beck
- SUnit -> JUnit -> xUnit
- Ward and Kent, c2.com Wiki
- talk at JUGS
- Volksfest
- new book Refactoring, 2nd ed.
<!--
TODO JUGS-Bild
-->
<!--
-->


## Design Patterns
Gang of Four, 1994, using C++

![](https://images-na.ssl-images-amazon.com/images/I/51szD9HC9pL._SX395_BO1,204,203,200_.jpg) ![](https://images-na.ssl-images-amazon.com/images/I/51uxEj502bL._SX389_BO1,204,203,200_.jpg)
<!-- Design Patterns for Dummies 
-->


## Test-Driven Development
Test-Driven Development (TDD), 2002
![](https://images-na.ssl-images-amazon.com/images/I/51kDbV%2BN65L._SX396_BO1,204,203,200_.jpg)


## XP
eXtreme Programming, 1999, 2nd ed. 2004
![](https://images-na.ssl-images-amazon.com/images/I/416Y8MS65TL._SX377_BO1,204,203,200_.jpg)


## Refactoring
2012, 2nd ed. 2019

![](https://images-na.ssl-images-amazon.com/images/I/51K-M5hR8qL._SX392_BO1,204,203,200_.jpg) ![](https://images-na.ssl-images-amazon.com/images/I/41LBzpPXCOL._SX379_BO1,204,203,200_.jpg)


## About the Book
- first as Smalltalk book, 1996
- then Java, when JUnit 4 was new
- 77 patterns
  - in 45 minutes!? Nope.

![](https://images-na.ssl-images-amazon.com/images/I/513f-WV%2BNjL._SX376_BO1,204,203,200_.jpg) ![](https://images-na.ssl-images-amazon.com/images/I/51CwRmCLjML._SX381_BO1,204,203,200_.jpg)

<!--
read the book
desk reference
2nd nature
"Projektsprache"
personal style
 
TODO was war der Satz mit breeds defects?
Nested conditionals breed defects.
TODO add code example

TODO is there an errata?
e.g. field roles, "plain data" is missing IMHO

What is old about the book
- Interfaces
- paper
- "he" not "she"
- functional
- annotations
- all real-world cross-cutting concern: authorizaiton, logging,
  multi-threading, versioning
  - authorization
  - persistence
  - logging
  - concurrency

examples from JUnit 4

Hey, which books have a theory section and a philosophy appendix!?

refers to Christopher Alexander

TODO how to write unmaintainable code

TODO using syntax highlighting, no types in names

TODO Kafka: alles umbenennen

TODO think about the debugger + stack traces
- need to work with code when error happens
- under stress

TODO beginner style: yet another level of if

-->


## Spanish Talk
<iframe width="640" height="360" src="https://www.youtube.com/embed/y82xz547zs8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

https://www.youtube.com/watch?v=y82xz547zs8


<!-- .slide: data-background="./structure.jpg" -->

<!-- 
## Structure
![](structure.jpg)
-->


## Mantra
Programming so that other people can understand your code

## Jeopardy
Example
- Answer: A word describing being thrown out of window <!-- .element: class="fragment" -->
- Question: What is defenestration? <!-- .element: class="fragment" -->


## Coding is like Jeopardy
- the Java code is the answer
- what was the question? 

A field declared as a `Set` means...


## Assumption, Premise

> Good code matters.

Most of the time, not always.


## Goal
- don't program by instinct
  - explainable, why?
- importance of other people
- consciously for others as well as for yourself


## How to use the Book
Kent writes
- read just in time
- use patterns every few seconds

First, browse content to know what's in there.

Read ch. "A Theory of Programming" first, it's great.
<!--
Chapter 1: Introduction
Tour Guide
And Now
Chapter 2: Patterns
Chapter 3: A Theory of Programming
Values
Communication
Simplicity
Flexibility
Principles
Local Consequences
Minimize Repetition
Logic and Data Together
Symmetry
Declarative Expression
Rate of Change
Conclusion
Chapter 4: Motivation
-->



## Theory


## "Laws"
- code is more often read than written
- there is no "done"
- basic set of control flow concepts (sequence, branch, loop, call)
- path of understanding
  - detail-to-concept
  - concept-to-detail
- the patterns are not general
  - adapt to personal style


## Values and Principles
- 3 values
- 6 principles


## Values
- communication
- simplicity
- flexibility


## Communication
- with other people
- literate programming
  - nice: Jupyter notebooks
- the other's perspective


## Simplicity
- remove excess complexity
- in the eye of the beholder
- have audience in mind
- waves of complexity and simplification


## Flexibility
- keep options open
- misused? speculative?

<!--
TODO naming
CamelCase, under_scores, lisp-style should go into style guide
-->


## Principles
- local consequences
- minimize repetition
- logic and data together
- symmetry
- declarative expression
- rate of change (temporal symmetry)


## Motivation
- cost
  - initial
  - maintenance
    - understanding
	- changing
	- testing
	- deploying
- don't forget human needs



## Patterns Overview by...
- Class
- State: different data
- Behavior: similar logic
- Methods: dividing logic
- Collections
- Frameworks


## Class Patterns 

**Class**
Simple Superclass Name
**Qualified Subclass Name** 
Abstract Interface
**Interface**
Abstract Class
**Versioned Interface**
Value Object
**Specialization**
Subclass
**Implementor**
Inner Class
**Instance-Specific Behavior**
Conditional
**Delegation**
Pluggable Selector
**Anonymous Inner Class**
Library Class

Note: (ch. 5)


## State Patterns 
State
**Access**
Direct Access
**Indirect Access**
Common State
**Variable State**
Extrinsic State
**Variable**
Local Variable
**Field**
Parameter
**Collecting Parameter**
Optional Parameter
**Var Args**
Parameter Object
**Constant**
Role-Suggesting Name
**Declared Type**
Initialization
**Eager Initialization**
Lazy Initialization

Note: (ch. 6)


## Behavior Patterns
Control Flow
**Main Flow**
Message
**Choosing Message**
Double Dispatch
**Decomposing (Sequencing) Message**
Reversing Message
**Inviting Message**
Explaining Message
**Exceptional Flow**
Guard Clause
**Exception**
Checked Exceptions
**Exception Propagation**

Note: Chapter 7: 


## Methods Patterns

**Composed Method**
Intention-Revealing Name
**Method Visibility**
Method Object
**Overridden Method**
Overloaded Method
**Method Return Type**
Method Comment
**Helper Method**
Debug Print Method
**Conversion**
Conversion Method
**Conversion Constructor**
Creation
**Complete Constructor**
Factory Method
**Internal Factory**
Collection Accessor Method
**Boolean Setting Method**
Query Method
**Equality Method**
Getting Method
**Setting Method**
Safe Copy

Note: Chapter 8: 


## Collections Patterns
- Metaphors, Issues
- Interfaces
  - **Array** Iterable **Collection** List **Set** SortedSet
    **Map**
- Implementations
  - **Collection** List **Set** Map **Collections** Searching
    **Sorting** Unmodifiable Collections **Single-Element
    Collections** Empty Collections **Extending Collections**

Note: Chapter 9: 


## Evolving Frameworks
- Changing Frameworks without Changing Applications
- Incompatible Upgrades
- Encouraging Compatible Change
- Library Class
- Objects



## Class Patterns


## Class
- data changes for often than logic
- expensive
- reduce number


## Simple Superclass Name
- the super class name is the most important name
- operation follow after the class name, not reverse
- tension long or short?
- pick strong metaphor
- a few single words
- use a thesaurus
- go for a walk


## Qualified Subclass Name
- one word would be best
- express how is the subclass
  - similar
  - different
- multi-level hierarchies are generally delegation waiting to happen
- too short names burden the developers' short term memory


## Abstract Interface
- each interface has a cost
  - one more thing to learn, understand, document, debug, organize,
    browse, and name
- can cause inflexibility
- there are limits to the value of "future-proofing" software
  through speculation
- Putting all these factors together - the need for flexibility,
  the cost of flexibility, the unpredictability of where
  flexibility is needed - leads me to the belief that the time to
  introduce flexibility is when it is definitely needed.


## Interface 
- named like classes
- names already used up by classes
  - ISomething is fine, see Eclipse
  - SomeImpl is a bit ugly
- changes to interfaces are discouraged


## Abstract Class
- a mix of interface and class


## Versioned Interface
- OK if not too many
- see Eclipse
  - ISomething, ISomething2, ISomething3
- `instanceOf` 


## Value Object
- set all fields in constructor
- always return new objects
- whenever possible create microworlds of math


## Specialization
- extremes
  - same logic, different data
  - different logic, same data


## Subclass
- can play this card only once :-/
- static, can not change at runtime
  - delegation can
- methods should do one job
  - to not have to copy from super class
- avoid parallel hierarchies


## Implementor
- polymorphic messages
  - to different receivers
  - for parameters see *overloading*
- to express choice
- open a system to variation


## Inner Class
- when nobody outside needs to know


## Instance-Specific Behavior
- static
- dynamic


## Conditional
- or maybe better
  - subclass
  - delegation
  
  
## Delegation
- pass delegator as a parameter
- store in a field
- or calculated


## Pluggable Selector
- call with reflection
- store name in field


## Anonymous Inner Class
- alternative way to implement *instance-specific behavior*
- override one or more methods for specific behavior
- more static that delegation
- difficult to test


## Library Class
- start with static methods
- try instances
- maybe evolve to a real class



## State Patterns


## State


## Access


## Direct Access


## Indirect Access


## Common State


## Variable State


## Extrinsic State


## Variable


## Local Variable


## Field


## Parameter


## Collecting Parameter


## Optional Parameter


## Var Args


## Parameter Object


## Constant


## Role-Suggesting Name


## Declared Type


## Initialization


## Eager Initialization


## Lazy Initialization



## Behavior Patterns


## Control Flow


## Main Flow


## Message


## Choosing Message


## Double Dispatch


## Decomposing (Sequencing) Message


## Reversing Message


## Inviting Message


## Explaining Message


## Exceptional Flow


## Guard Clause


## Exception


## Checked Exceptions


## Exception Propagation



## Methods Patterns


## Composed Method


## Intention-Revealing Name


## Method Visibility


## Method Object


## Overridden Method


## Overloaded Method


## Method Return Type


## Method Comment


## Helper Method


## Debug Print Method


## Conversion


## Conversion Method


## Conversion Constructor


## Creation


## Complete Constructor


## Factory Method


## Internal Factory


## Collection Accessor Method


## Boolean Setting Method


## Query Method


## Equality Method


## Getting Method


## Setting Method


## Safe Copy




## JavaScript
```JS
Reveal.initialize({
	// Options which are passed into marked
	// See https://marked.js.org/#/USING_ADVANCED.md#options
	markdown: {
		smartypants: true
	}
});
```



## Links
- https://github.com/gerhardt-io/slides

# One

> Best quote ever.

* Frag 1 <!-- .element: class="fragment" -->
* Frag 2 <!-- .element: class="fragment" -->

Note: speaker notes FTW!


<!-- .slide: data-background="#ffffff" -->
The End.
