# Mejores prácticas de la Programación - Tidbits
### Una colección de citas y frases obtenidos de la *web* para programadores.

* * *

## Nunca construir aplicaciones grandes

El secreto para construir aplicaciones grandes es nunca construir aplicaciones grandes. Rompe tus aplicaciones en piezas más pequeñas. Entonces, ensambla esas piezas del tamaño de un mordizco que pueden ponerse a prueba, dentro de tu aplicación grande.

Fuente: Justin Meyer, autor de *JavaScriptMVC* http://bitovi.com/blog/2010/11/organizing-a-jquery-application.html

## Acepta que no tienes idea de cómo esto va a crecer

La clave es reconocer desde el principio que no tienes idea de cómo esto va a crecer. Cuando aceptes que no lo sabes todo, empezarás a diseñar el sistema defensivamente... Deberías invertir la mayor parte de tu tiempo en pensar acerca de interfaces en vez de implementaciones.

Fuente: Nicholas Zakas, autor 'High-performance JavaScript websites' http://radar.oreilly.com/2011/06/big-javascript-apps-teams.html

Reconocimiento:
http://addyosmani.com/largescalejavascript/

## Sigue el principio de X

En 1984, Bob Scheifler y Jim Gettys establecieron los tempranos principios de X:

   * No añadir nueva funcionalidad a menos que un desarrollador no pueda completar una real aplicación sin ella.
   * Es tan importante decidir qué no es parte del sistema, como decidir que si lo es. No respondas a las necesidades de todo el mundo; en lugar de eso, haz el sistema extensible para que las necesidades adicionales puedan cubrirse de una manera compatible ascendente.
   * La única cosa peor que generalizar a partir de un ejemplo, es generalizar a partir de ningún ejemplo.
   * Si un problema no es comprendido completamente, probablemente es mejor no proporcionar ninguna solución.
   * Si puedes conseguir el 90 por ciento del efecto deseado para el 10 por ciento del trabajo, utiliza la solución más simple.
   * Aísla la complejidad tanto cuanto sea posible.
   * roporcionen un mecanismo en vez de una política. En particular, pongan la interfaz de política en las manos de los clientes.
   
El primer principio fue modificado durante el diseño del X11: "No añadan nueva funcionalidad a menos que ustedes sepan de alguna aplicación real que la requiera".

Fuente: http://en.wikipedia.org/wiki/X_Window_System_protocols_and_architecture#Design_principles

## La calidad importa

Cuando escucho "SÓLO LIBERA DE UNA VEZ EL CÓDIGO QUE YA FUNCIONA!" pienso en todas las aplicaciones que dejé de usar porque gradualmente perdieron la habilidad de iterar.

Fuente: https://twitter.com/#!/avdi/status/180747721852985344

## No hagas cosas difíciles, has cosas sencillas.

* Simple es mejor que complejo.
* Complejo es mejor que complicado.
* Plano es mejor que anidado.
* La legibilidad cuenta.
* Si la implementación es difícil de explicar, es una mala idea.
* Si la implementación es fácil de explicar, puede que sea una buena idea.

Fuente: El Zen de Python: http://www.python.org/dev/peps/pep-0020/
(Lista + título de Jack Diederich of http://pyvideo.org/video/880/stop-writing-classes)

## No escribas código

No escribas código (escribe nuevo código solamente cuando todo lo demás falle) es la lección más importante que todo desarrollado debería aprender. La cantidad de código duplicado y basura que existe (en todos los proyectos) es abrumadora. En muchos casos los desarrolladores ni se molestan en echar un vistazo. Lo único que quieren es escribir código.

Fuente: http://blogs.agilefaqs.com/2009/10/19/biggest-stinkers/

#### Reducir la cantidad de código en tu producto debería ser una meta.

"Odio el código, y quiero tan poco código como sea posible en nuestro producto." - Jack Diederich

## Deja de escribir clases

La señal de que "esto no debería ser una clase" es cuando la clase tiene 2 métodos, y uno de ellos es el constructor. Cada vez que veas estas señales, probablemente deberías sólo escribir una función.

Fuente: Jack Diederich, Stop Writing Classes http://pyvideo.org/video/880/stop-writing-classes

## Refactorizar > Reescribir

#### Excusas comunes para reescribir software
1. El código apesta
2. "Somos mucho más inteligentes ahora"
3. Escogimos la plataforma/lenguaje equivocado

#### Por qué reescribir (casi) nunca es una buena idea 

1. Tardará más de lo que piensas
2. Los mercados cambian
2. Los clientes existentes se frustran
3. Refactorizar puede limpiar el código
4. No controlas la reescritura, ella te controla a ti

http://onstartups.com/tabid/3339/bid/2596/Why-You-Should-Almost-Never-Rewrite-Your-Software.aspx

## Reescribir > Parchar
Si vas a cambiar más del 25% de una clase o método, considera simplemente reescribirlo. Escribirás código más limpio.

## Refinando funcionalidades existentes existing features > Agregando nuevas funcionalidades.

El problema: es muy fácil perder de vista lo que más importa a los usuarios, que es el rendimiento y la usabilidad de las aplicaciones y las funcionalidades que usan más a menudo.

Fuente: Tim Anderson "Making better software: forget new features, just do the same stuff better" http://www.itjoblog.co.uk/2011/06/making-better-software.html

## Escribe tests unitarios.
Todo programador sabe que debería escribir tests para su código. Pocos lo hacen. La respuesta universal al "¿Por qué no?" es "Tengo mucha prisa." Rápidamente esto se convierte en un círculo vicioso. Cuanta más presión sientas, menos pruebas escribirás. Entre menos pruebas escribas, serás menos productivo y tu código se volverá menos estable. Entre menos productivo seas, mayor presión sentirás. Los programadores se desgastan con esos ciclos. Romperlos requiere de una influencia externa. Encontramos esa influencia externa en un simple framework de pruebas que nos deja hacer pequeñas pruebas que hacen una gran diferencia.

Fuente: http://junit.sourceforge.net/doc/testinfected/testing.htm

#### [Sin los tests unitarios] No estás refactorizando, sólo estás cambiando mierda. — Hamlet D'Arcy

## To write effective unit tests, you need to write testable code

### Flaw #1: Constructor does Real Work
####Warning Signs
* new keyword in a constructor or at field declaration
* Static method calls in a constructor or at field declaration
* Anything more than field assignment in constructors
* Object not fully initialized after the constructor finishes (watch out forinitialize methods)
* Control flow (conditional or looping logic) in a constructor
* Code does complex object graph construction inside a constructor rather than using a factory or builder
* Adding or using an initialization block 

### Flaw #2: Digging into Collaborators
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


##Your architecture should resemble your domain

So what does the architecture of your application scream? When you look at the top level directory structure, and the source files in the highest level package; do they scream: health care system, or accounting system, or inventory management system? Or do they scream: rails, or spring/hibernate, or asp?

Architectures should not be supplied by frameworks. Frameworks are tools to be used, not architectures to be conformed to. If your architecture is based on frameworks, then it cannot be based on your use cases.

Source: Uncle Bob Martin "Screaming Architecture" http://blog.8thlight.com/uncle-bob/2011/09/30/Screaming-Architecture.html

##Unix Philosophy

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

Source: Eric S. Raymond "The Art of Unix Programming" http://www.catb.org/esr/writings/taoup/html/ch01s06.html