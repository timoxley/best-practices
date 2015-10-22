# Mejores Pr&aacute;cticas de la Programaci&oacute;n - Tidbits
### Una colecci&oacute;n de citas y frases obtenidos de la web para programadores

Utilice su propio juicio en su aplicaci&oacute;n.

* * *

## Nunca construyas aplicaciones grandes

El secreto para construir aplicaciones grandes es nunca construir aplicaciones grandes. Divide tus aplicaciones en piezas m&aacute;s peque&ntilde;as. Entonces, ensambla esas piezas del tama&ntilde;o de un mordizco que pueden ponerse a prueba, dentro de tu aplicaci&oacute;n grande.

*Justin Meyer, autor de JavaScriptMVC*.

[Fuente](http://bitovi.com/blog/2010/11/organizing-a-jquery-application.html).

## La calidad importa

Cuando escucho "¡S&Oacute;LO LIBERA DE UNA VEZ EL C&Oacute;DIGO QUE YA FUNCIONA!" pienso en todas las aplicaciones que dej&eacute; de usar porque gradualmente perdieron la habilidad de iterar.

*Avdi Grimm*

[Fuente](https://twitter.com/#!/avdi/status/180747721852985344).

## No escribas c&oacute;digo

No escribas c&oacute;digo (escribe nuevo c&oacute;digo solamente cuando todo lo dem&aacute;s falle) es la lecci&oacute;n m&aacute;s importante que todo desarrollador deber&iacute;a aprender. La cantidad de c&oacute;digo duplicado y basura que existe (en todos los proyectos) es abrumadora. En muchos casos los desarrolladores ni se molestan en echar un vistazo. Lo &uacute;nico que quieren es escribir c&oacute;digo.

[Fuente](http://blogs.agilefaqs.com/2009/10/19/biggest-stinkers)

#### Reducir la cantidad de c&oacute;digo en tu producto deber&iacute;a ser una meta

"Odio el c&oacute;digo, y quiero tan poco c&oacute;digo como sea posible en nuestro producto."

*Jack Diederich*

[Fuente](http://pyvideo.org/video/880/stop-writing-classes)

#### Mant&eacute;n las dependencias al m&iacute;nimo

El viejo dicho "No reinventes la rueda" no aplica cuando la rueda es del motor de una locomotora.

[Fuente](http://www.reddit.com/r/programming/comments/1bcebh/programming_best_practices/c9616mn)

## Deja de escribir clases

La se&ntilde;al de que "esto no deber&iacute;a ser una clase" es cuando la clase tiene dos m&eacute;todos, y uno de ellos es el constructor. Cuando quiera que veas estas se&ntilde;ales, significa que probablemente deber&iacute;as haber escrito s&oacute;lo una funci&oacute;n.

*Jack Diederich*

[Fuente](http://pyvideo.org/video/880/stop-writing-classes)

## Olvida nuevas funcionalidades, simplemente haz lo mismo pero mejor

El problema: es muy f&aacute;cil perder de vista lo que m&aacute;s importa a los usuarios, que es el rendimiento y la usabilidad de las aplicaciones y las funcionalidades que usan m&aacute;s a menudo.

*Tim Anderson*

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

*El Zen de Python*

[Fuente](http://www.python.org/dev/peps/pep-0020/)

## Reescribir > Refactorizar

Si vas a cambiar m&aacute;s del 25% de una clase o m&eacute;todo, considera simplemente reescribirlo. Escribir&aacute;s c&oacute;digo m&aacute;s limpio.

## Refactorizar > Reescribir

#### Excusas comunes para reescribir software

1. El c&oacute;digo apesta
2. "Ahora somos mucho m&aacute;s listos"
3. Escogimos la plataforma y/o lenguaje equivocado

#### Por qu&eacute; (casi) nunca es buena idea reescribir

1. [Tardar&aacute; m&aacute;s de lo que piensas](http://en.wikipedia.org/wiki/Hofstadter's_law)
2. Los mercados cambian
2. Los clientes existentes se frustran
3. Puedes limpiar el c&oacute;digo refactorizando
4. No controlas la reescritura, ella te controla a ti

[Fuente](http://onstartups.com/tabid/3339/bid/2596/Why-You-Should-Almost-Never-Rewrite-Your-Software.aspx)

## Acepta que no tienes idea de c&oacute;mo esto va a crecer

La clave es reconocer desde el principio que no tienes idea de c&oacute;mo esto va a crecer. Cuando aceptes que no lo sabes todo, empezar&aacute;s a dise&ntilde;ar el sistema defensivamente... Deber&iacute;as invertir la mayor parte de tu tiempo en pensando en interfaces en vez de implementaciones.

*Nicholas Zakas, autor de "High-performance JavaScript websites"*

[Fuente](http://radar.oreilly.com/2011/06/big-javascript-apps-teams.html)

[Reconocimiento a Addy Osmani](http://addyosmani.com/largescalejavascript/)

## Evita c&oacute;digo que apesta

[Fuente](http://www.codinghorror.com/blog/2006/05/code-smells.html)  

[Fuente](http://web.archive.org/web/20120130234037/http://stackoverflow.com/questions/114342/what-are-code-smells-what-is-the-best-way-to-correct-them)

## Escribe pruebas unitarias

Todo programador sabe que deber&iacute;a escribir tests para su c&oacute;digo. Pocos lo hacen. La respuesta universal al "¿Por qu&eacute; no?" es "Tengo mucha prisa." R&aacute;pidamente esto se convierte en un c&iacute;rculo vicioso. Cuanta m&aacute;s presi&oacute;n sientas, menos pruebas escribir&aacute;s. Entre menos pruebas escribas, ser&aacute;s menos productivo y tu c&oacute;digo se volver&aacute; menos estable. Entre menos productivo seas, mayor presi&oacute;n sentir&aacute;s. Los programadores se desgastan con esos ciclos. Romperlos requiere de una influencia externa. Encontramos esa influencia externa en un simple framework de pruebas que nos deja hacer peque&ntilde;as pruebas que hacen una gran diferencia.

[Fuente](http://junit.sourceforge.net/doc/testinfected/testing.htm)

#### [Sin las pruebas unitarias] no est&aacute;s refactorizando, s&oacute;lo est&aacute;s cambiando porquer&iacute;a. — Hamlet D'Arcy

## Para escribir pruebas unitarias efectivas, debes escribir c&oacute;digo que se pueda probar

### Falla #1: El constructor hace trabajo real
#### Se&ntilde;ales de alerta

* Existe `new` en un constructor o en la declaraci&oacute;n de un atributo.
* Static method calls in a constructor or at field declaration
* Se hace algo m&aacute;s que solo asignar en los constructores.
* El objeto no esta completamente inicializado cuando el constructor termina (cuidado con los m&eacute;todos 'para inicializar')
* Control de flujo en un constructor (existe un condicional o un bucle)
* Code does complex object graph construction inside a constructor rather than using a factory or builder
* Adding or using an initialization block

### Falla #2: Digging into Collaborators
#### Se&ntilde;ales de alerta

* Objects are passed in but never used directly (only used to get access to other objects)
* Law of Demeter violation: method call chain walks an object graph with more than one dot (.)
* Suspicious names: context, environment, principal, container, or manager

### Falla #3: Brittle Global State & Singletons
#### Se&ntilde;ales de alerta

* Adding or using singletons
* Adding or using static fields or static methods
* Adding or using static initialization blocks
* Adding or using registries
* Adding or using service locators

###Falla #4: La clase hace demasiado
#### Se&ntilde;ales de alerta

* Al resumir lo que hace la clase se incluye el conector "y".
* La clase ser&iacute;a dif&iacute;cil de leer y captar para nuevos miembros del equipo.
* La clase tiene atributos que son utilizados s&oacute;lo en algunos m&eacute;todos.
* La clase tiene m&eacute;todos est&aacute;ticos que s&oacute;lo operan sobre p&aacute;rametros

[Fuente](http://misko.hevery.com/code-reviewers-guide/)

[Fuente](http://misko.hevery.com/presentations/)

## Desarrollo guiado por pruebas con Inversi&oacute;n de Control

Incluso si no est&aacute;s probando tu c&oacute;digo, deber&iacute;as escribir c&oacute;digo que pueda probarse. IoC permite c&oacute;digo "testeable". Inyecta dependencias que faciliten las pruebas o "mocks" al tiempo de probar a fin de aislar la unidad bajo prueba.

## Evita mezclar la creaci&oacute;n de objetos con la l&oacute;gica de aplicaci&oacute;n

[Fuente](http://misko.hevery.com/2008/09/30/2008/07/08/how-to-think-about-the-new-operator/)

## Evita crear deuda t&eacute;cnica

"Aunque el c&oacute;digo inmaduro funcione bien y sea totalmente aceptable al cliente, cantidades excesivas del mismo har&aacute;n que un programa sea indomable, conduciendo a programadores extremadamente especializados y, finalmente, a un producto inflexible. [...] Un poco de deuda acelera el desarrollo siempre y cuando se pague prontamente con una reescritura. [...] *Cada minuto que se gasta en c&oacute;digo no muy bien escrito cuenta como inter&eacute;s en esa [deuda](http://en.wikipedia.org/wiki/Technical_debt)*. Organizaciones enteras de ingenier&iacute;a pueden detenerse bajo la deuda de implementaci&oacute;n sin consolidar"
(Cursivas m&iacute;as)

[Fuente](http://c2.com/doc/oopsla92.html)

## La optimizaci&oacute;n prematura es la ra&iacute;z de todos los males

"Los programadores desperdician mucha cantidad de tiempo pensando o preocup&aacute;ndose sobre el rendimiento de partes del programa que no son cr&iacute;ticas y estos intentos realmente tienen un poderoso impacto negativo cuando consideramos el mantenimiento y la depuraci&oacute;n. Deber&iacute;amos olvidarnos de las pequenas optimizaciones, digamos el 97% del tiempo: la optimizaci&oacute;n prematura es la ra&iacute;z de todos los males"

[Fuente](http://c2.com/cgi/wiki?PrematureOptimization)

## Planifica, Planifica, Planifica

Es mucho m&aacute;s barato hacerlo correctamente la primera vez que rehacerlo posteriormente. Mientras m&aacute;s pronto se identifica y soluciona un problema, es m&aacute;s barato hacerlo.

"El general que gana una batalla hace muchos c&aacute;lculos en su templo antes del fragor la batalla.   El general que pierde una batalla hace pocos c&aacute;lculos con antelaci&oacute;n. Hacer muchos c&aacute;lculos lleva a la victoria y pocos c&aacute;lculos a la derrota: ¡cu&aacute;nto m&aacute;s ning&uacute;n c&aacute;lculo en absoluto! Por dar atenci&oacute;n a este punto yo puedo preveer quien es probable que gane o pierda"

#### "Los planes son in&uacute;tiles, pero la planificaci&oacute;n lo es todo" - Sir Winston Churchill

For this to work, everyone involved has to listen, everyone has to be open, everyone has to be responsive. Or we could keep flailing away with the fucked up attitude that “it has to be this way” because the sacred project plan says it’s this way. Because that really is a lot of fun, isn’t it?

## Programar tambi&eacute;n envuelve ense&ntilde;ar a tu equipo

... un equipo de programadores mediocres, sin experiencia que trabajan juntos y escriben para el beneficio del equipo tiene la capacidad de convertirse en un gran equipo, y pueden tomar este enfoque para crear otros grandes equipos. *Todo se resume en si el eqiupo ve su trabajo como s&oacute;lo escribir c&oacute;digo, o escribir con el objetivo de tanto codificar como aprender*"
(Cursivas m&iacute;as)

*Reginald Braithwaite*

[Fuente](http://www.theserverside.com/tt/articles/article.tss?l=ProgrammingisAlsoTeachingYourTeam)

### "El elemento m&aacute;s importante del desarrollo de software con &eacute;xito es aprender"

Cuando todo el equipo alcanza un cierto nivel de competencia, existe una superficie expuesta de aprendizaje muy grande y el equipo es capaz de absorber m&aacute;s informaci&oacute;n.

[Fuente](http://weblog.raganwald.com/2007/06/which-theory-first-evidence.html)

## "...hay mentiras, mentiras descaradas, y estimaciones de desarrollo de software"

Software can only partially be designed in advance. ... requirements suffer from observation, that the act of building software causes the requirements to change. ...technical factors cannot be perfectly understood, that only the act of trying to build something with specific components will reveal all of the gotchas and who-knews associated with a chosen technology strategy. ...software design is an iterative process, starting with a best guess that is continually refined with experience.
the normal case for software projects is that tasks are rarely completed exactly as estimated, but that as a project progresses, the aggregate variance from estimates falls.

[Fuente](http://weblog.raganwald.com/2007/06/which-theory-first-evidence.html)

Nobody likes to look stupid. If you’re a professional and someone puts you on the spot to answer “how long will this take?” it’s only human to want to provide an answer. Whether you call it professional pride or ego, it’s a powerful driver.
Good IT workers really don’t like saying “I don’t know.” If they say it, they probably mean it. So stop pushing for a definitive answer when one doesn’t exist.It’s perfectly reasonable to want some sort of plan up front. I’m actually one of those funny types who believe up front planning is a necessity. So long as everyone understands an estimate is just that: an estimate. You learn as you go along and discover more detail. So you revise the estimate accordingly.

[![The mess we're in](https://cloud.githubusercontent.com/assets/43438/4344401/0ddd5fc8-408f-11e4-8887-b0bfbce91dc7.png)](https://www.youtube.com/watch?v=lKXe3HUG2l4)

*Joe Armstrong, autor de Erlang*

##Your architecture should resemble your domain

So what does the architecture of your application scream? When you look at the top level directory structure, and the source files in the highest level package; do they scream: health care system, or accounting system, or inventory management system? Or do they scream: rails, or spring/hibernate, or asp?

La arquitectura no deber&iacute;a ser dada por el framework. Los frameworks son herramientas para utilizarlas, no arquitecturas a las que haya que conformarse. Si tu arquitectua est&aacute; basada en frameworks, entonces no puede estar basado en tus casos de uso.

*Uncle Bob Martin, "Screaming Architecture"*

[Fuente](http://blog.8thlight.com/uncle-bob/2011/09/30/Screaming-Architecture.html)

## Sigue los principios de X

* No a&ntilde;adir nueva funcionalidad a menos que un desarrollador no pueda completar una aplicaci&oacute;n real sin ella.
* Es tan importante decidir qué no es parte del sistema, como decidir que s&iacute; lo es. No respondas a las necesidades de todo el mundo; en lugar de eso, haz el sistema extensible para que las necesidades adicionales puedan cubrirse de una manera compatible ascendente.
* La &uacute;nica cosa peor que generalizar a partir de un ejemplo, es generalizar a partir de ning&uacute;n ejemplo.
* Si un problema no es comprendido completamente, probablemente es mejor no proporcionar ninguna soluci&oacute;n.
* Si puedes conseguir el 90 por ciento del efecto deseado para el 10 por ciento del trabajo, utiliza la soluci&oacute;n m&aacute;s simple.
* A&iacute;sla la complejidad tanto como sea posible.
* Proporcionen un mecanismo en vez de una pol&iacute;tica. En particular, pongan la interfaz de pol&iacute;tica en las manos de los clientes.

[Fuente](http://en.wikipedia.org/wiki/X_Window_System_protocols_and_architecture#Design_principles)

## Sigue los principios de Unix

"Esta es la filosof&iacute;a de Unix: escribe programas que hagan una sola cosa y la hagan bien. Escribe programas para trabajar colectivamente. Escribe programas para manejar flujos de texto, porque esta es una interfaz universal."

*Doug McIlroy, citado en "A Quarter Century of Unix" [Salus]. Addison-Wesley. 1994. ISBN 0-201-54777-5.*

* Regla de Modularidad: Escribe partes simples conectadas por interfaces limpias.
* Regla de Claridad: La claridad es mejor que la habilidad y el ingenio.
* Regla de Composici&oacute;n: Diseña programas para ser conectados a otros programas.
* Regla de Separaci&oacute;n: Separa la pol&iacute;tica del mecanismo; separa las interfaces de los motores.
* Regla de Simplicidad: Diseña pensando en la simplicidad; agrega complejidad solamente donde debas.
* Regla de Parsimon&iacute;a: Escribe un programa grande solamente cuando es claro por demostraci&oacute;n que ninguna otra cosa funcionar&aacute;.
* Regla de Transparencia: Diseña pensando en la visibilidad para hacer la inspecci&oacute;n y la depuraci&oacute;n m&aacute;s f&aacute;cil.
* Regla de Robustez: La robustez es la hija de la transparencia y la simplicidad.
* Regla de Representaci&oacute;n: Pliega el conocimiento dentro de los datos de tal manera que la l&oacute;gica del programa pueda ser estúpida y robusta.
* Regla de la M&iacute;nima Sorpresa: En el diseño de interfaces, siempre has la cosa menos sorprendente.
* Regla del Silencio: Cuando un programa no tiene nada sorprendente que decir, no deber&iacute;a decir nada.
* Regla de Reparaci&oacute;n: Cuando debas fallar, falla ruidosamente y tan pronto como sea posible.
* Regla de Econom&iacute;a: El tiempo del programador es costoso; consérvalo en preferencia al tiempo de m&aacute;quina.
* Regla de Generaci&oacute;n: Evita el hackeo manual; escribe programas para escribir programas cuando puedas.
* Regla de Optimizaci&oacute;n: Haz prototipos antes de pulir. Haz que funcione antes que lo optimices.
* Regla de Diversidad: Desconf&iacute;a de todas las pretensiones para "una v&iacute;a verdadera".
* Regla de Extensibilidad: Diseña para el futuro, porque estar&aacute; aqu&iacute; m&aacute;s pronto de lo que piensas.

*Eric S. Raymond, "The Art of Unix Programming"*

[Fuente](http://www.catb.org/esr/writings/taoup/html/ch01s06.html)

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/timoxley/best-practices/trend.png)](https://bitdeli.com/free "Bitdeli Badge")
