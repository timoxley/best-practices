# Programming Best Practices Tidbits

When I hear "JUST BANG OUT CODE THAT WORKS" I think of all the apps I don't use anymore because they gradually lost the ability to iterate.

Source: https://twitter.com/#!/avdi/status/180747721852985344

## Don't do hard things, do easy things.

* Simple is better than complex.
* Complex is better than complicated.
* Flat is better than nested.
* Readability counts.
* If the implementation is hard to explain, it's a bad idea.
* If the implementation is easy to explain, it may be a good idea.

Source: The Zen of Python: http://www.python.org/dev/peps/pep-0020/
(shortlist + title from http://pyvideo.org/video/880/stop-writing-classes)

## Write unit tests.
Every programmer knows they should write tests for
their code. Few do. The universal response to "Why not?" is "I'm
in too much of a hurry." This quickly becomes a vicious cycle- the more pressure you feel, the fewer tests you write. The fewer tests you write, the less productive you are and the less stable your code becomes. The less productive and accurate you are, the more pressure you feel.
Programmers burn out from just such cycles.
Breaking out requires an outside influence. We found the outside influence we needed in a simple testing framework that lets us do a little testing that
makes a big difference.

Source: http://junit.sourceforge.net/doc/testinfected/testing.htm


#### [Without unit tests] You're not refactoring, you're just changing shit. — Hamlet D'Arcy

## To write effective unit tests, you need to write testable code

### Flaw #1: Constructor does Real Work
####Warning Signs
* new keyword in a constructor or at field declaration
* Static method calls in a constructor or at field declaration
* Anything more than field assignment in constructors
* Object not fully initialized after the constructor finishes (watch out forinitialize methods) Control flow (conditional or looping logic) in a constructor
* Control flow (conditional or looping logic) in a constructor
* Code does complex object graph construction inside a constructor rather than using a factory or builder
* Adding or using an initialization block 

### Flaw #2: Digging into Collaborators
#### Warning Signs
* Objects are passed in but never used directly (only used to get access to other objects)
* Law of Demeter violation: method call chain walks an object graph with more than one dot (.) 
* Suspicious names: context, environment, principal, container, or manager

### Flaw #3: Brittle Global State & Singletons
#### Warning Signs
* Adding or using singletons
* Adding or using static fields or static methods Adding or using static initialization blocks Adding or using registries
* Adding or using service locators

###Flaw #4: Class Does Too Much
####Warning Signs

* Summing up what the class does includes the word “and”
* Class would be challenging for new team members to read and quickly “get it” Class has fields that are only used in some methods
* Class has static methods that only operate on parameters

Source: http://misko.hevery.com/code-reviewers-guide/

http://misko.hevery.com/presentations/

## Test-Driven Development with Inversion of Control.

Even if you aren't testing your code, you should write testable code. IoC enables testable code. Inject test-friendly dependencies or mocks at test time, to isolate the unit-under-test.

## Avoid mixing Object Creation with Application Logic

http://misko.hevery.com/2008/09/30/2008/07/08/how-to-think-about-the-new-operator/

## Don't Write Code

Don’t write code (write new code only when everything else fails) is the single most important lesson every developer needs to learn. The amount of duplicate, crappy code (across projects) that exists today is overwhelming. In a lot of cases developers don’t even bother to look around. They just want to write code.

Source: http://blogs.agilefaqs.com/2009/10/19/biggest-stinkers/

## Avoid Code Smells

http://stackoverflow.com/questions/114342/what-are-code-smells-what-is-the-best-way-to-correct-them

## 10 ways NOT to Code

http://www.codfusion.com/blog/post.cfm/how-not-to-code

## Avoid creating technical debt.

"Although immature code may work fine and be completely acceptable to the customer, excess quantities will make a program unmasterable, leading to extreme specialization of programmers and finally an inflexible product. ... A little debt speeds development so long as it is paid back promptly with a rewrite ... *Every minute spent on not-quite-right code counts as interest on that debt.* Entire engineering organizations can be brought to a stand-still under the debt load of an unconsolidated implementation ...”
(Emphasis mine)

Source: http://c2.com/doc/oopsla92.html

http://en.wikipedia.org/wiki/Technical_debt

## Premature optimisation is the root of all evil

"Programmers waste enormous amounts of time thinking about, or worrying about, the speed of noncritical parts of their programs, and these attempts at efficiency actually have a strong negative impact when debugging and maintenance are considered. We should forget about small efficiencies, say about 97% of the time: premature optimization is the root of all evil. Yet we should not pass up our opportunities in that critical 3%."

Source: http://c2.com/cgi/wiki?PrematureOptimization

## Plan, Plan, Plan.

It is much cheaper to do it correctly the first time than to redo it later on.
The sooner a problem is identified and fixed, the cheaper it is to do so.

"The general who wins a battle makes many calculations in his temple before the battle is fought. The general who loses a battle makes but few calculations beforehand. Thus do many calculations lead to victory,
and few calculations to defeat: how much more no calculation at all! It is by attention to this point that I can foresee who is likely to win or lose."

#### "Plans are worthless, planning is invaluable."- Sir Winston Churchill

For this to work, everyone involved has to listen, everyone has to be open, everyone has to be responsive. Or we could keep flailing away with the fucked up attitude that “it has to be this way” because the sacred project plan says it’s this way. Because that really is a lot of fun, isn’t it?


## Refactoring > Rewriting

#### Common Excuses For A Software Rewrite
1. The Code Sucks
2. "We're So Much Smarter Now"
3. We Picked The Wrong Platform/Language

#### Why Rewriting Is (Almost) Never A Good Idea

1. It Will Take Longer Than You Think
2. Markets Change
2. Existing Customers Become Frustrated
3. Refactoring Can Cleanup The Code
4. You Don't Control The Rewrite, It Controls You

http://onstartups.com/tabid/3339/bid/2596/Why-You-Should-Almost-Never-Rewrite-Your-Software.aspx

## Rewriting > Patching
If you are changing more than 25% of a class or method, consider simply rewriting it. You will write the code more cleanly.

## Programming is also Teaching your team
... a team of mediocre, inexperienced coders who work together and write for the benefit of the team has the capability to become a great team, and they can take that learning approach to create other great teams. *It all comes down to whether the team sees its work as simply writing code... or writing with the goal of both code and learning*" 
(Emphasis mine)
http://www.theserverside.com/tt/articles/article.tss?l=ProgrammingisAlsoTeachingYourTeam
(Article itself not that great, but the message I quoted is important.)


### "The most important element of successful software development is learning."
When the entire team meets a certain standard for competence, there is a very large learning surface exposed and the team is able to absorb more information. 
http://weblog.raganwald.com/2007/06/which-theory-first-evidence.html

## "...there are lies, damned lies, and software development estimates."

Software can only partially be designed in advance. ... requirements suffer from observation, that the act of building software causes the requirements to change. ...technical factors cannot be perfectly understood, that only the act of trying to build something with specific components will reveal all of the gotchas and who-knews associated with a chosen technology strategy. ...software design is an iterative process, starting with a best guess that is continually refined with experience.
the normal case for software projects is that tasks are rarely completed exactly as estimated, but that as a project progresses, the aggregate variance from estimates falls.

http://weblog.raganwald.com/2007/06/which-theory-first-evidence.html

Nobody likes to look stupid. If you’re a professional and someone puts you on the spot to answer “how long will this take?” it’s only human to want to provide an answer. Whether you call it professional pride or ego, it’s a powerful driver.
Good IT workers really don’t like saying “I don’t know.” If they say it, they probably mean it. So stop pushing for a definitive answer when one doesn’t exist.It’s perfectly reasonable to want some sort of plan up front. I’m actually one of those funny types who believe up front planning is a necessity. So long as everyone understands an estimate is just that: an estimate. You learn as you go along and discover more detail. So you revise the estimate accordingly.



