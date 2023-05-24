<h1 align="center">
    Notes on book: "97 Things Every Programmer Should Know"<br>
</h1>

<div align="center">

<img src="https://github.com/medunes/97/blob/master/logo.jpg" width="200" href="https://www.amazon.com/Things-Every-Programmer-Should-Know/dp/0596809484/ref=sr_1_1?keywords=97+things+every+programmer+should+know">

</div>

[![Author](https://img.shields.io/badge/author-@medunes-blue.svg?style=flat-square)](https://twitter.com/medunes2)

## Symbols:

:+1: /  :+1::+1: /  :+1: :+1: :+1:  represent how much I learned from that particular point (and this is purely personal)
### [1- Act with prudence (Seb Rose)](#1)
* Whenever you implement solutions introducing technical debts, make sure you keep track of that. 
* Once done, estimate the cost of this tech-debt and include it in your "pricing"

### [2- Apply Functional Programming Principles (Edward Garson)](#2) :+1: :+1:
* Always fight for pure functions: functions which do not mutate data
* OOP design patterns, principles and best practices (for instance TDD) try to reduce the number of **random** context
where "weird" mutations might happen. Functional programming radically solves this problem.

### [3- Ask, “What Would the User Do?” (You Are Not the User) (Giles Kolborne)](#3) :+1:

* Users think differently than programmers: this is a fact
* A good approach to "explore" their minds is to ask them to perform simple tasks **in non-technical words**
[*User Story*? ] (ex:calculate the expenses), and watch how they do them.
* Usually, the majority of users will turn around a core behavior, this is your takeaway, and there you go.
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

### [10- Choose your tools with care (Giovanni Asproni)](#10) :+1:
* Yes, buying existing software might be cheaper and more reliable than hiring humans to create them.
* However, combining the bought software with each-other might require hacks and workarounds which could bypass in 
cost and time what would have been achieved by humans.
* Two more bad news for you: free tools have licenses (think GPL), and they also can make you doomed to a specific 
locked version of other tools.
* A good remedy for this is to leverage the [Dependency Inversion principle](https://en.wikipedia.org/wiki/Dependency_inversion_principle) from SOLID.

### [11- Code in the  Language of  the Domain  (Dan North)](#11) :+1:
* Leverage what the development eco-system grants you (latin letters, git commits, function and class names, JIRA links)
* Your ultimate goal is to reduce the technical jargon and increase the business one
* If technical low level implementation details have to be written the hardcode way (and they must at some point), try 
to put them in the lowest hidden level so that access them is "optional" and "on-demand" Do not make it the entrypoint!
>The programmer who comes along a few months later to work on the code will thank you.
>The programmer who comes along a few months later might be you.

### [12- Code Is Design  (Ryan Brush)](#12) :+1: :+1:
* The trickiest trap behind the so called *software crisis* is that software often involves zero material costs.
* This fact creates an illusion that we can re-create a better version, free of cost whenever a previous version wasn't
good enough, or even failed.
* The urge for competitiveness and be first in the market insanely fuels this rush and ends up with frustrating series
of collapse stories.
* The rule of thumb here is to put the emphasis on two pillars:
  * Robust automated test suites
  * Skilled and gifted code designers
>great designs are produced by great designers dedicating themselves to
>the mastery of their craft. Code is no different.

### [13- Code Layout Matters  (Steve Freeman)](#13) :+1:

* Our eyes (perception system) and our mind (brain) are crucial factors which -behind the scenes- are the real judges to
tell whether some piece of code is clean or nasty.
  * **Perception**: Our window to "the world" is the IDE's screen. Struggle that every single pixel of it participates in 
  communicating information about the code in the most *cohesive* way
  * **Mind**: conditions, if statements, inconsistent code styles, having to switch between files.. All these factors
  are building a "state machine" or a "pending stack" for the mind while analyzing the code. This thing is our public
  enemy number one that makes us feel uncomfortable while scanning code. We should reduce this stack to the minimum to
  free up resources for our minds and let them focus on one direction

### [14- Code Reviews  (Mathias Karlsson)](#14) :+1:
* Unless strictly required by some compliance rules, code review should be peer to peer rather than superior to peers.
* The reviewer's goal should be "understand the committed code and the coder's intention" rather than spotting issues.
* The ultimate keyword for code reviews is **knowledge sharing**. Remember that, always, please!
* Set up a diverse strategy where juniors review based on their academic and fresh theoretical background, while seniors
review from their experience and pragmatic perspective. This ensures knowledge-sharing, enthusiasm and smoothness for 
all participants
* Avoid aggressive, arrogant and sarcastic comments. Use suggestions, questions, arguments instead.
* Watch-out: a general failure in the code-review process can have severe impact on productivity, or even trigger more
critical team conflicts..

### [15- Coding with Reason  (Yechiel Kimchi)](#15) :+1:

* Several widely agreed best practices in software engineering turn around 
> don’t ask  an object for information to work with. Instead, ask the object to do the
work with the information it already has. 
> In other words, encapsulation is
all—and only—about narrow interfaces.om Technical (Dan Bergh Johnsson) :+1:
