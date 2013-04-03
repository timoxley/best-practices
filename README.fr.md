# Bonnes pratiques de programmation - Tidbits
### Une liste de citations et paraphrases de développeurs à travers le web.

Utilisez votre propre jugement sur leur application[.](http://www.reddit.com/r/programming/comments/1bcebh/programming_best_practices/c95y6la)

* * *

## Ne jamais créer de grosses applications

Le secret pour créer de grosses applications est de ne jamais en créer de grosses. Décomposez votre application en petites parties. Puis, assemblez celles qui peuvent être testées, de petite taille, sur votre grosse application.

– Justin Meyer, auteur de JavaScript MVC

[Source](http://bitovi.com/blog/2010/11/organizing-a-jquery-application.html)

## La qualité compte

Quand j'entends "BALANCE JUSTE DU CODE QUI MARCHE" je pense à toutes ces applications que je n'utilise plus parce qu'elles ont progressivement perdu la capacité d'évoluer.

– Avdi Grimm

[Source](https://twitter.com/#!/avdi/status/180747721852985344)

## N'écrivez pas de code

Ne pas écrire de code (n'en écrire que quand tout le reste a échoué) est l'unique leçon la plus importante que chaque développeur devrait apprendre. La quantité de code dupliqué, sale (à travers les projets) qui existe aujourd'hui est énorme. La plupart du temps les développeurs ne prennent même pas la peine de regarder autour d'eux. Ils veulent juste écrire du code.

[Source](http://blogs.agilefaqs.com/2009/10/19/biggest-stinkers/)

#### Réduire la quantité de code dans votre projet devrait être un objectif.

"Je déteste le code, et je n'en veux que le moins possible dans notre produit."
– Jack Diederich

[Source](http://pyvideo.org/video/880/stop-writing-classes)

#### Gardez de faibles dépendances
Le vieil adage "ne réinventez pas la roue" ne s'applique pas quand la roue est livrée avec le moteur de locomotive.

[Source](http://www.reddit.com/r/programming/comments/1bcebh/programming_best_practices/c9616mn)

## Arrêtez d'écrire des classes

L'indication "ceci ne devrait pas être une classe" intervient lorsque la classe a deux méthodes, et que l'une d'elles est le constructeur.
À chaque fois que vous voyez ces signes, vous devriez probablement simplement écrire une fonction.

– Jack Diederich

[Source](http://pyvideo.org/video/880/stop-writing-classes)

## Réinventez la roue
Créer vos propres roues vous donne une profonde appréciation et compréhension de comment les roues "roulent" et ce qui fait une bonne roue.

[Source](http://nodejs.debuggable.com/2011-02-26.txt)

## Ne faîtes de de choses difficiles, faîtes-en des faciles.

* Simple est mieux que complexe.
* Complexe est mieux que compliqué.
* Applati est mieux qu'imbriqué.
* La lisibilité compte.
* Si l'implémentation est dure à comprendre, c'est une mauvaise idée.
* Si l'implémentation est facile à comprendre, ça peut être une bonne idée.

– The Zen of Python

[Source](http://www.python.org/dev/peps/pep-0020/)

Présélection de la [présentation de Jack Diederich "Arrêtez d'écrire des classes"](http://pyvideo.org/video/880/stop-writing-classes)

## Réécrire > Factoriser
Si vous changez plus de 25% de votre classe ou votre méthode, envisagez de simplement la réécrire. Vous écrirez le code plus clairement.

## Factoriser > Réécrire

#### Raisons fréquentes pour réécrire un logiciel
1. Le code est mauvais
2. "Nous sommes tellement plus intelligents à présent"
3. Nous avons choisi le/la mauvais(e) langage/plate-forme

#### Pour la réécriture n'est (presque) jamais une bonne idée
1. [Ça prend plus de temps qu'on ne le croit](http://en.wikipedia.org/wiki/Hofstadter's_law)
2. Le marché évolue
2. Les clients existants deviennent frustrés
3. Factoriser peut nettoyer le code
4. Vous ne contrôlez pas la réécriture, c'est elle qui vous contrôle

[Source](http://onstartups.com/tabid/3339/bid/2596/Why-You-Should-Almost-Never-Rewrite-Your-Software.aspx)

## Forget new features, Just do the same stuff better.

The problem: it is too easy to lose sight of what users often care about more, which is the performance and usability of the applications and features they already use most often.

– Tim Anderson

[Source](http://www.itjoblog.co.uk/2011/06/making-better-software.html)


## Accept that you have no idea how this will grow

The key is to acknowledge from the start that you have no idea how this will grow. When you accept that you don't know everything, you begin to design the system defensively... You should spend most of your time thinking about interfaces rather than implementations.

– Nicholas Zakas, author "High-performance JavaScript websites"

[Source](http://radar.oreilly.com/2011/06/big-javascript-apps-teams.html)

[Acknowledgement to Addy Osmani](http://addyosmani.com/largescalejavascript/)

## Avoid Code Smells

[Source](http://www.codinghorror.com/blog/2006/05/code-smells.html)  
[Source](http://web.archive.org/web/20120130234037/http://stackoverflow.com/questions/114342/what-are-code-smells-what-is-the-best-way-to-correct-them)


## Write unit tests.
Every programmer knows they should write tests for
their code. Few do. The universal response to "Why not?" is "I'm
in too much of a hurry." This quickly becomes a vicious cycle- the more pressure you feel, the fewer tests you write. The fewer tests you write, the less productive you are and the less stable your code becomes. The less productive and accurate you are, the more pressure you feel.
Programmers burn out from just such cycles.
Breaking out requires an outside influence. We found the outside influence we needed in a simple testing framework that lets us do a little testing that
makes a big difference.

[Source](http://junit.sourceforge.net/doc/testinfected/testing.htm)


#### [Without unit tests] You're not refactoring, you're just changing shit. — Hamlet D'Arcy

## To write effective unit tests, you need to write testable code

### Flaw #1: Constructor does Real Work
#### Warning Signs
* new keyword in a constructor or at field declaration
* Static method calls in a constructor or at field declaration
* Anything more than field assignment in constructors
* Object not fully initialized after the constructor finishes (watch out for initialize methods)
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
* Adding or using static fields or static methods
* Adding or using static initialization blocks
* Adding or using registries
* Adding or using service locators

### Flaw #4: Class Does Too Much
#### Warning Signs

* Summing up what the class does includes the word “and”
* Class would be challenging for new team members to read and quickly “get it”
* Class has fields that are only used in some methods
* Class has static methods that only operate on parameters

[Source](http://misko.hevery.com/code-reviewers-guide/)

[Source](http://misko.hevery.com/presentations/)

## Test-Driven Development with Inversion of Control.

Even if you aren't testing your code, you should write testable code. IoC enables testable code. Inject test-friendly dependencies or mocks at test time, to isolate the unit-under-test.

## Avoid mixing Object Creation with Application Logic

[Source](http://misko.hevery.com/2008/09/30/2008/07/08/how-to-think-about-the-new-operator/)

## Avoid creating technical debt.

"Although immature code may work fine and be completely acceptable to the customer, excess quantities will make a program unmasterable, leading to extreme specialization of programmers and finally an inflexible product. ... A little debt speeds development so long as it is paid back promptly with a rewrite ... *Every minute spent on not-quite-right code counts as interest on that [debt](http://en.wikipedia.org/wiki/Technical_debt
).* Entire engineering organizations can be brought to a stand-still under the debt load of an unconsolidated implementation ...”
(Emphasis mine)

[Source](http://c2.com/doc/oopsla92.html)


## Premature optimisation is the root of all evil

"Programmers waste enormous amounts of time thinking about, or worrying about, the speed of noncritical parts of their programs, and these attempts at efficiency actually have a strong negative impact when debugging and maintenance are considered. We should forget about small efficiencies, say about 97% of the time: premature optimization is the root of all evil. Yet we should not pass up our opportunities in that critical 3%."

[Source](http://c2.com/cgi/wiki?PrematureOptimization)

## Plan, Plan, Plan.

It is much cheaper to do it correctly the first time than to redo it later on.
The sooner a problem is identified and fixed, the cheaper it is to do so.

"The general who wins a battle makes many calculations in his temple before the battle is fought. The general who loses a battle makes but few calculations beforehand. Thus do many calculations lead to victory,
and few calculations to defeat: how much more no calculation at all! It is by attention to this point that I can foresee who is likely to win or lose."

#### "Plans are worthless, planning is invaluable."- Sir Winston Churchill

For this to work, everyone involved has to listen, everyone has to be open, everyone has to be responsive. Or we could keep flailing away with the fucked up attitude that “it has to be this way” because the sacred project plan says it’s this way. Because that really is a lot of fun, isn’t it?

## Programming is also Teaching your team
... a team of mediocre, inexperienced coders who work together and write for the benefit of the team has the capability to become a great team, and they can take that learning approach to create other great teams. *It all comes down to whether the team sees its work as simply writing code... or writing with the goal of both code and learning*"
(Emphasis mine)

– Reginald Braithwaite

[Source](http://www.theserverside.com/tt/articles/article.tss?l=ProgrammingisAlsoTeachingYourTeam)

### "The most important element of successful software development is learning."
When the entire team meets a certain standard for competence, there is a very large learning surface exposed and the team is able to absorb more information.

[Source](http://weblog.raganwald.com/2007/06/which-theory-first-evidence.html)

## "...there are lies, damned lies, and software development estimates."

Software can only partially be designed in advance. ... requirements suffer from observation, that the act of building software causes the requirements to change. ...technical factors cannot be perfectly understood, that only the act of trying to build something with specific components will reveal all of the gotchas and who-knews associated with a chosen technology strategy. ...software design is an iterative process, starting with a best guess that is continually refined with experience.
the normal case for software projects is that tasks are rarely completed exactly as estimated, but that as a project progresses, the aggregate variance from estimates falls.

[Source](http://weblog.raganwald.com/2007/06/which-theory-first-evidence.html)

Nobody likes to look stupid. If you’re a professional and someone puts you on the spot to answer “how long will this take?” it’s only human to want to provide an answer. Whether you call it professional pride or ego, it’s a powerful driver.
Good IT workers really don’t like saying “I don’t know.” If they say it, they probably mean it. So stop pushing for a definitive answer when one doesn’t exist.It’s perfectly reasonable to want some sort of plan up front. I’m actually one of those funny types who believe up front planning is a necessity. So long as everyone understands an estimate is just that: an estimate. You learn as you go along and discover more detail. So you revise the estimate accordingly.


##Your architecture should resemble your domain

So what does the architecture of your application scream? When you look at the top level directory structure, and the source files in the highest level package; do they scream: health care system, or accounting system, or inventory management system? Or do they scream: rails, or spring/hibernate, or asp?

Architectures should not be supplied by frameworks. Frameworks are tools to be used, not architectures to be conformed to. If your architecture is based on frameworks, then it cannot be based on your use cases.

– Uncle Bob Martin, "Screaming Architecture"

[Source](http://blog.8thlight.com/uncle-bob/2011/09/30/Screaming-Architecture.html)

## Follow the principles of X

* Do not add new functionality unless you know of some real application that will require it.
* It is as important to decide what a system is not as to decide what it is. Do not serve all the world's needs; rather, make the system extensible so that additional needs can be met in an upwardly compatible fashion.
* The only thing worse than generalizing from one example is generalizing from no examples at all.
* If a problem is not completely understood, it is probably best to provide no solution at all.
* If you can get 90 percent of the desired effect for 10 percent of the work, use the simpler solution. (See also Worse is better.)
* Isolate complexity as much as possible.
* Provide mechanism rather than policy. In particular, place user interface policy in the clients' hands.

[Source](http://en.wikipedia.org/wiki/X_Window_System_protocols_and_architecture#Design_principles)


## Follow the principles of Unix

"This is the Unix philosophy: Write programs that do one thing and do it well. Write programs to work together. Write programs to handle text streams, because that is a universal interface" - Doug McIlroy, quoted in A Quarter Century of Unix [Salus]. Addison-Wesley. 1994. ISBN 0-201-54777-5.

* Rule of Modularity: Write simple parts connected by clean interfaces.
* Rule of Clarity: Clarity is better than cleverness.
* Rule of Composition: Design programs to be connected to other programs.
* Rule of Separation: Separate policy from mechanism; separate interfaces from engines.
* Rule of Simplicity: Design for simplicity; add complexity only where you must.
* Rule of Parsimony: Write a big program only when it is clear by demonstration that nothing else will do.
* Rule of Transparency: Design for visibility to make inspection and debugging easier.
* Rule of Robustness: Robustness is the child of transparency and simplicity.
* Rule of Representation: Fold knowledge into data so program logic can be stupid and robust.
* Rule of Least Surprise: In interface design, always do the least surprising thing.
* Rule of Silence: When a program has nothing surprising to say, it should say nothing.
* Rule of Repair: When you must fail, fail noisily and as soon as possible.
* Rule of Economy: Programmer time is expensive; conserve it in preference to machine time.
* Rule of Generation: Avoid hand-hacking; write programs to write programs when you can.
* Rule of Optimization: Prototype before polishing. Get it working before you optimize it.
* Rule of Diversity: Distrust all claims for “one true way”.
* Rule of Extensibility: Design for the future, because it will be here sooner than you think.

– Eric S. Raymond, "The Art of Unix Programming"

[Source](http://www.catb.org/esr/writings/taoup/html/ch01s06.html)
