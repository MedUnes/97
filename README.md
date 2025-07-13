<h1 align="center">
    The annotated 97 <br>
</h1>

<div align="center">

</div>

[![Author](https://img.shields.io/badge/author-@medunes-blue.svg?style=flat-square)](https://twitter.com/medunes2)

## What is it?
* These are my **own** notes/thoughts/annotations on the very famous book "97 Things Every Programmer Should Know".
* I did it for three main purposes:
    * Summarize that valuable information in a more packed size so that I can refer to it and re-read it more often
    * Merge the books information with my own information that I gathered from other sources
    * Share it with people

## Symbols/Typography:

* :+1: /  :+1::+1: /  :+1: :+1: :+1:  represent how much I learned from that particular point (and this is purely personal)
* In case I copy/paste the the authors words, I list them quoted:
> like this
* If the note is not a summary, but rather my own opinion, I format it like this:
  
> [!tip]  
> IMHO this point has potential flaws because ..

## My Notes

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

> [!tip]  
> This is a rephrasal of the [Liskov principle](https://en.wikipedia.org/wiki/Liskov_substitution_principle).

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
### 15- A comment on comments  (Cal Events) :+1: :+1:
* Comments are not evil, they are very welcome, they are first class citizens in the world of programming.
* Do not surrender to indoctrinations of the notoriety of comments. Use them as much as you want as long as you keep explaining your code to yourself and to future programmers coming across it.
* This might sound like a "devil's advocate PoV", if you are do belong to the "clean code" team. The two quotes below are very clear about this:
> Sprinkle your code with relevant comments explaining what the code is supposed to accomplish. - *Cal Events* 

> The proper use of comments is to compensate for our failure to express ourself in code. Note that I used the word failure. I meant it. Comments are always failures. - *Uncle Bob*

### 16- Comment only what the code cannot say  (Kevlin Henney) :+1:
* Unless literally deleted, comments are non-refactorable tech debt and kind of resident flaws that nor compilers neither linters can fix.
* Oppposed to what they were meant to be useful for, comments won't communicate more info for two reasons:
  * The developer's mind flags them as "ambiguous" then systematically puts them under "ignored crap".
  * They can be replcaed by dedicated tools (VCS, real code, and yes: DEL key)
* Write comments if, and only if, you can't replace them by real code. (A rephrasal of "Comment the *why*, not the *what*)
  > Comment what the code cannot say,not simply what it does not say.

### 17- Continous Learning (Clint Shank) :+1:
* Continous learning is good, in software engineering is a must, else you risk your job as the change is fast and the competition is high.
* There are two styles of learning: passive (blogs, mentors, conferences) and active (teaching, coding, blogging)
* A good way to stand out from the crowd, is to dig deeper and deeper your favourite tech-stack, debug and read the source code, up to the point it becomes naked and the magic fades away. The more magic it looks like, the more learning you need.

### 18- Convenience Is Not an -ility (Gregor Hohpe) :+1:
* API is composed of two parts: *"Application Programming"* and *"Interface"*. Your focus should be balanced towards the second part.
* What makes API different from "normal code" it is built to be used by other programmers in other programs.
* You should opt for code that is self-explanatory, optimally without the documentation. Repetition and couple more lines of code shouldn't be a problem in favor of a better DX (Developer Eperience).
* In this context, if you face a trade-off situtation of convenience vs efficiency, convenience vs consistency, or convenience vs elegance, go convenience!
* Take your time, writing an API is like raising a child, you don't usually get a second chance for it.

### 19- Deploy Early and Often (Steve Berczuk) :+1:
* Deployable production environment should come first and certainly not last.
* Releasing to production is not a magic that "those devops" bring to life over night. It should be a part of the development task itself including estimation, refinement, planning, and testing.
* Progressing for a long time on the local environment without any iterations on the production one can end up with bad surprises.
* Sometimes it is too late to fix deep code issues caused by accumulated wrong assumptions about the non-ready production.
* If someone argues about the business value of a production environment preparation, just tell them that the business value only runs on production.

### 20- Don't Ignore That Error (Pete Goodliffe) :+1:
* Ignoring errors under known developers excuses (tough deadline, it won't happen, To Do..) can lead to:
  * Security Issues (the error state is the entrypoint)
  * Ugly code to shut up the error
    
> [!tip]  
> * there should be a pre-agreed minimum level, below which errors can be "safely" ignored, something like the [RFC5424](https://datatracker.ietf.org/doc/html/rfc5424)
> [!tip]  
> * *Don't Ignore That Error* is so similar to this [Zen of Python](https://peps.python.org/pep-0020/#the-zen-of-python):
  
  > Errors should never pass silently.

  > Unless explicitly silenced.

### 21- Don’t Just Learn the Language, Understand Its Culture (Anders Norås) :+1:
* Assuing that nowadays, it is possible to solve almost any programming problem in any programming langauge, why should we learn new langauges?
* The answer is: it is not only about the language, it is about the culture. Yes you can write complete Java application with zero classes and zero interfaces, in a procedural C way, but, why would you?
* If you learn a new language, do not loose its gem: seeing the world with that languages "eyes".
  > It takes more than just learning the syntax to learn a language: you need to understand its culture
  
### 22- Don’t Nail Your Program into the Upright Position (Verity Stob) :+1:
* Choking your program with dozens if *try .. catch* and similar error muters is like hiding cancer with tons of painkillers.
* Write consistent and useful error handlers or avoid that thing completely. Doing it wrong will make you suffer twice: fixing the error handler and fix the error.

### 23- Don’t Rely on “Magic Happens Here” (Alan Griffiths) :+1:
> [!tip]  
> * The word *magic* here is a good example of the Clarke's third law

  >  Any sufficiently advanced technology is indistinguishable from magic (Clarke)
    
* The IT industry has a very large landscape and is getting only larger. Therefore having experts in the smallest part of it is inevitable. However we shouldn't reach the point where expert in domain A sees domain B as magic, or vice-versa.
* No matter how much different both domains are, each expert is very encouraged to gather minimum knowledge from other domains so that it doesn't look like magic anymore for him.

> [!tip]  
> * How much is minimum? good question! if you are able to imagine approximative causes of eventual failures on the foreign domain, you already know the minimum. A developer supposing "low server memory" as root cause for a "Redis server down" passed the magic test. Similarly if a product manager thinks *unit tests* might have caused recent bugs of the last release. It is obviously not the case if a frontend developer thinks the build is "something" that happens to their source code making it small, fast written in some Devops programming language.

  >  You don’t have to understand all the magic that makes your project work, but it doesn’t hurt to understand some of it— or to appreciate someone who understands the bits you don’t.

### 24- Don’t Repeat Yourself (Steve Smith) :+1: :+1:
* Don’t Repeat Yourself (DRY) is probably the most fundamental of all fundamental programming rules.
* We know the **S****O**LID principles. There would be no **S**ingle Responsibility Principle without *DRY*, as duplication will definitely lead to more than one cause to change the code unit. There would also be no **O**pen/Closed principle without *DRY*, as duplication will force any module to be open for modifications.
* There might be situtations when you can trade off DRY for more crucial requirements such as performance and scaling (data redundancy through DB denormalization). The need must be real so that the trade-off makes sense.
> [!tip]  
> * However, the DRY principle might be in some situations under double check, specially when we oppose it to other principles such as [The rule of three](https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming)) or the *"Duplication is far cheaper than the wrong abstraction"* principle. Briefly said, DRY will require some kind of abstraction under which the duplication hides, and abstraction requires a certain level of accuracy and expertise so that it can handle the repeated cases without the need to handle missing ones with nasty conditions. There is no free lunch!

### 25- Don’t Touch That Code! (Cal Evans) :+1:
* Developers should **NEVER** do any manual changes on any environment except their local ones. Moreover, they should never have access to production servers, even in situations where a very urgent hotfix is required.
> [!tip]  
> * This rule is good to follow, no doubt. However, it comes with costs and needs dedicated manpower and resources, and many companies/startups can't afford that luxury and keep relying on grey areas and shared responsibilities. It is when you grow to big enough company that fine grained responsibilities and stricter border lines are the very welcome.

### 26- Encapsulate Behavior, Not Just State (Einar Landre) :+1: :+1:

* "Object Zero" (~ Coke Zero) is the trend nowadays, yet, Einar Landre warns us that combining logic and state changes in the same class isn't bad, but rather the standard.  He literally wrote:
  
> the objects are plain and simple, but not dumb
* Objects can change their own states (and should be able to). Foreign classes must communicate through those methods, after all, they constitute its actual interface. This is what Martin Fowler defends in his [Tell don't ask principle](https://martinfowler.com/bliki/TellDontAsk.html)

> [!tip]  
> Couple arguments might oppose this principle:
>  * Rigidity and tight coupling violating the Open/Closed principle
>  * Fragility if deep inheritance comes into play
>  * Harder unit test developer experience
>  * ORM issues due to eventual "unexpected internal state changes"
>  * Eventual concurrency challenges, also due to internal state change.

> [!tip]  
> A possible compromise, would be the following: keep using dumb `struct` like *POXO* objects, yet, implement encapsulated "services" which know how to validate, mutate and utilize those simple objects the right way.

### 27- Floating-Point Numbers Aren’t Real (Chuck Allison) :+1: :+1: :+1:
* *infinitesimal* is an abstract math concept that doesn't exist in the machine's world. The "smallest" unit is known as the *machine epsilon* defined by: ```ɛ = 2^(1-p), where p is the precision (24 for float, 53 for double)```
* Keeping this in mind is important when trying to find an acceptable small enough value for equations, else you'll loop forver in vain!
* Another trap, konw as the **smearing problem** happens when the difference in scale between the numbers is too great, the smaller number might not affect the total at all. This can lead to inaccuracies in calculations where you expect these small additions to make a difference. the floating point representation can't accurately capture the small change, and over time, these inaccuracies accumulate and might diverge to infinity.
* As these errors might be devastating in contexts such as finance, it makes always sense to rely on dedicated decimal classes almost every popular programming language has. Even if your own implementations might be more effecient:
> efficiency is worthless without accuracy.

### 28- Fulfill Your Ambitions with Open Source (Richard Monson-Haefel) :+1: :+1:
* "Cutting-edge technologies, green-field projects, best practices, and world-valuable solutions fulfilling your beliefs? Unfortunately, the majority of the daily work of software developers does not adhere to their dreams. Instead, they wake up in the morning to monitor yesterday's releases or fix a couple of bugs and write corresponding unit tests.

* What's the escape? Open Source. Besides the high probability of finding your tailor-made project for maximum enthusiasm, open-source projects can offer you the following benefits:

    * Leave your fingerprint on world-class projects.
    * Learn from the world's best developers and gain deeper insights into the culture of your favorite tech stack community.
    * Make valuable friends for fun and profit.
* Everything good comes with a price: you might need to be prepared for a few commitments, such as sacrificing some of your free time for free, or starting the journey by writing unit tests or documentation for your beloved open-source project."

### 29- The Golden Rule of API Design (Michael Feathers) :+1: :+1:
* APIs (not Web APIs, but rather public vendor packages) should be treated as very special code base.
* Writing curated unit tests is crucial, mandatory but, unfortunately, not enough.
* "Locking" your classes with ant-inheritance language keywords (```final```, ```static```, ```sealed```) is also good but not enough.
* The golden rule here is to "impersonate" you API's user and see if you would encounter problems while using it the weirdest way. How can we guess those strange use cases: Unit Tests!
> It’s not enough to write tests for an API you develop; you have to write unit tests for code that uses your API.

### 30- The Guru Myth (Ryan Brush) :+1:
* A Guru is someone who has dedicated years to analyzing and solving problems. They likely possess high intellectual abilities and immense enthusiasm. However, they are not magicians. When seeking their support, provide detailed information and possibly suggest solutions.
* Moreover, elevating experts to a 'Guru' status can harm the industry by creating an image of untouchable idols.
> [!tip]  
> Slow down, beware of arrogance and premature claims of seniority. Being rude to domain experts suggests a 0.01% chance you're a genius and a 99.99% chance you're foolishly risking an early career setback."

### 31- Hard Work Does Not Pay Off (Olve Maudal) :+1: :+1:
* Overworking doesn't necessarily lead to career advancement, personal development, productivity, or success.
* True growth stems from effectively utilizing your free time in activities like workshops, conferences, reading, and networking.
> Act like a professional: prepare, effect, observe, reflect, and change.

> [!tip]  
> However, there are two exceptions to this rule: Firstly, if your job already involves activities you'd typically reserve for free time, such as working on innovative projects in a startup environment. This can provide ample opportunities for personal growth. Secondly, tackling challenging tasks like bug fixing can often be more enriching than attending numerous leisurely conferences. Striking a balance between these two approaches is key.

### 32- How to Use a Bug Tracker (Matt Doar) :+1:
* A bug report says something about the reporter's seniority and "developer's honor", so do it well.
* Your bug report should follow the *What/Why/How* pattern:
  * What happened (context, data, dumps..)
  * Why it happened (your two cents about the root cause)
  * How it happened: the reproduction scenario
    
> a bug is not a standard unit of work any more than a line of code is a precise measurement of effort.

### 33- Improve Code by Removing It (Pete Goodliffe) :+1:
* If your codebase is backed by a solid test suite, involve your Project Manager in couple sessions for a removal of all unnecessary features. Yes, Legacy code often accumulates irrelevant YAGNI breaches..

> One of my most productive days was throwing away 1000 lines of code. (Ken Thompson)
Install Me Marcus Baker

### 34- Install Me (Marcus Baker) :+1:
* When launching products, ensure your landing page is concise and direct.
* You typically have a brief window, around three seconds, to convince visitors that your product addresses their needs, not yours. 
* Any hint of dishonesty, like pushing unwanted downloads, spamming emails, or deceptive practices, can lead to permanent distrust. The customer might not only reject your product but also spread negative feedback or even write a critical blog post.

> if the tutorial mentions my problem, I’ll cheer up.

### 35- Install Me (Marcus Baker) :+1:
* When launching products, ensure your landing page is concise and direct.
* You typically have a brief window, around three seconds, to convince visitors that your product addresses their needs, not yours. 
* Any hint of dishonesty, like pushing unwanted downloads, spamming emails, or deceptive practices, can lead to permanent distrust. The customer might not only reject your product but also spread negative feedback or even write a critical blog post.

> if the tutorial mentions my problem, I’ll cheer up.

### 36- Interprocess Communication Affects Application Response Time (Randy Stafford) :+1: :+1:
* What's the problem with slow software?
> We feel as if the software is wasting our time and affecting our productivity.

* Avoid getting overly absorbed in minor, abstract software design details while chasing perfect performance.
* Always remember that your clean-code runs on a machine and an operating system.
* Speed bottlenecks can arise from external sources like databases, third-party web APIs, or storage services.
* Although you can't alter the internals of these external systems, you often have control over how you manage data transmission to and from them: caching, batching, smart-fetching..
* Ways to improve IPC-to-stimilus ratio: parsimony, concurrency and caching. Additionally, never take your framework and/or vendor solutions as granted specially if they are involved in IPC ( you there ORM, I see you..)
> [!tip]  
> Running clean code on a dirty machine is like serving healthy food in an infected dish.

### 37- Keep the Build Clean (Johannes Brodwall) :+1:
* Zero Tolerance for Build Warnings: Enforce a strict policy where the build process must complete without any warnings. This is non-negotiable and crucial for maintaining code quality.
* Team Consensus on Warning Relevance: If you believe certain warnings are irrelevant, don't ignore them silently. Instead, bring them up for discussion with your team. Upon agreement, these warnings can be explicitly disabled in the build rules.
* Preventing Codebase Degradation: Adhering to this approach aligns with the principles of the [Broken Windows Theory](https://en.wikipedia.org/wiki/Broken_windows_theory). It emphasizes that overlooking minor issues (like build warnings) can lead to a gradual decline in standards, eventually resulting in significant deterioration of the codebase. By maintaining strict standards from the onset, the overall quality and integrity of the code are preserved.

### 38- Know How to Use Command-Line Tools (Carroll Robinson) :+1:
* While GUI tools like IDE plugins are convenient, they can become dependencies that limit deeper understanding. It's important to recognize that many functions they provide can be effectively performed using command-line tools such as grep, sort, and Makefiles. Trying out these CLI tools can be a valuable first step before relying on GUI 'black boxes.'

* After gaining experience with command-line interfaces, you'll be in a better position to choose between continuing with CLI or returning to GUI tools. Even if you opt for GUI, your CLI experience will give you a deeper understanding of the processes involved.

> [!tip]  
> This approach aligns with the Japanese martial arts principle of [Shuhari (守破離)](https://fr.wikipedia.org/wiki/Shuhari), emphasizing the journey from adhering to traditional practices (Shu), to breaking away (Ha), and finally to transcending (Ri).

### 39- Know Well More Than Two Programming Languages (Russel Winder) :+1:
* Mastering various programming paradigms enhances expertise.Diverse languages offer unique problem-solving approaches.
* Exploring different programming languages, even while primarily using one in your daily work, provides a unique perspective on problem-solving that's not typically available to those accustomed to a single-language ecosystem.

> cross-fertilization is at the core of expertise

### 40- Know Your IDE (Heinz Kabutz) :-1:
* The evolution of programming environments: From basic text editors in the 1980s to modern Integrated Development Environments (IDEs) with advanced features like automated refactoring and style rule enforcement, highlighting the ease of use but also the risk of not fully mastering these tools.

### 41- Know Your Limits (Greg Colvin) :+1: :+1:
* Recognizing the orders of magnitude in machine-level access times and capacities is crucial. Coupled with an understanding of abstract time/space complexity, it safeguards against inadvertently making poor design choices. Always remeber: infinite resources do only exist in theoretical computer science books.

| Storage     | Access time | Capacity |
|-------------|-------------|----------|
| Register    | < 1 ns      | 64 b     |
| L1 cache    | 1 ns        | 64 KB    |
| L2 cache    | 4 ns        | 8 MB     |
| RAM         | 20 ns       | 32 GB    |
| Disk        | 10 ms       | 10 TB    |
| LAN         | 20 ms       | > 1 PB   |
| Internet    | 100 ms      | > 1 ZB   |

> Complexity analysis is measured in terms of an abstract machine, but software runs on real machines.

### 42- Know Your Next Commit Dan (Bergh Johnsson) :+1:
* Clear, incremental tasks prevent speculative coding, unlike vague, larger tasks that risk poor commits.
> [!tip]  
> Adhering to strict Scrum rules will make you definitely know your next commit very well.

### 43- Large, Interconnected Data Belongs to a Database (Diomidis Spinellis) :+1:
* SQL simplifies data manipulation and querying, supports declarative constraints for data integrity, and allows easy scaling and multi-language development.
> [!tip]  
> RDBMS aren't a free ride. Understand their mechanics, study the vendor docs, and grasp their limitations. Also, using YAML or JSON files could suit your MVP better before you truly require an RDBMS.

### 44- Learn Foreign Languages (Klaus Marquardt) :+1:
* Besides the "Machine language", programmers are encouraged to learn couple "foreign languages":
    * Their mother tongue: be fluent in it.
    * Foreign human spoken languages
    * Domain Specific Languages (DSL) of the stakeholdes: Marketing, Legal, and  Sales jargons

> [!tip]  
> When you hit a plateau in your technical skills, mastering soft skills becomes key for your growth.

### 45- Learn to Estimate (Giovanni Asproni) :+1:
* Often, managers confuse estimates with commitments, leading to unrealistic project expectations; understanding and clarifying these concepts is crucial for project success.

> [!tip]  
> Again, Scrum is your way to go. Adhering to [Rough Order of Magnitude (ROM)](https://project-management.info/rom-rough-order-of-magnitude/) such as [Fibonacci Sizing](https://www.scrum.org/resources/blog/practical-fibonacci-beginners-guide-relative-sizing) or T-Shirt Sizing are good techniques to separate commitments from estimates.

> “The primary purpose of software estimation is not to predict a project’s outcome; it is to determine whether a project’s targets are realistic enough to allow the project to be controlled to meet them.” (Steve McConnell)

### 46- Let Your Project Speak for Itself (Daniel Lindner) :+1: :+1:
* [Extreme Feedback Devices](https://www.linkedin.com/pulse/extreme-feedback-devices-xfd-thomas-hartmann/) could actually be a good idea:
  * Being fun and creative, it can bring motivation and empower team building
  * Ensure end customers use stable products and get notified in real life about any inconveniences.

> [!tip]  
> On the long run, XFD might have negative impacts on developers minds.  
> Developers need frequent breaks from the digital world's stress to the peace of the real world (coffee, walk, ping-pong), while XFD will only build a permanent joint between the two worlds. 

### 47- The Linker Is Not a Magical Program (Walter Bright) :-1:
* A linker is not a magician, rather a relatively simple program achieving the following: concatenating object files, resolving symbol references, and generating executables, often confused due to complex file formats.

### 48- The Longevity of Interim Solutions (Klaus Marquardt) :+1 :+1: :+1:

* Interim projects usually meet stakeholder expectations, reducing the likelihood of revisions or upgrades unless mandated by rigorous quality standards. 
* As a developer, it's often more practical to avoid overexerting yourself on these projects unless you possess the necessary authority to make significant changes.

> May you be granted the serenity to accept the things you cannot change, the courage to change the things you can, and the wisdom to know the difference

### 49- Make the Invisible More Visible (Jon Jagger) 👍
> Software and the process of developing it can be, to paraphrase Douglas Adams, *mostly invisible*

* Living under the shadow can seriously endanger the lifecycle of software development for both developers and stakeholders.

* Failing to meet deadlines or expectations can be hard to justify, especially when the unexpected results are caused by the typical "bug-fixing" capacity blackholes.

* Developers should aim for transparency in communicating progress and blockers in real time to avoid the consequences of eventual invisibility.

> [!tip]  
> Following modern/de facto software engineering best practices on both the technical side (testing, CI/CD, code reviews, etc.) and management side (Agile) will empirically save you from all the "invisible syndrome" effects without you even being aware of it.

### 50- Message Passing Leads to Better Scalability in Parallel Systems (Russel Winder) 👍 👍

* When it comes to concurrency and parallelism shared memory is the mother of all sins: race conditions, deadlocks and all the crew.
*Embracing message passing and process models offers a radical solution to these problems. However, as long as mainstream programming languages like C, C++, and Java dominate system programming, developers will continue grappling with the pitfalls of shared memory.

> [!tip]  
> Nowadays, Rust stands out as a system programming language that effectively addresses these issues, demonstrating its prowess in modern computing environments.

### 51- A Message to the Future (Linda Rising) 👍👎

* "*Smart Developers Syndrome*": This refers to the tendency of some developers to overcomplicate solutions in order to impress others. Not only is this approach detrimental, but it also complicates collaboration within software development teams. As you delve deeper into the field of software engineering, you'll find how much the *KISS* principle (Keep It Simple Stupid) is valued among community members.

> [!tip]  
> "Simplicity is the ultimate sophistication." (Leonardo da Vinci)

### 52- Missing Opportunities for Polymorphism (Kirk Pepperdine) 👎

> [!tip]  
> In the context of *OOP*, this equation is always valid:
> 
>      `logic switch + object type --> interfaces + strategy pattern` 
