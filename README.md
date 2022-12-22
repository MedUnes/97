<h1 align="center">
    Notes on book: "97 Things Every Programmer Should Know"<br>
</h1>

<div align="center">

<img src="https://github.com/medunes/97/blob/master/logo.jpg" width="200" href="https://www.amazon.com/Things-Every-Programmer-Should-Know/dp/0596809484/ref=sr_1_1?keywords=97+things+every+programmer+should+know">

</div>

[![Author](https://img.shields.io/badge/author-@medunes-blue.svg?style=flat-square)](https://twitter.com/medunes2)

### [1- Act with prudence (Seb Rose)](#1)
* Whenever you implement solutions introducing technical debts, make sure you keep track of that. 
* Once done, estimate the cost of this tech-debt and include it in your "pricing"

### [2- Apply Functional Programming Principles (Edward Garson)](#2) :+1: :+1:
* Always fight for pure functions: functions which do not mutate data
* OOP design patterns, principles and best practices (for instance TDD) try to reduce the number of **random** context
were "weird" mutations might happen. Functional programming radically solves this problem.

### [3- Ask, “What Would the User Do?” (You Are Not the User) (Giles Kolborne)](#3) :+1:

* Users think differently than programmers: this is a fact
* A good approach to "explore" their minds is to ask them to perform simple tasks ** in a non-technical words**
[*User Story*? ] (ex:calculate the expenses), and watch how they do them.
* Usually all or almost all users turn around a core behavior, this is your takeaway.
* Trap N.1: Avoid discussions where the topic is "so we suppose the users should do this and that"
* Trap N.2: Watch out what users say they need, only trust what users "truly" need by watching them.
* Trap N.3: Do not lose your time "forcing" users do something your way, they will always use their "weird" ways.


### [4- Automate Your Coding Standard (Filip van Laenen)](#4) :+1:

* There are mature and widely accepted tools which guarantee coding standards and most of those boring repetitive tasks
aimed to keeping the codebase at a minimal standard.
* Hints: linters, static code analyzers, code coverage, type coverage, cognitive complexity, mess detectors..
* If you include the following two practices in your team's discipline (or self-disciple), you already close the door
against a huge amount of human conflicts, technical debts and management delays:
    * Agree on a set of rules, **beforehand**
    * Invest time to include all of these rules in an automated process that **breaks** the build if not applied
* It is **never** a waste of time or money to dedicate resources for correctly building and implementing reusable
pipelines for faster incorporation in all projects.

### [5- Beauty Is in Simplicity (Jørn Ølmheim)](#5)
* Simplicity relates to code beauty which is a subjective topic.
* We might agree on the principle of beauty through credibility principle: you can learn beautiful code design by reading
into well-known accepted leaders of the domain.

### [6- Before You Refactor (Rajith Attapattu)](#6) :+1:
* We might end-up writing worse code after refactoring if we **do not learn** from the legacy smells.
* No matter how ugly it might look, think twice about rewriting a production code.
* A production code includes ages of work-arounds, bug-fixes and subtle business logic, so watch out while touching!
* Subjective personal choices souldn't be **alone** a reason for refactoring.
* Tests are a treasure of knowledge: pay attention to what they try to verify before refactoring!
* A new technology would be a reason for rewrite if and only if a significant improvements in
  functionality, maintainability, or productivity is required and most likely to happen.
### [7- Beware the Share (Udi Dahan)](#7)
* This is IMHO a rephrasal of the [Liskov principle](https://en.wikipedia.org/wiki/Liskov_substitution_principle).
* In few words, DRY principle which might imply packing and reusing some code blocks, should take into consideration the
**context** and the expected evolution trajectory of the implementation.

### [8- The Boy Scout Rule (Robert C. Martin, a.k.a Uncle Bob)](#8) :+1:
* The original form of that rule, written by Robert Stephenson Smyth Baden-Powell, the father of scouting, was “Try and
  leave this world a little better than you found it.”.
* You don't need to do radical rewrite, you only want to do a **small little improvement** of the code you came across,
something like a better method name or adding a tiny unit test.
* Code dirt should be considered as rude as real social dirt and rudeness!

### [9- Check Your Code First Before Looking to Blame Others (Allan Kelly)](#9) :+1:
* Widely used and tested tools are way less error-prone than your personal code, that's why you should start blaming it!
* **"Assumptions"**, Beware of assumptions! The tools you use might have different conventions and assumptions than 
yours. And as assumptions are usually out of questioning, they might take you ages before you start checking them!
* Often a sticky resistant bug might be hidden in a higher or lower layer of the tech-stack. So if code is ok, check the
surroundings.
* Remember Sherlock Holmes’s advice: 
>"Once you eliminate the impossible, whatever remains, no matter how improbable, must be the truth."