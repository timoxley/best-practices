# Mejores Pr&aacute;cticas de la Programaci&oacute;n - Tidbits
### Una colecci&oacute;n de citas y frases obtenidos de la web para programadores

Utilice su propio juicio en su aplicaci&oacute;n.

* * *

## Nunca construyas aplicaciones grandes

El secreto para construir aplicaciones grandes es nunca construir aplicaciones grandes. Rompe tus aplicaciones en piezas m&aacute;s pequeñas. Entonces, ensambla esas piezas del tamaño de un mordizco que pueden ponerse a prueba, dentro de tu aplicaci&oacute;n grande.

- Justin Meyer, autor de *JavaScriptMVC*.

[Fuente](http://bitovi.com/blog/2010/11/organizing-a-jquery-application.html).

## La calidad importa

Cuando escucho "¡S&Oacute;LO LIBERA DE UNA VEZ EL C&Oacute;DIGO QUE YA FUNCIONA!" pienso en todas las aplicaciones que dej&eacute; de usar porque gradualmente perdieron la habilidad de iterar.

- Avdi Grimm

[Fuente](https://twitter.com/#!/avdi/status/180747721852985344).

## No escribas c&oacute;digo

No escribas c&oacute;digo (escribe nuevo c&oacute;digo solamente cuando todo lo dem&aacute;s falle) es la lecci&oacute;n m&aacute;s importante que todo desarrollador deber&iacute;a aprender. La cantidad de c&oacute;digo duplicado y basura que existe (en todos los proyectos) es abrumadora. En muchos casos los desarrolladores ni se molestan en echar un vistazo. Lo único que quieren es escribir c&oacute;digo.

[Fuente](http://blogs.agilefaqs.com/2009/10/19/biggest-stinkers)

#### Reducir la cantidad de c&oacute;digo en tu producto deber&iacute;a ser una meta

"Odio el c&oacute;digo, y quiero tan poco c&oacute;digo como sea posible en nuestro producto."

- Jack Diederich

[Fuente](http://pyvideo.org/video/880/stop-writing-classes)

#### Mant&eacute;n las dependencias al m&iacute;nimo

El viejo dicho "No reinventes la rueda" no aplica cuando la rueda es del motor de una locomotora.

[Fuente](http://www.reddit.com/r/programming/comments/1bcebh/programming_best_practices/c9616mn)

## Deja de escribir clases

La señal de que "esto no deber&iacute;a ser una clase" es cuando la clase tiene dos m&eacute;todos, y uno de ellos es el constructor. Cualquier rato que veas estas señales, significa que probablemente deber&iacute;as haber escrito s&oacute;lo una funci&oacute;n.

Jack Diederich

[Fuente](http://pyvideo.org/video/880/stop-writing-classes)

## Olvida nuevas funcionalidades, simplemente haz lo mismo pero mejor

El problema: es muy f&aacute;cil perder de vista lo que m&aacute;s importa a los usuarios, que es el rendimiento y la usabilidad de las aplicaciones y las funcionalidades que usan m&aacute;s a menudo.

Tim Anderson

[Fuente](http://www.itjoblog.co.uk/2011/06/making-better-software.html)

## Reinventa la rueda

Inventar tus propias ruedas te da un mayor aprecio y entendimiento de c&oacute;mo funcionan las ruedas y qu&eacute; hace que una sea buena.

[Fuente](http://nodejs.debuggable.com/2011-02-26.txt)

## No hagas cosas dif&iacute;ciles, haz cosas sencillas

* Simple es mejor que complejo.
* Complejo es mejor que complicado.
* Plano es mejor que anidado.
* La legibilidad cuenta.
* Si la implementaci&oacute;n es dif&iacute;cil de explicar, es una mala idea.
* Si la implementaci&oacute;n es f&aacute;cil de explicar, puede que sea una buena idea.

- El Zen de Python

[Fuente](http://www.python.org/dev/peps/pep-0020/)

## Reescribir > Refactorizar

Si vas a cambiar m&aacute;s del 25% de una clase o m&eacute;todo, considera simplemente reescribirlo. Escribir&aacute;s c&oacute;digo m&aacute;s limpio.

## Refactorizar > Reescribir

#### Excusas comunes para reescribir software

1. El c&oacute;digo apesta
2. "Ahora somos mucho m&aacute;s listos"
3. Escogimos la plataforma/lenguaje equivocado

#### Por qu&eacute; reescribir (casi) nunca es una buena idea 

1. [Tardar&aacute; m&aacute;s de lo que piensas](http://en.wikipedia.org/wiki/Hofstadter's_law)
2. Los mercados cambian
2. Los clientes existentes se frustran
3. Refactorizar puede limpiar el c&oacute;digo
4. No controlas la reescritura, ella te controla a ti

[Fuente](http://onstartups.com/tabid/3339/bid/2596/Why-You-Should-Almost-Never-Rewrite-Your-Software.aspx)

## Acepta que no tienes idea de c&oacute;mo esto va a crecer

La clave es reconocer desde el principio que no tienes idea de c&oacute;mo esto va a crecer. Cuando aceptes que no lo sabes todo, empezar&aacute;s a diseñar el sistema defensivamente... Deber&iacute;as invertir la mayor parte de tu tiempo en pensando en interfaces en vez de implementaciones.

- Nicholas Zakas, autor de *High-performance JavaScript websites*

[Fuente](http://radar.oreilly.com/2011/06/big-javascript-apps-teams.html)

[Reconocimiento a Addy Osmani](http://addyosmani.com/largescalejavascript/)

## Evita c&oacute;digo que apesta

[Fuente](http://www.codinghorror.com/blog/2006/05/code-smells.html)  

[Fuente](http://web.archive.org/web/20120130234037/http://stackoverflow.com/questions/114342/what-are-code-smells-what-is-the-best-way-to-correct-them)

## Escribe pruebas unitarias

Todo programador sabe que deber&iacute;a escribir tests para su c&oacute;digo. Pocos lo hacen. La respuesta universal al "¿Por qu&eacute; no?" es "Tengo mucha prisa." R&aacute;pidamente esto se convierte en un c&iacute;rculo vicioso. Cuanta m&aacute;s presi&oacute;n sientas, menos pruebas escribir&aacute;s. Entre menos pruebas escribas, ser&aacute;s menos productivo y tu c&oacute;digo se volver&aacute; menos estable. Entre menos productivo seas, mayor presi&oacute;n sentir&aacute;s. Los programadores se desgastan con esos ciclos. Romperlos requiere de una influencia externa. Encontramos esa influencia externa en un simple framework de pruebas que nos deja hacer pequeñas pruebas que hacen una gran diferencia.

[Fuente](http://junit.sourceforge.net/doc/testinfected/testing.htm)

#### [Sin los tests unitarios] No est&aacute;s refactorizando, s&oacute;lo est&aacute;s cambiando mierda. — Hamlet D'Arcy

## Para escribir pruebas unitarias efectivas, debes escribir c&oacute;digo que se pueda probar

### Flaw #1: El constructor hace trabajo real
#### Se&ntilde;ales de alerta

* Existe `new` en un constructor o en la declaraci&oacute;n de un atributo.
* Static method calls in a constructor or at field declaration
* Se hace algo m&aacute;s que solo asignar en los constructores.
* El objeot no esta completamente inicializado cuando el constructor termina (cuidado con los m&eacute;todos 'para inicializar')
* Control de flujo en un constructor (conditional or looping logic)
* Code does complex object graph construction inside a constructor rather than using a factory or builder
* Adding or using an initialization block 

### Flaw #2: Digging into Collaborators
#### Se&ntilde;ales de alerta

* Objects are passed in but never used directly (only used to get access to other objects)
* Law of Demeter violation: method call chain walks an object graph with more than one dot (.)
* Suspicious names: context, environment, principal, container, or manager

### Flaw #3: Brittle Global State & Singletons
#### Se&ntilde;ales de alerta

* Adding or using singletons
* Adding or using static fields or static methods
* Adding or using static initialization blocks
* Adding or using registries
* Adding or using service locators

###Flaw #4: La clase hace demasiado
#### Se&ntilde;ales de alerta

* Summing up what the class does includes the word “and”
* Class would be challenging for new team members to read and quickly “get it”
* Class has fields that are only used in some methods
* Class has static methods that only operate on parameters

[Fuente](http://misko.hevery.com/code-reviewers-guide/)

[Fuente](http://misko.hevery.com/presentations/)

## Test-Driven Development with Inversion of Control.

Even if you aren't testing your code, you should write testable code. IoC enables testable code. Inject test-friendly dependencies or mocks at test time, to isolate the unit-under-test.

## Evita mezclar la creaci&oacute;n de objetos con la l&oacute;gica de aplicaci&oacute;n

[Fuente](http://misko.hevery.com/2008/09/30/2008/07/08/how-to-think-about-the-new-operator/)

## Evita crear deuda t&eacute;cnica

"Although immature code may work fine and be completely acceptable to the customer, excess quantities will make a program unmasterable, leading to extreme specialization of programmers and finally an inflexible product. ... A little debt speeds development so long as it is paid back promptly with a rewrite ... *Every minute spent on not-quite-right code counts as interest on that [debt](http://en.wikipedia.org/wiki/Technical_debt
).* Entire engineering organizations can be brought to a stand-still under the debt load of an unconsolidated implementation ...”
(Emphasis mine)

[Fuente](http://c2.com/doc/oopsla92.html)

## La optmizaci&oacute;n prematura es la ra&iacute;z de todos los males

"Programmers waste enormous amounts of time thinking about, or worrying about, the speed of noncritical parts of their programs, and these attempts at efficiency actually have a strong negative impact when debugging and maintenance are considered. We should forget about small efficiencies, say about 97% of the time: premature optimization is the root of all evil. Yet we should not pass up our opportunities in that critical 3%."

[Fuente](http://c2.com/cgi/wiki?PrematureOptimization)

## Plan, Plan, Plan.

It is much cheaper to do it correctly the first time than to redo it later on.
The sooner a problem is identified and fixed, the cheaper it is to do so.

"The general who wins a battle makes many calculations in his temple before the battle is fought. The general who loses a battle makes but few calculations beforehand. Thus do many calculations lead to victory,
and few calculations to defeat: how much more no calculation at all! It is by attention to this point that I can foresee who is likely to win or lose."

#### "Plans are worthless, planning is invaluable."- Sir Winston Churchill

For this to work, everyone involved has to listen, everyone has to be open, everyone has to be responsive. Or we could keep flailing away with the fucked up attitude that “it has to be this way” because the sacred project plan says it’s this way. Because that really is a lot of fun, isn’t it?

## Programa tambi&eacute;n envuelve ense&nacute;ar a tu equipo

... un equipo de programadores mediocres, sin experiencia que trabajan juntos y escriben para el beneficio del equipo tiene la capacidad de convertirse en un gran equipo, y pueden tomar este enfoque para crear otros grandes equipos. *Todo se resume en si el eqiupo ve su trabajo como s&oacute;lo escribir c&oacute;digo, o escribir con el objetivo de tanto codificar como aprender*"
(Cursivas m&iacute;as)

– Reginald Braithwaite

[Fuente](http://www.theserverside.com/tt/articles/article.tss?l=ProgrammingisAlsoTeachingYourTeam)

### "The most important element of successful software development is learning."

When the entire team meets a certain standard for competence, there is a very large learning surface exposed and the team is able to absorb more information.

[Fuente](http://weblog.raganwald.com/2007/06/which-theory-first-evidence.html)

## "...there are lies, damned lies, and software development estimates."

Software can only partially be designed in advance. ... requirements suffer from observation, that the act of building software causes the requirements to change. ...technical factors cannot be perfectly understood, that only the act of trying to build something with specific components will reveal all of the gotchas and who-knews associated with a chosen technology strategy. ...software design is an iterative process, starting with a best guess that is continually refined with experience.
the normal case for software projects is that tasks are rarely completed exactly as estimated, but that as a project progresses, the aggregate variance from estimates falls.

[Fuente](http://weblog.raganwald.com/2007/06/which-theory-first-evidence.html)

Nobody likes to look stupid. If you’re a professional and someone puts you on the spot to answer “how long will this take?” it’s only human to want to provide an answer. Whether you call it professional pride or ego, it’s a powerful driver.
Good IT workers really don’t like saying “I don’t know.” If they say it, they probably mean it. So stop pushing for a definitive answer when one doesn’t exist.It’s perfectly reasonable to want some sort of plan up front. I’m actually one of those funny types who believe up front planning is a necessity. So long as everyone understands an estimate is just that: an estimate. You learn as you go along and discover more detail. So you revise the estimate accordingly.

[![The mess we're in](https://cloud.githubusercontent.com/assets/43438/4344401/0ddd5fc8-408f-11e4-8887-b0bfbce91dc7.png)](https://www.youtube.com/watch?v=lKXe3HUG2l4)

– Joe Armstrong, autor de Erlang

##Your architecture should resemble your domain

So what does the architecture of your application scream? When you look at the top level directory structure, and the source files in the highest level package; do they scream: health care system, or accounting system, or inventory management system? Or do they scream: rails, or spring/hibernate, or asp?

Architectures should not be supplied by frameworks. Frameworks are tools to be used, not architectures to be conformed to. If your architecture is based on frameworks, then it cannot be based on your use cases.

– Uncle Bob Martin, "Screaming Architecture"

[Fuente](http://blog.8thlight.com/uncle-bob/2011/09/30/Screaming-Architecture.html)

## Sigue los principios de X

* No añadir nueva funcionalidad a menos que un desarrollador no pueda completar una real aplicación sin ella.
* Es tan importante decidir qué no es parte del sistema, como decidir que s&iacute; lo es. No respondas a las necesidades de todo el mundo; en lugar de eso, haz el sistema extensible para que las necesidades adicionales puedan cubrirse de una manera compatible ascendente.
* La única cosa peor que generalizar a partir de un ejemplo, es generalizar a partir de ningún ejemplo.
* Si un problema no es comprendido completamente, probablemente es mejor no proporcionar ninguna solución.
* Si puedes conseguir el 90 por ciento del efecto deseado para el 10 por ciento del trabajo, utiliza la solución más simple.
* Aísla la complejidad tanto como sea posible.
* Proporcionen un mecanismo en vez de una política. En particular, pongan la interfaz de política en las manos de los clientes.

[Fuente](http://en.wikipedia.org/wiki/X_Window_System_protocols_and_architecture#Design_principles)

## Sigue los principios de Unix

"Esta es la filosof&iacute;a de Unix: Escribe programas que hacen una cosa y lo hagan bien. Write programs to work together. Write programs to handle text streams, because that is a universal interface"

- Doug McIlroy, citado en A Quarter Century of Unix [Salus]. Addison-Wesley. 1994. ISBN 0-201-54777-5.

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

[Fuente](http://www.catb.org/esr/writings/taoup/html/ch01s06.html)

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/timoxley/best-practices/trend.png)](https://bitdeli.com/free "Bitdeli Badge")
