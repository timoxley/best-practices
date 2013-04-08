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

## Oubliez les nouvelles fonctionnalités, faîtes la même chose en mieux.

Le problème : il est vite arrivé que l'on perde de vue ce à quoi les utilisateurs tiennent le plus, qui sont la facilité d'utilisation des applications et les fonctionnalités qu'ils utilisent déjà le plus souvent.

– Tim Anderson

[Source](http://www.itjoblog.co.uk/2011/06/making-better-software.html)

## Réinventez la roue
Créer vos propres roues vous donne une profonde appréciation et compréhension de comment les roues "roulent" et ce qui fait une bonne roue.

[Source](http://nodejs.debuggable.com/2011-02-26.txt)

## Ne faîtes pas de choses difficiles, faîtes-en des faciles.

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
Si vous changez plus de 25% de votre classe ou votre méthode, envisagez plutôt de la réécrire. Vous écrirez le code plus clairement.

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


## Acceptez que vous n'avez aucune idée de comment cela va évoluer

La clé est de reconnaître dès le début que vous n'avez aucune idée de comment cela va évoluer. Lorsque l'on accepte que l'on ne sait pas tout, on commence à concevoir le système sur la défensive... Il faudrait passer plus de temps à réfléchir aux interfaces plutôt qu'aux implémentations.

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

### Premier défaut : Le constructeur fait du vrai boulot
#### Signaux d'avertissement
* Nouveau mot clé dans un constructeur ou dans un champ de déclaration
* Appels à une méthode statique dans un constructeur ou dans un champ de déclaration
* N'importe quoi plus gros qu'un champ d'assignement dans les constructeurs
* Un objet avec initialisation incomplète après que le constructeur ait fini (faîtes attention aux méthodes d'initialisation)
* Flux de contrôle (logique conditionnelle ou boucle) dans un constructeur
* Le code fait un graphe de construction d'objet complexe à l'intérieur du constructeur plutôt qu'utiliser une fabrique ou un monteur
* Ajouter ou utiliser un bloc d'initialisation

### Deuxième défaut : Creuser dans les collaborateurs
#### Signaux d'avertissement
* Les objets sont transmis mais jamais utilisés directement (utilisés seulement pour accéder à d'autres objets)
* Violation de la loi de Déméter : la chaîne d'appel de méthode crée un graphe d'objet avec plus d'un point (.)
* Noms suspects : contexte, environnement, principal, conteneur ou gestionnaire *(voir leur traduction anglaise)*

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

Bien que du code immature puisse fonctionner et être parfaitement acceptable pour le client, en abuser rendra un programme incontrôlable. ... Une petite dette accélère le développement jusqu'à ce qu'elle doive être rapidement remboursée par une réécriture ... *Chaque minute passée sur du code "pas tout à fait correct" s'ajoute aux intérêt de cette [dette](http://en.wikipedia.org/wiki/Technical_debt).* Des organisations d'ingénieurie toutes entières peuvent être bloquées sous le poids d'une dette d'implémentation non consolidée. ..." (Souligné par l'auteur)

[Source](http://c2.com/doc/oopsla92.html)


## Une optimisation prématurée est la racine du mal

"Les programmeurs perdent énormément de temps à réfléchir ou à se préoccuper de la rapidité de parties non critiques de leurs programmes, et ces tentatives d'efficacité ont en réalité un impact très négatif lorsque le debug et la maintenance sont pris en compte. Nous devrions abandonner les petites améliorations environ 97% du temps : une optimisation prématurée est la racine du mal. Encore faut-il ne pas laisser filer l'opportunité dans les 3% critiques."

[Source](http://c2.com/cgi/wiki?PrematureOptimization)

## Planifiez, planifiez, planifiez.

Il est moins coûteux de faire correctement la première fois que le refaire plus tard.
Plus tôt un problème est identifié et corrigé, moins il sera nécessaire de s'investir dessus.

"Que chacun se représente les évaluations faites dans le temple, avant les hostilités, comme des mesures : elles disent la victoire lorsqu'elles démontrent que votre force est supérieure à celle de l'ennemi; elles indiquent la défaite lrsqu'elles démontrent qu'il est inférieur en force. Considérez qu'avec de nombreux calculs on peut remporter la victoire, redoutez leur insuffisance. Combien celui n'en fait point a peu de chances de gagner ! C'est grâce à cette méthode que j'examine la situation, et l'issue apparaîtra clairement." (*The Art of War* by Sun Tzu)

#### "Les plans sont sans valeur, la préparation est inestimable."- Sir Winston Churchill

Pour que cela marche, toutes les personnes concernées doivent écouter, tout le monde doit être ouvert et réactif. Ou nous pouvons continuer à aller dans le mur en nous répétant "ça doit être comme ça" parce que le plan *sacré* du projet dit que c'est ainsi. Parce que c'est vraiment éclatant, n'est-ce pas ?

## La programmation c'est aussi apprendre à votre équipe
... Une équipe de développeurs incompétents, inexpérimentés qui travaillent ensemble et écrivent  pour le bien de l'équipe, a la capacité de devenir une grande équipe et ils peuvent itiliser cette méthode d'apprentissage pour créer d'autres bonnes équipes. *Cela résulte du fait que l'équipe voir son travail grâce à une simple écriture de code... Ou bien avec l'objectif du code et de lapprentissage*"
(Souligné par l'auteur)

– Reginald Braithwaite

[Source](http://www.theserverside.com/tt/articles/article.tss?l=ProgrammingisAlsoTeachingYourTeam)

### "L'élément le plus important dans la réussite du développement d'un programme est l'apprentissage"
Quand l'équipe toute entière rencontre un certain standard de compétence, alors apparait une très grande surface d'apprentissage et l'équipe est capable d'absorber plus d'informations.

[Source](http://weblog.raganwald.com/2007/06/which-theory-first-evidence.html)

## "...il y a des mensonges, de lourds mensonges et des estimations de développement de logiciel."

Un logiciel ne peut être conçu à l'avance que partiellement. ... Les besoins souffrent de l'observation que le fait de créer le logiciel les amènent à changer. ...Les facteurs techniques ne peuvent pas être parfaitement compris, c'est seulement en essayant de créer quelque chose avec des composants spécifiques que l'ont découvre tous les défauts imprévus associés à une stratégie technique définie. ...la conception de logiciel est un processus itératif, commençant par une meilleure déduction possible qui est ensuite constamment affinée avec l'expérience. Le cas normal pour des projets logiciels est les tâches s'effectuent rarement telles qu'elles le devaient, mais au fur et à mesure que le projet avance, le total de variations des estimations s'amenuise.

[Source](http://weblog.raganwald.com/2007/06/which-theory-first-evidence.html)

Personne n'aime avoir l'air idiot. Si vous êtes un professionnel et que quelqu'un vous met dans l'embarras en vous demandant "combien de temps ça prendra ?", c'est humain de vouloir être capable de répondre. Que vous appeliez cela de la fierté professionnelle ou de l'égo, c'est un puissant conducteur.
Les informaticiens talentueux n'aiment vraiment pas dire "je ne sais pas". S'ils le disent, ils le pensent très certainement. Alors arrêtez d'exiger une réponse définitive lorsqu'il n'en existe pas. C'est tout à fait raisonnable de vouloir un plan de départ. En réalité je suis moi-même un de ces types qui pensent qu'un plan de départ est nécessaire. Tant que tout le monde comprend ce que représente une estimation : une estimation. Vous apprendrez au fur et à mesure et découvrirez davantage de détails. Vous pourrez alors corriger l'estimation en fonction.


## Votre architecture doit ressembler à votre domaine

Qu'est-ce que l'architecture de votre application vous crie ? Lorsque vous regardez la structure du dossier le plus haut, et les fichiers sources dans le package le plus haut; est-ce qu'ils vous crient système de santé, ou système comptable, ou système de gestion d'inventaire ? Ou crient-ils rails, ou spring/hibernate, ou asp ?

Les architectures ne doivent pas être fournies par les frameworks. Les frameworks sont des outils à utiliser, pas des architectures auxquelles se conformer. Si votre architecture est basée sur des frameworks, alors elle ne peut pas être basée sur votre cas d'utilisation.

– Uncle Bob Martin, "Screaming Architecture"

[Source](http://blog.8thlight.com/uncle-bob/2011/09/30/Screaming-Architecture.html)

## Suivez le principe de X

* N'ajoutez pas de nouvelle fonctionnalité à moins que vous connaissiez une vraie application qui en aura besoin.
* Il est tout aussi important de décider de ce qu'un système n'est pas que de décider de ce qu'il est. Ne répondez pas aux besoins de la terre entière; plutôt, faîtes un système souple pouvant accueillir des besoins additionnels en toute compatibilité.
* La seule chose pire que la généralisation depuis un seul exemple est la généralisation depuis aucun exemple du tout.
* Si un problème n'est pas totalement compris, il vaudrait probablement mieux ne pas lui fournir de solution du tout.
* Si vous pouvez obtenir 90% des effets désirés avec 10% de travail, utilisez la solution la plus simple. (Voir aussi *Le pire est mieux.*)
* Isolez le plus possible la complexité.
* Fournissez des mécanismes plutôt des politiques. En particulier, déléguez au client la politique d'interface.

[Source](http://en.wikipedia.org/wiki/X_Window_System_protocols_and_architecture#Design_principles)


## Suivez les principes d'Unix

"Voici la philosophie d'Unix : écrire des programmes qui font une chose correctement. Écrire des programmes qui fonctionnent ensemble. Écrire des programmes qui gèrent des flux de texte, parce que c'est une interface universelle" - Citation de Doug McIlroy dans Un Quart de Siècle d'Unix [Salus]. Addison-Wesley. 1994. ISBN 0-201-54777-5.

* Règle de la Modularité : écrire des parties simples connectées par des interfaces propres.
* Règle de la Clarté : la clarté est meilleure que l'intelligence.
* Règle de la Composition : concevoir des programmes pouvant être connectés à d'autres programmes.
* Règle de la Séparation : séparer la politique du méchanisme; séparer les interfaces des moteurs.
* Règle de a Simplicité : concevoir pour la simplicité; ajouter de la complexité seulement où il le faut.
* Règle de la Parsimonie : écrire un gros programme seulement quand il est prouvé que rien d'autre ne sera fait.
* Règle de la Transparence : concevoir pour la visibilité et ainsi rendre l'inspection et le debug plus aisés.
* Règle de la Robusticité : la robusticité est l'enfant de la transparence et de la simplicité.
* Règle de la Représentation : inclure la connaissance dans les données pour que la logique du programme puissent être bête et robuste.
* Règle de la Surprise : dans la conception d'interface, toujours faire le moins surprenant possible.
* Règle du Silence : quand un programme n'a rien d'intéressant à dire, il devrait ne rien dire du tout.
* Règle de la Réparation : lorsque vous devez échouer, échouez bruyamment et aussi vite que possible.
* Règle de l'Économie : le temps d'un programmeur vaut cher, le transformer de préférence en temps machine.
* Règle de la Génération : éviter le *fait à la main*, écrire les programmes pour écrire des programmes dès que possible.
* Règle de l'Optimisation : prototyper avant de polir. Faire marcher avant d'optimiser.
* Règle de la Diversité : détruire toutes les reventications de "une seule vraie façon de faire".
* Règle de l'Extensibilité : concevoir pour le futur, parce que ça arrivera plus vite qu'on ne le pense.

– Eric S. Raymond, "L'Art de la Programmation Unix"

[Source](http://www.catb.org/esr/writings/taoup/html/ch01s06.html)
