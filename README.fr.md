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

## Oubliez les nouvelles fonctionnalités, faîtes juste la même chose en mieux.

Le problème : il est vite arrivé que l'on perde de vue ce à quoi les utilisateurs tiennent le plus, qui sont la facilité d'utilisation des applications et les fonctionnalités qu'ils utilisent déjà le plus souvent.

– Tim Anderson

[Source](http://www.itjoblog.co.uk/2011/06/making-better-software.html)


## Acceptez que vous n'avez aucune idée de comment cela va évoluer

La clé est de reconnaître dès le début que vous n'avez aucune idée de comment cela va évoluer. Lorsque l'on acceptez que l'on ne savez pas tout, on commence à concevoir le système sur la défensive... Il faudrait passer plus de temps à réfléchir aux interfaces plutôt qu'aux implémentations.

– Nicholas Zakas, auteur de "High-performance JavaScript websites"

[Source](http://radar.oreilly.com/2011/06/big-javascript-apps-teams.html)

[Renvoi vers Addy Osmani](http://addyosmani.com/largescalejavascript/)

## Évitez le code sale

[Source](http://www.codinghorror.com/blog/2006/05/code-smells.html)
[Source](http://web.archive.org/web/20120130234037/http://stackoverflow.com/questions/114342/what-are-code-smells-what-is-the-best-way-to-correct-them)


## Écrivez des tests unitaires.

Tous les programmeurs savent qu'ils devraient écrire des tests pour leur code. Peu le font. La réponse universelle à "Pourquoi pas ?" est "Je suis à la bourre." Cela devient rapidement un cercle vicieux -plus la pression augmente, moins on écrit de tests. Moins on écrit de tests, moins on est productif et moins stable devient notre code. Moins on est productif et précis, plus on a la pression. Les programmeurs s'épuisent dans de tels cycles. S'en sortir demande une aide extérieure. On trouve cette aide extérieure dont on a besoin dans un simple framework de test qui nous permet d'écrire un peu tests qui font un grande différence.

[Source](http://junit.sourceforge.net/doc/testinfected/testing.htm)


#### [Sans tests unitaires] Vous ne factorisez pas, vous remuez juste la merde. — Hamlet D'Arcy

## Pour écrire des tests unitaires efficaces, vous avez besoin d'écrire du code qui peut être testé

### Premier défaut : Le constructeur marche vraiment
#### Signaux d'avertissement
* nouveau mot clé dans un constructeur ou dans un champ de déclaration
* Appels à une méthode statique dans un constructeur ou dans un champ de déclaration
* N'importe quoi plus qu'un champ d'assignement dans les constructeurs
* Un objet avec initialisation incomplète après que le constructeur ait fini (faîtes attention aux méthodes d'initialisation)
* Flux de contrôle (logique conditionnelle ou boucle) dans un constructeur
* Le code fait un graphe de construction d'objet complexe à l'intérieur du constructeur plutôt qu'utiliser une fabrique ou un monteur
* Ajouter ou utiliser un bloc d'initialisation

### Deuxième défaut : Creuser dans les collaborateurs
#### Signaux d'avertissement
* Les objets sont transmis mais jamais utilisés directement (utilisés seulement pour accéder à d'autres objets)
* Violation de la loi de Déméter : la chaîne d'appel de méthode créé un graphe d'objet avec plus d'un point (.)
* Noms suspects : contexte, environnement, principal, conteneur ou gestionnaire

### Troisième défaut : État global et singleton fragiles
#### Signaux d'avertissement
* Ajouter ou utiliser des singletons
* Ajouter ou utiliser des champs statiques ou des méthodes statiques
* Ajouter ou utiliser des blocs d'initialisation statiques
* Ajouter ou utiliser des registres
* Ajouter ou utiliser des repères de service

### Quatrième défaut : Les classes en font trop
#### Signaux d'avertissement
* Résumer ce que la classe fait en incluant le mot "et"
* La classe est difficile à lire et à comprendre rapidement pour les nouveaux membres de l'équipe
* La classe a des champs qui ne sont utilisés que dans certaines méthodes
* La classe a des méthodes statiques qui ne fonctionnent qu'avec des paramètres

[Source](http://misko.hevery.com/code-reviewers-guide/)

[Source](http://misko.hevery.com/presentations/)

## Développement piloté par les tests avec Inversion de contrôle.

Même si vous ne testez pas votre code, vous devez écrire du code capable d'être testé. L'Inversion de contrôle permet d'écrire du code testable. Injectez des dépendances favorables aux tests ou des objets factices durant la période de test, pour isoler les parties en cours de test.

## Évitez de mélanger la création d'objet avec la logique de l'application

[Source](http://misko.hevery.com/2008/09/30/2008/07/08/how-to-think-about-the-new-operator/)

## Éviter de créer une dette technique.

Bien que du code immature puisse fonctionner et être parfaitement accepetable pour le client, en abuser rendra un programme incontrôlable. ... Une petite dette accélère le développement jusqu'à ce qu'elle doive être rapidement remboursée par une réécriture ... *Chaque minute passée sur du code "pas tout à fait correct" s'ajoute aux intérêt de cette [dette](http://en.wikipedia.org/wiki/Technical_debt).* Des organisations d'ingénieurie toutes entières peuvent être bloquées sous le poids d'une dette d'implémentation non consolidée. ..." (Souligné par l'auteur)

[Source](http://c2.com/doc/oopsla92.html)


## Une optimisation prématurée est la racine du mal

"Les programmeurs perdent énormément de temps à réfléchir ou à se préoccuper de la rapidité de parties non critiques de leurs programmes, et ces tentatives d'efficacité ont en réalité un impact très négatif lorsque de debug et la maintenance sont pris en compte. Nous devrions abandonner les petites améliorations environ 97% du temps : une optimisation prématurée est la racine du mal. Encore faut-il ne pas laisser filer l'opportunité dans les 3% critiques."

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
