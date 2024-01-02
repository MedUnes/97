<h1 align="center">
    Notes on book: "97 Things Every Programmer Should Know" (A.K.A The annotated 97)<br>
</h1>

<div align="center">

<img src="https://github.com/medunes/97/blob/master/logo.jpg" width="200" href="https://www.amazon.com/Things-Every-Programmer-Should-Know/dp/0596809484/ref=sr_1_1?keywords=97+things+every+programmer+should+know">

</div>

[![Author](https://img.shields.io/badge/author-@medunes-blue.svg?style=flat-square)](https://twitter.com/medunes2)

## What is it?
* These are my **own** notes/thoughts/annotations on the very famous book "97 Things Every Programmer Should Know".
* I did it for three purposes:
    * Summarize that valuable information in a more packed size so that I can refer to it and re-read it more often
    * Merge the books information with my own information that I gathered from other sources
    * Share it with people

## Symbols/Typography:

* :+1: /  :+1::+1: /  :+1: :+1: :+1:  represent how much I learned from that particular point (and this is purely personal)
* In case I copy/paste the the authors words, I list them quoted:
> like this

## The Notes

### 1- Act with prudence (Seb Rose)
* Whenever you implement solutions introducing technical debts, make sure you keep track of that. 
* Once done, estimate the cost of this tech-debt and include it in your "pricing"

### 2- Apply Functional Programming Principles (Edward Garson) :+1: :+1:
* Always fight for pure functions: functions which do not mutate data
* OOP design patterns, principles and best practices (for instance TDD) try to reduce the number of **random** context
where "weird" mutations might happen. Functional programming radically solves this problem.

### 3- Ask, “What Would the User Do?” (You Are Not the User) (Giles Kolborne) :+1:

* Users think differently than programmers: this is a fact
* A good approach to "explore" their minds is to ask them to perform simple tasks **in non-technical words**
[*User Story*? ] (ex:calculate the expenses), and watch how they do them.
* Usually, the majority of users will turn around a core behavior, this is your takeaway, and there you go.
* Trap N.1: Avoid discussions where the topic is "so we suppose the users should do this and that"
* Trap N.2: Watch out what users say they need, only trust what users "truly" need by watching them.
* Trap N.3: Do not lose your time "forcing" users do something your way, they will always use their "weird" ways.


### 4- Automate Your Coding Standard (Filip van Laenen) :+1:

* There are mature and widely accepted tools which guarantee coding standards and most of those boring repetitive tasks
aimed to keeping the codebase at a minimal standard.
* Hints: linters, static code analyzers, code coverage, type coverage, cognitive complexity, mess detectors..
* If you include the following two practices in your team's discipline (or self-disciple), you already close the door
against a huge amount of human conflicts, technical debts and management delays:
    * Agree on a set of rules, **beforehand**
    * Invest time to include all of these rules in an automated process that **breaks** the build if not applied
* It is **never** a waste of time or money to dedicate resources for correctly building and implementing reusable
pipelines for faster incorporation in all projects.

### 5- Beauty Is in Simplicity (Jørn Ølmheim)
* Simplicity relates to code beauty which is a subjective topic.
* We might agree on the principle of: *beauty through credibility* principle: you can learn beautiful code design by reading
into well-known accepted leaders of the domain.

### 6- Before You Refactor (Rajith Attapattu) :+1:
* We might end-up writing worse code after refactoring if we **do not learn** from the legacy smells.
* No matter how ugly it might look, think twice about rewriting a production code.
* A production code includes ages of work-arounds, bug-fixes and subtle business logic, so watch out while touching!
* Subjective personal choices souldn't be **alone** a reason for refactoring.
* Tests are a treasure of knowledge: pay attention to what they try to verify before refactoring!
* A new technology would be a reason for rewrite if and only if significant improvements in
  functionality, maintainability, or productivity is required and most likely to happen.
### 7- Beware the Share (Udi Dahan)
* This is IMHO a rephrasal of the [Liskov principle](https://en.wikipedia.org/wiki/Liskov_substitution_principle).
* In few words, DRY principle which might imply packing and reusing some code blocks, should take into consideration the
**context** and the expected evolution trajectory of the implementation.

### 8- The Boy Scout Rule (Robert C. Martin, a.k.a Uncle Bob) :+1:
* The original form of that rule, written by Robert Stephenson Smyth Baden-Powell, the father of scouting, was “Try and
  leave this world a little better than you found it.”.
* You don't need to do radical rewrite, you only want to do a **small little improvement** of the code you came across,
something like a better method name or adding a tiny unit test.
* Code dirt should be considered as rude as real social dirt and rudeness!

### 9- Check Your Code First Before Looking to Blame Others (Allan Kelly) :+1:
* Widely used and tested tools are way less error-prone than your personal code, that's why you should start blaming it!
* **"Assumptions"**, Beware of assumptions! The tools you use might have different conventions and assumptions than 
yours. And as assumptions are usually out of questioning, they might take you ages before you start checking them!
* Often a sticky resistant bug might be hidden in a higher or lower layer of the tech-stack. So if code is ok, check the
surroundings.
* Remember Sherlock Holmes’s advice: 
>"Once you eliminate the impossible, whatever remains, no matter how improbable, must be the truth."

### 10- Choose your tools with care (Giovanni Asproni) :+1:
* Yes, buying existing software might be cheaper and more reliable than hiring humans to create them.
* However, combining the bought software with each-other might require hacks and workarounds which could bypass in 
cost and time what would have been achieved by humans.
* Two more bad news for you: free tools have licenses (think GPL), and they also can make you doomed to a specific 
locked version of other tools.
* A good remedy for this is to leverage the [Dependency Inversion principle](https://en.wikipedia.org/wiki/Dependency_inversion_principle) from SOLID.

### 11- Code in the  Language of  the Domain  (Dan North) :+1:
* Leverage what the development eco-system grants you (latin letters, git commits, function and class names, JIRA links)
* Your ultimate goal is to reduce the technical jargon and increase the business one
* If technical low level implementation details have to be written the hardcode way (and they must at some point), try 
to put them in the lowest hidden level so that access them is "optional" and "on-demand" Do not make it the entrypoint!
>The programmer who comes along a few months later to work on the code will thank you.
>The programmer who comes along a few months later might be you.

### 12- Code Is Design  (Ryan Brush) :+1: :+1:
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

### 13- Code Layout Matters  (Steve Freeman) :+1:

* Our eyes (perception system) and our mind (brain) are crucial factors which -behind the scenes- are the real judges to
tell whether some piece of code is clean or nasty.
  * **Perception**: Our window to "the world" is the IDE's screen. Struggle that every single pixel of it participates in 
  communicating information about the code in the most *cohesive* way
  * **Mind**: conditions, if statements, inconsistent code styles, having to switch between files.. All these factors
  are building a "state machine" or a "pending stack" for the mind while analyzing the code. This thing is our public
  enemy number one that makes us feel uncomfortable while scanning code. We should reduce this stack to the minimum to
  free up resources for our minds and let them focus on one direction

### 14- Code Reviews  (Mathias Karlsson) :+1:
* Unless strictly required by some compliance rules, code review should be peer to peer rather than superior to peers.
* The reviewer's goal should be "understand the committed code and the coder's intention" rather than spotting issues.
* The ultimate keyword for code reviews is **knowledge sharing**. Remember that, always, please!
* Set up a diverse strategy where juniors review based on their academic and fresh theoretical background, while seniors
review from their experience and pragmatic perspective. This ensures knowledge-sharing, enthusiasm and smoothness for 
all participants
* Avoid aggressive, arrogant and sarcastic comments. Use suggestions, questions, arguments instead.
* Watch-out: a general failure in the code-review process can have severe impact on productivity, or even trigger more
critical team conflicts..
### 15- Code Reviews  (Mathias Karlsson) :+1:
* Unless strictly required by some compliance rules, code review should be peer to peer rather than superior to peers.
* The reviewer's goal should be "understand the committed code and the coder's intention" rather than spotting issues.
* The ultimate keyword for code reviews is **knowledge sharing**. Remember that, always, please!
* Set up a diverse strategy where juniors review based on their academic and fresh theoretical background, while seniors
review from their experience and pragmatic perspective. This ensures knowledge-sharing, enthusiasm and smoothness for 
all participants
* Avoid aggressive, arrogant and sarcastic comments. Use suggestions, questions, arguments instead.
* Watch-out: a general failure in the code-review process can have severe impact on productivity, or even trigger more
critical team conflicts..
### 16- A comment on comments  (Cal Events) :+1: :+1:
* Comments are not evil, they are very welcome, they are first class citizens in the world of programming.
* Do not surrender to indoctrinations of the notoriety of comments. Use them as much as you want as long as you keep explaining your code to yourself and to future programmers coming across it.
* This might sound like a "devil's advocate PoV", if you are do belong to the "clean code" team. The two quotes below are very clear about this:
> Sprinkle your code with relevant comments explaining what the code is supposed to accomplish. - *Cal Events* 

> The proper use of comments is to compensate for our failure to express ourself in code. Note that I used the word failure. I meant it. Comments are always failures. - *Uncle Bob*

### 17- Comment only what the code cannot say  (Kevlin Henney) :+1:
* Unless literally deleted, comments are non-refactorable tech debt and kind of resident flaws that nor compilers neither linters can fix.
* Oppposed to what they were meant to be useful for, comments won't communicate more info for two reasons:
  * The developer's mind flags them as "ambiguous" then systematically puts them under "ignored crap".
  * They can be replcaed by dedicated tools (VCS, real code, and yes: DEL key)
* Write comments if, and only if, you can't replace them by real code. (A rephrasal of "Comment the *why*, not the *what*)
  > Comment what the code cannot say,not simply what it does not say.

### 18- Continous Learning (Clint Shank) :+1:
* Continous learning is good, in software engineering is a must, else you risk your job as the change is fast and the competition is high.
* There are two styles of learning: passive (blogs, mentors, conferences) and active (teaching, coding, blogging)
* A good way to stand out from the crowd, is to dig deeper and deeper your favourite tech-stack, debug and read the source code, up to the point it becomes naked and the magic fades away. The more magic it looks like, the more learning you need.

### 19- Convenience Is Not an -ility (Gregor Hohpe) :+1:
* API is composed of two parts: *"Application Programming"* and *"Interface"*. Your focus should be balanced towards the second part.
* What makes API different from "normal code" it is built to be used by other programmers in other programs.
* You should opt for code that is self-explanatory, optimally without the documentation. Repetition and couple more lines of code shouldn't be a problem in favor of a better DX (Developer Eperience).
* In this context, if you face a trade-off situtation of convenience vs efficiency, convenience vs consistency, or convenience vs elegance, go convenience!
* Take your time, writing an API is like raising a child, you don't usually get a second chance for it.

### 20- Deploy Early and Often (Steve Berczuk) :+1:
* Deployable production environment should come first and certainly not last.
* Releasing to production is not a magic that "those devops" bring to life over night. It should be a part of the development task itself including estimation, refinement, planning, and testing.
* Progressing for a long time on the local environment without any iterations on the production one can end up with bad surprises.
* Sometimes it is too late to fix deep code issues caused by accumulated wrong assumptions about the non-ready production.
* If someone argues about the business value of a production environment preparation, just tell them that the business value only runs on production.

### 21 Don't Ignore That Error (Pete Goodliffe) :+1:
* Ignoring errors under known developers excuses (tough deadline, it won't happen, To Do..) can lead to:
  * Security Issues (the error state is the entrypoint)
  * Ugly code to shut up the error
* IMHO, there should be a pre-agreed minimum level, below which errors can be "safely" ignored, something like the [RFC5424](https://datatracker.ietf.org/doc/html/rfc5424)
* *Don't Ignore That Error* was IMHO mentioned in this quote from the [Zen of Python](https://peps.python.org/pep-0020/#the-zen-of-python)
  > Errors should never pass silently.
  > Unless explicitly silenced.

### 22 Don’t Just Learn the Language, Understand Its Culture (Anders Norås) :+1:
* Assuing that nowadays, it is possible to solve almost any programming problem in any programming langauge, why should we learn new langauges?
* The answer is: it is not only about the language, it is about the culture. Yes you can write complete Java application with zero classes and zero interfaces, in a procedural C way, but, why would you?
* If you learn a new language, do not loose its gem: seeing the world with that languages "eyes".
  > It takes more than just learning the syntax to learn a language: you need to understand its culture
  
### 23 Don’t Nail Your Program into the Upright Position (Verity Stob) :+1:
* Choking your program with dozens if *try .. catch* and similar error muters is like hiding cancer with tons of painkillers.
* Write consistent and useful error handlers or avoid that thing completely. Doing it wrong will make you suffer twice: fixing the error handler and fix the error.

### 24 Don’t Rely on “Magic Happens Here” (Alan Griffiths) :+1:
* The word *magic* here is, IMHO, a good example of the Clarke's third law
  >  Any sufficiently advanced technology is indistinguishable from magic (Clarke)
* The IT industry has a very large landscape and is getting only larger. Therefore having experts in the smallest part of it is inevitable. However we shouldn't reach the point where expert in domain A sees domain B as magic, or vice-versa.
* No matter how much different both domains are, each expert is very encouraged to gather minimum knowledge from other domains so that it doesn't look like magic anymore for him.
* How much is minimum? good question! IMHO, if you are able to imagine approximative causes of eventual failures on the foreign domain, you already know the minimum. A developer supposing "low server memory" as root cause for a "Redis server down" passed the magic test. Similarly if a product manager thinks *unit tests* might have caused recent bugs of the last release. It is obviously not the case if a frontend developer thinks the build is "something" that happens to their source code making it small, fast written in some Devops programming language.
  >  You don’t have to understand all the magic that makes your project work, but it doesn’t hurt to understand some of it— or to appreciate someone who understands the bits you don’t.

### 25 Don’t Repeat Yourself (Steve Smith) :+1: :+1:
* Don’t Repeat Yourself (DRY) is probably the most fundamental of all fundamental programming rules.
* We know the **S****O**LID principles. There would be no **S**ingle Responsibility Principle without *DRY*, as duplication will definitely lead to more than one cause to change the code unit. There would also be no **O**pen/Closed principle without *DRY*, as duplication will force any module to be open for modifications.
* There might be situtations when you can trade off DRY for more crucial requirements such as performance and scaling (data redundancy through DB denormalization). The need must be real so that the trade-off makes sense.
* However, IMHO, the DRY principle might be in some situations under double check, specially when we oppose it to other principles such as [The rule of three](https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming)) or the *"Duplication is far cheaper than the wrong abstraction"* principle. Briefly said, DRY will require some kind of abstraction under which the duplication hides, and abstraction requires a certain level of accuracy and expertise so that it can handle the repeated cases without the need to handle missing ones with nasty conditions. There is no free lunch!

### 27 Don’t Touch That Code! (Cal Evans) :+1:
* Developers should **NEVER** do any manual changes on any environment except their local ones. Moreover, they should never have access to production servers, even in situations where a very urgent hotfix is required.
* This rule is good to follow, no doubt. However, IMHO, it comes with costs and needs dedicated manpower and resources, and many companies/startups can't afford that luxury and keep relying on grey areas and shared responsibilities. It is when you grow to big enough company that fine grained responsibilities and stricter border lines are the very welcome.

### 27 Encapsulate Behavior, Not Just State (Einar Landre) :+1:

"Object Zero" (~ Coke Zero) is the trend nowadays, yet, Einar Landre warns us that combining logic and state changes in the same class isn't bad, but rather the standard.  He literally wrote:

> the objects are plain and simple, but not dumb

Objects can change their own states (and should be able to). Foreign classes must communicate through those methods, after all, they constitute its actual interface. This is what Martin Fowler defends in his "Tell don't ask" principle [Tell don't ask](https://martinfowler.com/bliki/TellDontAsk.html)

* IMHO, couple arguments might oppose this principle:

 - Rigidity and tight coupling violating the Open/Closed principle
 - Fragility if deep inheritance comes into play
 - Harder unit test developer experience
 - ORM issues due to eventual "unexpected internal state changes"
 - Eventual concurrency challenges, also due to internal state change.

* A possible compromise, would be the following: keep using dumb `struct` like *POXO* objects, yet, implement encapsulated "services" which know how to validate, mutate and utilize those simple objects the right way.
