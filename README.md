<h1 align="center"> 
<br>
    <img src="https://github.com/medunes/97/blob/master/logo.jog" width="200">
</h1>
<h5>Notes on book: "97 things every programmer should know</h5>
[![Author](https://img.shields.io/badge/author-@medunes-blue.svg?style=flat-square)](https://twitter.com/medunes2)

<br>

### Act with prudence (Seb Rose)
* Whenever you implment solutions introducing technical debts, make sure you keep track of that. 
* Once done, estimate the cost of this tech-debt and include it in your "pricing"

### Apply Functional Programming Principles (Edward Garson)
* Always fight for pure functions: functions which do not mutate data
* OOP design patterns, principles and best practices (for instance TDD) try to reduce the number of **random** context
were "weird" mutations might happen. Functional programming radically solves this problem.

### Ask, “What Would the User Do?” (You Are Not the User) (Giles Kolborne) ++

* Users think differently than programmers: this is a fact
* A good approach to "explore" their minds is to ask them to perform simple tasks ** in a non-technical words**
[*User Story*? ] (ex:calculate the expenses), and watch how they do them.
* Usually all or almost all users turn around a core behavior, this is your takeaway.
* Trap N.1: Avoid discussions where the topic is "so we suppose the users should do this and that"
* Trap N.2: Watch out what users say they need, only trust what users "truly" need by watching them.
* Trap N.3: Do not lose your time "forcing" users do something your way, they will always use their "weird" ways.


### Automate Your Coding Standard (Filip van Laenen)

* There are mature and widely accepted tools which guarantee coding standards and most of those boring repetitive tasks
aimed to keeping the codebase at a minimal standard.
* Hints: linters, static code analyzers, code coverage, type coverage, cognitive complexity, mess detectors..
* If you include the following two practices in your team's discipline (or self-disciple), you already close the door
against a huge amount of human conflicts, technical debts and management delays:
    * Agree on a set of rules, **beforehand**
    * Invest time to include all of these rules in an automated process that **breaks** the build if not applied
* It is **never** a waste of time or money to dedicate resources for correctly building and implementing reusable
pipelines for faster incorporation in all projects.

### 