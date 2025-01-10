---
created: 2024-12-12T09:58:45
modified: '"2025-01-02 10:59", "4tc/G1T+6"'
date: 2024-12-12
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "11236"
---
## Fecha de Reunion
2024-12-12

## Asistentes

### Davivienda
* David Alejandro Romero - Arquitecto de DAV supongo
* Sandra Ojeda 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
* Levantamiento de infraestructura
* Lineamientos de DevOps
* Accesos
* Comunicaciones
* 

## Puntos de Acción acordados
- Organización de recursos en cuentas y distribución de costos: 
	- Sandra dice no usar cuentas Shared
	- El objetivo es desplegar sus propias cuentas (3 para PER por ambiente (DEV,LAB,PROD), y 3 para Camara Compensación (una por ambiente) - Total 6 cuentas
	- Las cuentas compartidas son por países
	- Los porcentajes ya están establecidos, tanto para la ejecucion, como para los consumos
		- Esta Tareas debería ser de Nicolas. dice que ya se hizo
		- Colombia es la que va pagar mas.
		- Involucrar a FinOps?
		- Estrategia de Tagging??
			- Todos los componentes son una sola solución...no se puede taggear por tasks.
	- El consumo lo debe gestionar la aplicacion 🚩
		- A futuro!! en este momento la estrategia debe ser fija
	- Conclusion: cuentas nuevas, por ambiente (6 en total)
- Aspectos de Infraestructura y Seguridad
	- [ ] Darwin Gabriel Arellano pide sesiones para revisar la infraestructura. Diferencias entre laboratorio y producción. #followup #id11236
		- Hay componentes que no son iguales entre ambientes (F5, etc..)
	- [ ] Infraestructura de seguridad perimetral #followup #id11236  ⚠ 🔺 🚩 🚩
		- Esto es administrado por Cyberseguridad Colombia
	- [ ] Lineamientos de seguridad #followup
### Principales actividades
1.  Definir mapa de dependencias (conexiones)
	1. David Alejandro Romero dice que ya existe un mapeo de dependencias generales 
	2. Se puede hacer diagramas más específicos según sea requerido
	3. Son dos diagramas/sesiones: Uno de interrelación de funcionalidades y flujos y otro de conectividad
	4. Se deberia empezar a trabajar con el de Single-Sign On
		1. Tenemos una dependencia con el proveedor Technyisis

2. Herramienta de DevOps
	- Accesos: Jhonan y Francisoco aún no tienen acceso al Tenant
	- Modulos
	- Pipelines
	- Se solicita que se tenga alguna persona asignada de DevOps y Seguridad al proyecto
3. Refinamiento de Backlog
	- [ ] Definición de Historias de Usuario con el analista funcional (Rerfinamiento de Backlog) #followup
4. Herramientas de Gestión de proyectos
	- [x] MC pide acceso a JIRA - en cual Jira #followup ✅ 2025-01-02
		- MC tambien pide los prototipos
		- Con eso pueden empezar a volcar los HU

### Siguientes Pasos
1. Mapa de Dependencias

## Proxima Reunión
*   

----
## Resumen de Read.Ai


Resumen:

Se abordaron varios aspectos clave relacionados con la infraestructura y la gestión de costos del proyecto. Jenny propuso definir lineamientos iniciales de DevOps, mientras que Sandra expresó preocupaciones sobre la distribución de costos en cuentas compartidas, lo que podría complicar la facturación en diferentes países. David aseguró que se crearían cuentas específicas para el proyecto y que los porcentajes de cobro ya estaban establecidos, además de la necesidad de coordinar con el área financiera para una adecuada distribución de costos. Se acordó la creación de seis cuentas para el ecosistema, abarcando ambientes de desarrollo, laboratorio y producción, y se discutieron inquietudes sobre la arquitectura y la gestión de logs, sugiriendo sesiones adicionales para abordar estos temas.

La reunión también se centró en la implementación de la aplicación, destacando la importancia de un mapeo de dependencias y la gestión de accesos en GitHub. Se acordó que la seguridad se trataría en una sesión separada y se mencionó la necesidad de crear diagramas detallados para las funcionalidades del proyecto, comenzando con el single sign-on. Carlos y Nicolás propusieron establecer reuniones regulares para coordinar el avance del proyecto, sugiriendo un formato semanal o bisemanal, y Nicolás se encargará de crear un canal en Google Chat para facilitar la comunicación. Se destacó la importancia de tener acceso a un sistema de gestión de proyectos como Jira y se acordó realizar sesiones de refinamiento para asegurar la comprensión de las historias de usuario y funcionalidades requeridas.


Capítulos y Temas:

**Título de la sección de reunión:** Definición de lineamientos para la infraestructura del ambiente de desarrollo
**Resumen conciso en 2-4 oraciones:** Jenny propuso definir los lineamientos para habilitar la infraestructura del ambiente de desarrollo, sugiriendo comenzar con los lineamientos de DevOps. Sandra planteó preocupaciones sobre la distribución de costos en cuentas compartidas, solicitando claridad sobre cómo se manejarían los cobros entre los países. David confirmó que se establecerían cuentas específicas para el proyecto y que los porcentajes de facturación ya estaban definidos.
* Definición de lineamientos para habilitar la infraestructura del ambiente de desarrollo.
* Creación de cuentas para el Portal Empresarial Regional y la cámara de compensación.

Alineación sobre la creación de cuentas y arquitectura de infraestructura
Se acordó habilitar seis cuentas para el ecosistema de cuentas, que abarcarán ambientes de desarrollo, laboratorio y producción, compartidos entre los países involucrados. Erwin expresó su preocupación sobre la arquitectura y la posibilidad de que las infraestructuras de laboratorio y producción no sean equivalentes, sugiriendo la necesidad de sesiones adicionales para abordar estos temas. Franklin destacó la importancia de involucrar al equipo de seguridad en el proyecto para asegurar la homogeneidad en la infraestructura.
* Importancia de la seguridad perimetral y la homogeneidad en los ambientes de desarrollo, laboratorio y producción.

Implementación de la Aplicación y Gestión de Dependencias
Se abordó la necesidad de establecer un mapeo de dependencias y gestionar accesos al entorno de DevOps para comenzar la implementación de la aplicación. David enfatizó que es crucial tener un apoyo de DevOps y seguridad para resolver problemas y facilitar el despliegue. Además, se mencionó que la seguridad debe ser tratada en una sesión aparte debido a su complejidad.

Discusión sobre Integración de Servicios y Autenticación
Se propuso desarrollar diagramas específicos para cada funcionalidad del proyecto, comenzando con el single sign-on, para mejorar la comprensión de las integraciones necesarias. Martín y otros oradores coincidieron en que es crucial entender cómo se manejará la autenticación de clientes y el flujo de información entre aplicaciones. Se acordó organizar reuniones para discutir estos temas en detalle.
* Necesidad de sesiones de trabajo para definir diagramas de dependencias y flujos de información.

Planificación de Reuniones y Gestión de Proyectos
Carlos y Nicolás proponen realizar reuniones semanales o bisemanales para mantener la comunicación y el seguimiento del proyecto. Se acordó que Nicolás será responsable de crear un canal en Teams para invitar a los miembros del equipo y al cliente. Además, se abordó la necesidad de gestionar accesos a GitHub y la creación de repositorios.


Puntos de Acción:

* David revisará y confirmará la distribución de costos con el área financiera.
* Jenny definirá en dónde se crearán las cuentas para el Portal Empresarial Regional y la cámara de compensación.
* Martín iniciará el mapeo de dependencias y definirá los lineamientos de seguridad.
* Nicolás creará un canal de comunicación en Slack para el equipo de desarrollo y la vivienda.
* Sergio gestionará el acceso a los repositorios de GitHub y Jira para el equipo de desarrollo.


Preguntas clave:

* ¿Qué criterios se utilizarán para etiquetar los servicios y costos por país en la aplicación?
* ¿Qué medidas de seguridad se implementarán para asegurar la homogeneidad entre los ambientes de desarrollo y producción?
* ¿Cómo se gestionará el acceso a los repositorios de GitHub y Jira para el equipo de desarrollo?
* ¿Cuándo se llevarán a cabo las sesiones para definir el diagrama de dependencias?


Bloc de notas:

* No hay notas
## Transcripción de la Reunion 

11236-CO-Davivienda-Portal Empresarial Regional-Sync Inicial - 2024_12_12 11_43 GMT-04_00 - Recording.mp4 
Thu, Dec 12, 2024

0:00 - Jenny Rodriguez 
Bueno, más que de mi parte, entiendo que el objetivo de la sesión, según lo que hablamos al finalizar el kick-off de esta semana, con David es importante entonces empezar a definir los lineamientos para empezar a habilitar entonces la infraestructura para iniciar lo que viene a ser ambiente de desarrollo. Entonces, la vez pasada David mencionaba como ¿Por qué podemos iniciar? A menos de que Johan me diga lo contrario, pero yo les decía a ellos que, pues, inicialmente, un primer lineamiento que podemos empezar a trabajar son los lineamientos de DevOps, en este caso, con los servicios que vamos a empezar a habilitar para pedir uno, dos accesos y tres, empezar tal vez a definir también lineamientos y sesión de discovery para todo lo que viene a ser tema de conectividad. Y ya entendería que una vez dejemos esto definido, el objetivo ya como tal sería trabajar muy de la mano con Martín para empezar entonces a habilitar los servicios en el ambiente de desarrollo que ustedes requieran ya como tal para la implementación de la aplicación. Eso era lo que habíamos mapeado. No sé, allí, David, si se me, creo que era Diego, si se me pasa algo de las cosas que tengo acá en nota fue lo que lo que anotamos para esta primera sesión.

1:26 - David Santiago Bohorquez Rodriguez 
¿No hay alineados, Jenny? Ahí estamos desde acá, pues, desde el equipo de Nico Conectado. Si bien era Nicolás, somos los otros tres acá. Ah, bien, perfecto. Y de pronto aprovechar el espacio y presentar al equipo de infraestructura, aunque creo que tú ya los conoces, pero de pronto aquí, Fernando y Edwin, comentarles que ya arrancó el proyecto Portal Empresarial Regional. Ya estamos acá con el Aleo Estrategico, que es escala 24-7. Y de acuerdo a eso, pues, nos toca, como dice Jenny, hacer todo el tema de levantamiento de la infraestructura y todo el tema de conexión e integraciones entre barco de vivienda y AWS para este proyecto. No sé si tengan de pronto alguna duda o si podríamos, entonces, ir arrancando, como dice Jenny, con esos hitos.

2:13 - Sandra Ojeda 
Sí, yo tengo una pregunta ahí, Jenny. Buenos días a todos. Gracias, Daniel. Hablando más de cómo va a ser la implementación, en una cuenta compartida y cómo se van a distribuir los costos a cada país, o va a ser temas definidos para cada país. Ese tema de las cuentas shared a veces nos generan unos pequeños inconvenientes en la distribución de los costos para cada país. No sé si ya se lo definió proyectos o ahí veo a David en arquitectura. Creo que a veces olvidamos unos detalles que tienen que ver con ese tipo de cosas. Entonces, no quisiera que me empezara a parecer estructura en unas cuentas Cher, que después cada país, especialmente El Salvador, como sabes Jenny, pregunta que qué le estás cobrando. Entonces no sé si esas definiciones las hicieron, las dejaron claramente identificadas, supongo que es una responsabilidad del proyecto y de la arquitectura, pero pues es importante porque después, desafortunadamente, las preguntas nos llegan a nosotros.

3:11 - Jenny Rodriguez 
No, totalmente alineada con su merced, señora Sandra, de hecho el objetivo también de estas es empezarlo a afinar, ahí para que ustedes tengan visibilidad. Inicialmente, pues, cuando hicimos la estimación del proyecto, el objetivo es que para el despliegue de estas cargas, o sea, todo lo que está relacionado con PERI, con cámara de compensación, el objetivo es habilitar su ecosistema de cuentas. Nosotros, para cada una de las iniciativas, señora Sandra, Se planteó el desplegar las cuentas para la carga de PER y, posterior, las cuatro cuentas para lo que viene, bueno, me tiran las tres cuentas para PER, que vendría a ser ambiente de desarrollo, ambiente de laboratorio y su ambiente productivo. Y tendríamos tres cuentas también para lo que vendría a ser cámara de compensación. En este orden de ideas, estas cuentas serían, pues, efectivamente de uso a nivel regional. Va a ser una sola solución. A los cuatro países. Y entendería que, pues, bueno, ya con respecto a los alineamientos del banco para el esquema de facturación, no sé aquí, digamos, la directriz, ahí sí tocaría revisarlo con David, si esto a nivel de Corus usted lo van a cobrar por consumo esquema transaccional o tienen definido otro. Pero, pues, digamos, si inicialmente para darle respuesta en este momento serían tres cuentas nuevas, unas para PER y tres cuentas para Cama de compensación en donde desplegaríamos el ecosistema de servicios para cada ambiente. ¿Listo?

4:45 - Sandra Ojeda 
Y- Sí, ahí es súper importante, David, tener en cuenta, vas a levantar la mano, supongo que ya me vas a contestar que ya hablaste con el área financiera, que ya sabes cómo es este rollo, en donde ellos son los que definen si es que eso se va a distribuir proporcionalmente en los países. Ellos definen cuál serían esos porcentajes que hay que cobrarle a cada Y supongo que eso debería ser como para mañana, porque si van a habilitar las cuentas mañana, ya deberíamos tener para la siguiente factura. Jenny, eso tan pronto empieza a subir máquinas, empieza a facturar.

5:22 - David Alejandro Romero Romero 
Entonces, hay que saber quién va a pagar. Gracias. Sandra, como dijo Jenny, las cuentas son compartidas por todos los países y ya hay unos porcentajes establecidos. Los porcentajes inicialmente estaban establecidos para la ejecución del proyecto, pero entendía que también era para el pago de la mensualidad de la infraestructura, pero podríamos confirmarlo con. Pues más con negocios y si están de acuerdo con el cobro de la infraestructura, sea igual que el cobro de el proyecto.

5:49 - Sandra Ojeda 
Eso seguramente lo tiene que definir financiera, no? Ahí, ahí, o sea, ahí normalmente hay una validación que hay que hacer con Juan Jara y Juan Jara es el que ha definido la mayoría de los porcentajes que yo conozca, entonces no sé si esa tarea ya que le dan toda la mano.

6:07 - David Santiago Bohorquez Rodriguez 
Sí, esa esa tarea se hizo al inicio del proyecto de San Marita para todo el tema de de gestión presupuestal y el contrato. Los porcentajes ya están definidos por cada una de las de las filiales y de la casa matriz. Colombia me parece que es la que va a pagar más más el el proyecto como tal y dentro de la estimación de escala de estado por infraestructura proyectado a a tres años, si no estoy mal.

6:31 - Nicolas Leon Perez 
Sí, pero ahí hay de pronto para aclarar un del presupuesto por infraestructura a escala? Ese lo tenemos, pero Sandrita, de infraestructura CAMP, ¿va a haber algún costo adicional?

6:41 - Sandra Ojeda 
No, lo que pasa es que eso todo llega a las mismas cuentas y se factura, supongo, dentro de los mismos valores de AWS. Más allá de CAMP, cada país tiene que pagar su factura. Entonces, eso es a lo que estamos hablando. Cuando hablamos de CAMP, hablamos de los países.

6:59 - Nicolas Leon Perez 
Sí, sí, sí. Perdón, Darwin, eso, ¿eso qué corresponde a lo que nos estimamos? De cobro por impasura y el mantenimiento recurrente a tres años, eso ya está seccionado, ya se le notificó a los países cuál es el cobro que va a tener por por ese rubro en particular, y se tiene distribuido de acuerdo a lo que nos dijo Planación Financiera, de los porcentajes de acuerdo a a cómo va a quedar la participación de cada uno de los países dentro del PER. Entonces, para que cuando hagan la distribución de las facturas llegue así eh sí yo yo quería que nos compartió la distribución Jenny para que lo pueda revisar fue María Fernández de la Edad Escala para para entender nada más todo

7:50 - Fernando Guerrero 
esto todo esto este entonces ahí estoy entendiendo Jenny entonces se va a abrir una una cuenta nueva la facturación de acuerdo a los porcentajes que están mencionando que ya se. Sí, señor.

8:04 - Jenny Rodriguez 
Ahí para ponerlos un poco en contexto. Entonces, a qué pena, Anfer, que se le estaba entrecortando, yo pensé que ya había terminado. No, ahí les voy a hacer la proyección del diagrama inicial. De todas maneras, yo me llevo el punto y, bueno, yo creo que con Carlitos también, para revisarlo con Mafe, porque yo entiendo que sí, que ya iba a ser la distribución. Pero para que todos 2 sistemas alineados de un FER. Y, pues, dentro del alcance que tenemos es vamos a habilitar el ecosistema de cuentas para lo que vendría a ser de la carga PER. ¿Listo? El portal empresarial. Dentro del alcance tenemos, entonces, crear 3 cuentas en donde vamos a tener ambiente de desarrollo, ambiente laboratorio, que sería donde ustedes van a certificar, y posterior el ambiente productivo. ¿Listo? Estas 3 cuentas que se van a habilitar, van a ser para las cargas transaccionales de los cuatro, bueno, de los, de todos los países. En este caso no, no es que vayamos a habilitar infraestructura por país, sino en este caso va a ser una sola cuenta donde pues todos van a, vamos a desarrollar ahí para los cuatro países, de igual forma para el tema de certificación y el ambiente productivo.

9:21 - Orador no identificado 
Entonces.

9:21 - Fernando Guerrero 
Son nuevas cuentas, esas tres.

9:24 - Orador no identificado 
Exactamente.

9:24 - Sandra Ojeda 
Son como si fueran. Ya tenemos cuentas compartidas. Son nuevas cuentas, ¿OK? Son nuevas cuentas, pero dentro de esas nuevas cuentas son compartidas, o sea, cada una de esas cuentas va a ser compartida. Ahora. Entendido.

9:38 - Jenny Rodriguez 
Ahora ahí. Son seis, ¿Verdad? Sí, serían seis, serían tres para PER, y tendríamos tres para lo que vendría a ser cámara de compensación. Ahora, lo que habría, bueno, no sé, ahí tal vez me remite un poco más me apoyó con Frank. No sé si hoy en día dentro del de la unidad organizativa que tiene la vivienda, tal vez tenga una buen que diga regional y esas clientes y esas cuentas nazcan ahí con sus respectivas cargas.

10:10 - Frank Caicedo 
Bueno, pero el objetivo es está segmentado, entonces estaremos habilitando 6 cuentas. Listo. Perfecto. Darwin quiere participar.

10:18 - Fernando Guerrero 
Tengo una duda. Bueno, disculpen la ignorancia, porque realmente está participando David, pero obviamente ya estoy incorporándome un poco más a nivel más arriba. Pero sí quisiera entender un poco más a detalle la arquitectura que van a implementar. Me imagino que habrá sesiones posteriores para ver al detalle de esta infraestructura. Porque sí quisiera entender cómo se va a hacer un tema de los logs por país o cómo sería esa infraestructura. Porque nos ha pasado con otros proveedores, a veces el ambiente de laboratorio de integración no tiene la misma infraestructura que producción y cuando pasamos a producción nos va mal. Entonces, ¿va a haber sesiones posteriores para ver este detalle con infraestructura?

11:00 - Jenny Rodriguez 
Sí, Erwin, vamos a empezar a tener ya como tal las sesiones en donde por lo menos, no sé, desde los primeros aspectos considero que lo primero que hay que ver es el tema de conectividad, este tema que estaba mencionando la señora Sandra de, bueno, ¿Dónde van a nacer estas cuentas? Y ya, pues, efectivamente, para darte tranquilidad, la idea es que efectivamente el ambiente de desarrollo va a tener, digamos, como siempre los mismos recursos, tal vez más bien no con la misma cantidad que tendríamos en un ambiente productivo, pues, para que efectivamente se habilite. Y ya por lo menos el ambiente laboratorio y producción se puedan parecer más para todo el esquema de Dentro de la definición de las sesiones, vamos a ir definiendo todo el esquema que, pues, en este caso, si te das cuenta, es una solución multiregional en donde, pues, habilitamos un solo portal para todos. Entonces, hay que dejar definido, efectivamente, ya para la construcción ahí con Martín, el tema de las tramas o la gestión de logs, en donde nosotros, pues, los vamos a centralizar y, pues, posterior, ustedes podrían ya como tal entrar a hacer allí la explotación para todo el tema de trazabilidad, monitoreo, rastreo y ese tipo de características, bueno, entonces son cosas que vamos a ir revisando ya como tal dentro del baseline una vez inicie el desarrollo y esas consideraciones que hay que tener en cuenta, ¿ok?

12:25 - Fernando Guerrero 
De acuerdo, nada más que para aclarar y ahí Sandra creo que ofrece estar claro, es que a veces sí la infraestructura de ustedes puede ser igual a la de producción pero las conexiones o los puntos intermedios no son iguales y a veces nos ha pasado que cuando certificamos en laboratorio, pasamos a producción y la infraestructura es diferente. Por ejemplo, pasa por un F5, que no sucede en ambientes previos, temas de muchos componentes de seguridad que están en producción que no están en ambientes previos, que logramos certificar y cuando ya vamos a producción, pues obviamente nos rebota y pues nos da dolores de cabeza para poder solucionarlo. Es la duda que tenía, pero por eso era las sesiones, digamos que entiendo se van a realizar para ver esos temas y poder minimizar esos casos o esos errores que se nos puedan presentar cuando pasamos a producción.

13:18 - Frank Caicedo 
Alineados, Darwin, alineados contigo.

13:20 - Franklin Garcia 
Hola, buenos días, ¿cómo están? Un placer verlos, Sandra. Sí, corresponde a lo de los costos, es importante que una de las sesiones, una de las primeras sesiones que tengamos, sea una sesión etiquetado de esta infraestructura, ¿sí? Para poder nosotros saber cuáles son las intenciones de ustedes a nivel de finanzas y costos, y poder etiquetar los servicios según cada país. La buena noticia es que tenemos SS, y SS es un servicio que te permite incluso etiquetar los TAS y los servicios que van corriendo dentro de él, la diferencia es que es más complejo. Entonces, SS, al permitirnos esa anularidad en tax, podemos saber cuánto está costando en tax y servicios corriendo en contenedores cada país. Si un país crece, pues tendrá la cantidad de etiquetas necesarias para poder monitorear su costo. Donde está medio complicado, va a ser en la base de datos, porque será una para todos.

14:21 - Jenny Rodriguez 
De hecho, los microservicios también es uno para todos, Frank. Yo creo que la estrategia aquí es más con base en lo que defina negocio, el ver si va a ser así porcentual como se trajo la iniciativa inicial, o si efectivamente, por lo menos, no sé si quieren ir mucho más granulares, pensaría que toca empezar a cuantificar por consumo a nivel transaccional. Porque en este caso, la base de datos, los microservicios, todos los componentes van a ser una sola solución para todos los países.

14:53 - Franklin Garcia 
Ah, bueno, entonces ya en ese caso sí toca literalmente el 25%. Exacto.

14:58 - Jenny Rodriguez 
El taggeo nos serviría más para la identificación de los componentes asociados a la carga, pero digamos que a partir de allí ya como tal para lo que viene a ser, no sé, si por ejemplo la minucia va a ser el consumo transaccional de cada país, no nos servirían estas estrategias para tenerlo en cuenta. ¿Listo?

15:18 - Franklin Garcia 
Está bien, está bien. Nada, desconocer la arquitectura del software, ¿no? No, no te preocupes. Mira, lo otro, lo segundo punto que que no lo iba a traer pero lo comentó el señor Darwin con respecto a la infraestructura de seguridad perimetral. Es importante acotar que la seguridad perimetral que hoy existe en CAM no es parte de la infraestructura de de escala ni implementada por escala ¿Sí? Es parte de la de de la regional de Colombia. Todo tiene que pasar por ahí y todo tiene que salir por ahí. Tanto en tráfico como entrada y salida, todo pasa por esa también pasen por allí para poder ser más homogéneos en la infra, así como lo tenemos en CyberBank. Entonces, para hacerle, para calmar un poco esa parte o esa incertidumbre de qué va a pasar o no, pues desarrollo, laboratorio y producción van a tener la misma infra de seguridad perimetral de Colombia. Entonces, esa primera fase de desarrollo va a tardar un poco más, pero ya esperemos que en las otras eso ya esté, se haya, digamos, resuelto y sea más fácil. Sí, pero es importantísimo involucrar al equipo de seguridad, del equipo de debo en este proyecto, para eso, para que esto vaya con los tiempos que que queremos todo. Y eso es todo. Alineados. Gracias, Franklin.

16:38 - Jenny Rodriguez 
Nada, solo para complementar y allí tal vez para que lo revise el equipo de adivina dado a lo que menciona la señora Sanda con respecto al tema de los costos Yo creo que sería bueno que lo debatan y se defina. Porque en dado caso de que ustedes quieran hacer una segmentación por consumo, pensaría yo que viene a ser un atributo que Martín va a tener que contemplar en el desarrollo de la aplicación para que quede de una vez habilitado. Porque lo controlaría es como tal ya la aplicación. Entonces, sería bueno que eso lo revisen y con eso, Mati, lo tengan ahí dentro de los requerimientos cuando se desarrolle el portal. ¿Listo? Y cámara.

17:22 - Carlos Ramírez 
Son entiendo bien y solo para entender, entonces, digamos, esa separación de costos no se puede hacer por medio de tax, por lo que estás explicando, sino que sería la aplicación la que se debería encargar de llevar ese tracking, digamos.

17:40 - Orador no identificado 
Sí.

17:41 - Jenny Rodriguez 
Si el objetivo del banco es cobrar, al país por el consumo que hagan del uso del portal. Ahí, Martín, la única estrategia que yo veo es que la aplicación sea la que lo controle. Con respecto a los componentes, no lo podríamos hacer porque, como tal, esto no es que vayamos a desplegar componentes por país, sino a hacer una solución homogénea para los 4. Entonces, sería algo que toca gestionarlo más a nivel del software. Ahora, si ese no va a ser el alcance del banco y Y, efectivamente, va a ser más bien una distribución porcentual que, independientemente de lo que usen o consuman o transen, van a pagar. Pues, digamos que este no sería como tal ya un impedimento que el software tenga que asumir. Pero es importante que, como lo mencionaba Sandra, que lo definan. Si en el corto, mediano y largo plazo ese va a ser el foco o si lo van a cambiar y luego lo van a pensar en distribución exacto. Por país lo tiene que gestionar el software, ¿OK?

18:42 - Orador no identificado 
Sí.

18:42 - Martín Vasconcelos 
Igual cada, o sea, el software ya va a estar separado por países. Sí o sí, el token de usuario va a tener el país desde el cual ingresó el usuario. O sea, que toda esa información la podemos estar, la vamos a estar guardando por separado futuro. Así que después hay que elegir, si quisieran ir por ese lado, elegir cuál es el criterio que utilizan para dividir, no sé, si es cantidad de login, cantidad de transferencia, cantidad de consultas, eso ya no excede, pero eso se

19:11 - Jenny Rodriguez 
va a poder separar como país seguro.

19:14 - Fernando Guerrero 
Alineados. Gracias Martín. Pero entiendo que en este momento Entiendo que la decisión es que sea fijo, perdón.

19:22 - David Alejandro Romero Romero 
No, ahí tiene una consulta como para Martín, de todas formas va a quedar todo esto con de de las peticiones y todo lo demás que podría explotarse esta información a través de de en los logs agregar algún tag o

19:40 - Martín Vasconcelos 
algo para que sea fácil de identificar.

19:43 - Orador no identificado 
Hola, adelante.

19:45 - David Santiago Bohorquez Rodriguez 
Sí, aquí solo tenemos una duda y es, entonces, ¿la relación va a ser una cuenta? ¿Va a ser una cuenta o una cuenta por filial?

19:58 - Jenny Rodriguez 
No, una cuenta en donde tenemos a habilitar para todas las filiales.

20:04 - David Alejandro Romero Romero 
Y de todas formas, Jenny, como para apoyarte, esto es un único canal, o sea, no es que sean varios canales, es un único canal que tiene acceso a a seis cores bancarios diferentes, pero es un único aplicativo. Entonces, no, no es segmentable.

20:23 - Orador no identificado 
En sí, su esencia es ser uno.

20:26 - Frank Caicedo 
Gracias David. Vale, gracias. Vamos adelante.

20:28 - Fernando Guerrero 
No, yo solo quería recalcar solo para que quedemos todos en claro. Actualmente entiendo que la distribución de costos es un porcentaje fijo, según lo que ya entiendo definieron. Entonces, cualquier tema de que lo gestione la aplicación es algo que no está en el alcance actualmente, sino es más a futuro, ¿verdad? O sea, lo que estamos diciendo es que sí se podría hacer en el futuro.

20:49 - Jenny Rodriguez 
No, lo que estamos diciendo es que Martín dice, o sea, sí se va a considerar de una vez. Martín va a dejar todo planeado para que si después van a cambiar esa distribución, pues va a ser, va a tocar hacerlos a nivel de lo que trance la aplicación, los log, como se ha establecido, si es que luego quieren cambiar el modelo. Bueno, pero pues al igual con el que está definido, podemos arrancar.

21:16 - Orador no identificado 
¿Sí o no, Martín? Sí, sí.

21:19 - Jenny Rodriguez 
Todos alineados. No sé, señora Sandra, si le resolvimos sus inquietudes de momento. Que muy buenas. Muchas gracias. Buenas, señora.

21:32 - Jenny Rodriguez 
Bueno, entonces ya aclaramos el tema de las cuentas, ¿cierto? Entonces ya todos tenemos claro. Pensaría yo que sí sería entonces el, y no sé, Frank, si tal vez pues como esto ahora va a ser regional, no sé si dentro de la organización de la vivienda debería nacer. Creo que esto, bueno, también David y equipo de la vivienda hay que revisarlo, porque pues sí hay que definir en dónde van a nacer las cuentas, ¿no? Tanto para PER, como para cámara de compensación en que, bueno, creo que ese es uno de los primeros lineamientos. No sé, Frana y Johanna, ustedes me dirán.

22:07 - Speaker 8 
Ay, cuando dices dónde van a ir a hacer, ¿cuál va a ser la distribución de las cuentas?

22:13 - Franklin Garcia 
Sí, ¿en qué organización? Porque lo tenemos por ahí. Pero eso, digamos, no afecta mucho en costos ni nada. Simplemente es un tema organizativo. Y coincido con la idea de Jenny de usar algo que se llame regional o no sé, algo así, una organización que ahí tú digas, ok, no es ni Panamá, ni Honduras, si no es. Y regional abarca, pues, los países de Centroamérica, Colombia y los demás.

22:45 - Orador no identificado 
Listo.

22:45 - Speaker 8 
¿Cuál es el segundo paso, Jenny, que estás mencionando?

22:50 - Jenny Rodriguez 
Bueno, ese uno, definir en dónde se crean las cuentas. Paso número 2, bueno, no sé, Fran, ahí, no sé si sería primero ideal revisar los alineamientos con respecto a la parte de Dbox o que nos podamos entrar tal vez acá a empezar a hacer ese mapa o diagrama de pendencias con el cual, pues, esta solución se va a tener que integrar dado que, pues, va a tener que comunicarse con los 4 o 6 cores a nivel de las filiales. Ahí sí, no sé, ya como tal, empezar a dimensionar para, pues, empezar a hacer el mapeo y, digamos, tener como objetivo el empezar a habilitar, en este caso, la cuenta de desarrollo que sería la que en este momento Martín

23:38 - Franklin Garcia 
necesita, pues, para que el equipo pueda arrancar con la implementación de la aplicación. Sí. Lo primerito es definir ese mapeo. Saber cómo se van a manejar las interconexiones con premisa, por bancario. Que sea, que haga falta ahí. Si existe, entonces ya descartarlo, si no, crearlo. Lo segundo y no menos importante es el tema de los accesos al equipo, al Denon de DevOps de GitHub. El equipo debe tener una IP única, debe tener acceso a eso y los módulos que deben estar ahí en el DevOps. Los pipelines, todo eso. Deben estar ya creados para el proyecto para poder comenzar.

24:24 - Jenny Rodriguez 
Bueno, mibran, solo para complementar, entonces, ¿te entendería? ¿Ideal iniciar a hacer, entonces, mapa de dependencias? ¿Y entendería ahí también de una vez sumar el ítem o los lineamientos de seguridad también, cierto? ¿Para de una vez empezarlos a revisar o consideras verlos por aparte?

24:42 - Franklin Garcia 
Pues, debe ser una sesión aparte, porque seguridad se puede extender un poco. OK. Y yo creo que la dependencia va por otro lado, ¿no? Si esto va a interactuar con otras cuentas o otras cargas de otras cuentas que existen aquí, con algo en Colombia, en las cuentas de Colombia, o con algo en premisa, o con algo de cada país. O sea, hay que levantar bien eso porque esa es la base fundacional del proyecto y eso tiene que estar primero que nada. O sea, por lo menos mapeado para irlo haciendo mientras se hace el reto. Lo segundo es, DevOps, porque eso no sé qué tanto pueda tardar. Dependemos mucho del equipo de DevOps para que nos habiliten los accesos, los módulos, todo. Y eso hay que irlo gestionando lo más rápido posible. Y ya lo tercero sería seguridad. Que, bueno, básicamente sería decirles a ellos que necesitamos publicar una aplicación en algún momento y tienen que darnos, digamos, a alguien. Que yo daría para este proyecto es tener a alguien de DevOps dedicado para que nos resuelva cuando salgan issues y problemas con las pipelines y todo eso, y alguien de seguridad que nos pueda agilizar cualquier tema o bloqueante que tengamos en Colombia. Si no, pues todo se maneja con RTM y sabemos cómo es ese proceso. Pero si se puede tener a alguien, mejor. Pero serían esos tres casos, ¿no? Dependencia, DevOps y seguridad.

26:10 - Jenny Rodriguez 
Vale. Entendido. Entonces, bueno, esas serían como nuestras principales actividades en las que nos vamos a enfocar, pero ya digamos como next steps, entiendo, una vez hagamos estas actividades, podríamos ya como tal empezar a definir lineamientos de networking y conectividad para estas

26:27 - Franklin Garcia 
aplicaciones, ¿correcto? Sí, el tema aquí es que necesitaríamos de DevOps para poder desplegar VPC.

26:34 - Jenny Rodriguez 
Sí, alineados, alineados. Que están hablando de DevOps.

26:37 - David Alejandro Romero Romero 
En el banco ya tiene un estándar que ya se ha manejado en otros proyectos que está involucrado a escala. No sé si han escuchado al proyecto de Wiley's que ahí están usando estándar de banco, entonces es importante manejar ese estándar.

26:53 - Franklin Garcia 
Sí, de hecho, precisamente a eso me refiero, que hay solamente una persona que es Liliana, que tiene acceso ya al repo o al Tenant, digamos, pero Johan y Francisco, ¿no? Entonces hay que empezar a gestionar eso, ver qué módulos son los que vamos a usar, según la arquitectura, habilitarles acceso a ellos para que puedan desplegar y tener a alguien de DevOps, de ese equipo que hace el troubleshooting y todo eso, que nos apoye. Porque nosotros no gestionamos los pipelines allí ni los módulos. Si hay issues, del que sea, necesitamos el apoyo del equipo o del banco, o del regional, para que nos apoyen.

27:34 - Jenny Rodriguez 
Es cómo adoptar el modelo, David, que estamos gestionando con Waylist, que ahí tenemos una persona que nos ayuda con, si no hay algo definido, ver cómo se va a trabajar, de si se presenta un nicho, nos lo ayuda a resolver, si hicieron alguna actualización y demás. Como esos contratiempos que ustedes gestionan a nivel interno y si no nos dan visibilidad, muy probablemente cuando vayamos a hacer el despliegue o avanzar, pues vamos a chocar. Entonces, pues pensaría que el objetivo sería tener esa figura también en el equipo, de igual forma con el equipo de seguridad.

28:15 - Franklin Garcia 
Sí, por supuesto, hay que salir por imperio y todo aquello, entonces hay que gestionarlo.

28:21 - Jenny Rodriguez 
Alineados. Pues bueno, yo creo que si nadie más tiene inquietudes, pensaría que esos son, Entonces, ¿cómo los citen para empezar a trabajar? Y, pues, no sé si en esta sesión contamos con todo el auditorio para, entonces, empezarnos a enfocar en la primera sesión de determinar, entonces, el diagrama de dependencias, que, pues, en este caso la solución de PERT va a tener que interactuar con todas las filiales. Creo que ese es como el primer paso. Y ya, pues, posterior pensaría que lo de Dbox se puede ir trabajando en paralelo.

28:52 - Orador no identificado 
¿Estás aquí? Listo.

28:53 - David Alejandro Romero Romero 
Pues, quería indicar que ya existe un diagrama. Dependencias con el cual se hicieron estimaciones. Creo que lo compartimos, ahí se indican los servicios. Pero también hay que tener en cuenta que se hizo un único diagrama para toda la solución. Entonces, podría no tener el detalle suficiente que se requiera. Entonces, podrían revisar este como punto inicial. Y si es necesario, podemos empezar a mirar de hacer diagramas ya puntuales para para funcionalidades ya como para cada funcionalidad o como ustedes estén manejando el proyecto.

29:33 - Orador no identificado 
Alineados.

29:33 - Speaker 12 
Sí, una consulta respecto a los ambientes. Ahí, por lo que había comentado, creo que Franklin, la idea es tener todos los ambientes con el mismo nivel de seguridad ¿Con eso evitaríamos hacer pruebas en ambiente que tengan distintos niveles de seguridad al momento de hacer el pasaje? Sí.

30:01 - Orador no identificado 
Ok.

30:02 - Speaker 12 
¿Y eso también implica el ambiente de desarrollo? ¿Con lo cual, para contar con un ambiente de desarrollo, para empezar a hacer las primeras configuraciones del proyecto, despliegues y demás, deberíamos esperar los permisos de seguridad, o podríamos iniciar, tener un ambiente de desarrollo sin ese nivel de seguridad y después agregárselo. ¿Cómo creen posible eso? Yo para no demorar todas las tareas de configuración de ambientes, usuarios y demás. Sinceramente desconozco los tiempos que manejan en cuanto a autorizaciones y más con los equipos Me imagino que no debe ser algo trivial dentro del banco. Por eso es mi consejo.

30:53 - Orador no identificado 
Jenny, ¿cómo lo ves?

30:55 - Speaker 8 
Dejar un poquito más abierto desarrollo y de pronto sí replicar laboratorio con las mismas políticas y restricciones de producción. Tal vez esa fue tu pregunta, no sé cómo lo ves también.

31:07 - Sandra Ojeda 
Quizá más que una pregunta para Jenny, creo que es una pregunta para Fabián Zambrano. Entonces, ahí tenemos que alinearlo en banco. Porque toca mirar qué tan flexible te deja ser de seguridad dejar el envío.

31:23 - Orador no identificado 
Vale. Algo en adelante. Perfecto.

31:25 - Frank Caicedo 
Aquí tiene la mano levantada.

31:27 - Sandra Ojeda 
Bueno, un poco más con esa guía.

31:31 - Fernando Guerrero 
Van a haber revisiones de las historias de usuarios contra los formularios o el MVP con los funcionarios para ver cómo va a ser el proceso de implementación de esos temas? Eso puede ir en paralelo mientras va la infraestructura, ¿no?

31:49 - Speaker 12 
Sí, yo no hice esa consulta acá porque entendía que la reunión era más técnica, pero me la había guardado para hacérsela a Frank y a Carlos por mail. Nosotros lo que necesitaríamos en ese sentido es acceso a Jira, o a la herramienta creo que a la que vamos a usar para la gestión, para el seguimiento, así empezamos a cargar ahí las historias y a validarlas, y a validar el alcance de la dependencia, y necesitaríamos acceso a los prototipos, que en la documentación indicaba que en el momento de iniciar el proyecto nos lo iban a publicizar. Con eso, ya tenemos, con Abuel, que será nuestro analista funcional, ya tenemos como para empezar a volcar y a revisar, nosotros ya lo hicimos, pero bueno, ya dejarlo en la herramienta con la que vamos a estar trabajando.

32:48 - Fernando Guerrero 
Sí, eso para mí es importante porque con la experiencia que disponemos, o por lo menos tengo, es que a veces las historias usuarias no son tan detalladas y hay cosas como reglas de negocios que no se ven, entonces tal vez en esas revisiones que se hacen se puedan aclarar y pues evitar cualquier dicho futuro, ¿no? Y obviamente tener una documentación aprobada por el banco, que es la que se estaría implementando por ustedes, ¿no?

33:17 - Speaker 12 
A nivel de la funcionalidad. Sí, sí. Sí, por supuesto. Y sobre todo porque tenemos el proyecto en un alcance fijo. Así que tenemos que avanzar sobre firme.

33:28 - Fernando Guerrero 
Sí, y aparte poder ganar tiempo adelantando eso y no esperar en principio para avanzar eso, ir en paralelo. Por supuesto.

33:36 - Speaker 12 
Ahí Frank, no sé si Frank o Carlos, quién se lleva el tema, pero bueno, lo mismo en los canales de comunicación, en el canal de Slack íbamos a habilitar interno con Scala, posteriormente Meet con el banco, bueno, nosotros estamos a la espera, entendemos que ya se va a estar dando en estos en estos días, si no soy indignada, vamos a estar en el pasado, para poder empezar a trabajar sobre la definición futura.

34:12 - Frank Caicedo 
Sí, Cole, está adelante.

34:14 - Orador no identificado 
Sí, correcto.

34:15 - Fernando Guerrero 
Hoy vamos a crear los canales, tanto el interno para tener ahí la comunicación con el equipo de desarrollo y con la vivienda. Aunque en la vivienda entiendo yo que hay una restricción de ciertos países, a chatear con con personas externas pero si es directo, por ejemplo, si crean un grupo y lo crea Colombia, es fácil porque ahí no hay problema, pero

34:42 - Fernando Guerrero 
si yo quiero hacerlo directo con ustedes no podría, tiene que ser alguien, un grupo que creen, que no sé si lo van a hacer por país o va a ser uno solo, pero tiene que crear Colombia, Colombia. No lo podemos crear cada país. Por ejemplo, si yo creo uno en Costa Rica, no puedo agregar nadie de un tercero, salvo que sea de la vivienda. Pero Colombia en este momento sí puede, por el momento. Entonces, ahí yo hemos podido hacer comunicaciones, he podido comunicarme o hacer este comentarios o requerimientos a un externo y no tengo problemas.

35:21 - Fernando Guerrero 
Ya. Ok, entonces en este caso les diría que lo creen.

35:25 - Sandra Ojeda 
¿Tenemos alguien de seguridad ahorita en la sesión?

35:36 - Orador no identificado 
¿Tienes alguna consulta?

35:40 - Speaker 8 
Vamos a tener que tener una sesión con ellos.

35:52 - Franklin Garcia 
con ellos porque esta arquitectura es muy diferente a la que nosotros hemos manejado con otras con otras iniciativas como cyberbank aquí son servicios administrados de amazon contenedores y esas cosas y ellos limitan mucho el tema de la salida hacia

36:08 - David Alejandro Romero Romero 
internet entonces no y en cyberbank también debe estar limitada a internet toda esa exposición de apis debe ser privada y sale por la carpa que se llama imperva Exactamente, entonces todo esto... ¿A qué le puedo detallar un poco más el diagrama enfocado a networking, para asegurar toda esta salida hacia internet y también las conexiones hacia un premium? Y ya hacer más ese detalle.

36:38 - Franklin Garcia 
Sí, sí, es importantísima esa secuencia de seguridad.

36:42 - Jenny Rodriguez 
Vale, David, ahí para responderte, cuando hicimos el levantamiento trabajamos con este diagrama que tiene dos y mapea efectivamente la conectividad con países y como con la fuente responsable. No sé si de este vos me puedas compartir más bien la fuente y ya con base en eso entonces trabajamos en ese diagrama ya más orientado a sólo el esquema de conectividad que como tal pues quedaría, que debería quedar habilitado para las cuentas de PERI y cámara de compensación.

37:14 - Orador no identificado 
¿Listo? ¿Listo?

37:16 - David Alejandro Romero Romero 
Sí. Yo creo que nos tocaría en dos frentes, Jenny. Un tema que sea más técnico de networking y todos esos temas de seguridad. Y este diagrama que muestras es más de integración de servicios. Entonces, como mencioné hace un rato, este diagrama está muy alto nivel, está todo el proyecto. Y si necesitamos más detalle, pues podemos coger puntualmente la funcionalidad de single sign-on y hacer un diagrama del single sign-on y entender ser el single sign-on de punta a punta. Y asimismo con cada funcionalidad que se necesite para identificar los servicios y las integraciones.

37:52 - Jenny Rodriguez 
Mucho mejor. Sí. Yo creo que sí. Nosotros desde infra lo necesitamos. Y creo que Martín también desde la parte de aplicación también lo necesita.

38:02 - David Alejandro Romero Romero 
Sí, creo que sobre todo de aplicación.

38:04 - Martín Vasconcelos 
Si podemos empezar por lo de single sign-on, ya podríamos ir organizando una reunión.

38:10 - David Alejandro Romero Romero 
Sí, pues, si lo necesitan empiezo a construir diagramas, pues, ya, una cantidad N diagramas, dependiendo cómo esté segmentado el proyecto. Y sería así como nuestra base de integraciones.

38:26 - Fernando Guerrero 
Sí, por el Spring.

38:29 - David Alejandro Romero Romero 
Sí, por Spring o por funcionalidad. Hay como 20 funcionalidades en el primer entregable, Entonces, serían 20 diagramas que corresponden a eso. Sí, no hace falta que los haga los 20 ya, pero.

38:43 - Martín Vasconcelos 
Claro, ahí vamos con el avance, se van generando. Lo vamos hablando, pero ya te digo que me parece que lo primero va a ser lo de Single Sign-On, porque aparte es lo que más dudas técnicas, digamos, nos genera. El resto me parece que son llamadas a servicios. Tengo que verlos en qué orden y todo, No pareciera haber ningún misterio con eso. Decirles, Añón, tenemos que terminar de entender bien cómo es el login en cada una de los portales y todo eso.

39:15 - Orador no identificado 
Listo.

39:15 - Martín Vasconcelos 
Así que, bueno, después avísame y lo organizamos para juntarnos y lo revisamos. Sí, sí, sí.

39:21 - David Alejandro Romero Romero 
Nos podemos juntar con Jenny, que también ahí tengo unas dudas de mi lado hacia ustedes de la autenticación de clientes y cómo van a manejar el token, que en el diagrama no donde se va a validar el toque de clientes. Pero lo detallamos en una sesión. Enfocada a todo lo que sea autenticación. Tengo el sign up. Busquemos el espacio.

39:43 - Orador no identificado 
Vale.

39:43 - Jenny Rodriguez 
Yo creo que nos toca entonces dividirlas en dos. Una orientada netamente a temas de conectividad, ¿cierto? Que, pues, en este caso serían las dependencias con las cuales Per va a interactuar. Y pensaría que ya la otra va más ligada al tema de las funcionalidades de la aplicación y flujos de las cosas, pues, que se van a reutilizar, que hoy en día ya tiene el banco.

40:13 - Orador no identificado 
¿Correcto? Sí, correcto, Jenny. Listo.

40:15 - Frank Caicedo 
Chicos, ¿algún punto adicional? ¿Alguna duda? Vale, Sergio. Ahí haremos sesiones internas para alinearnos con Mobile Computing y Scala sobre qué actividades se necesitan para que se vaya construyendo cada uno de los, del backlog que se va a trabajar. Entiendo que hay información del negocio que hay que también levantar. Ahí identificamos qué información necesitas o necesitas Mobile Computing para empezar a construir las tareas o el backlog de cada una de las funcionalidades. Y luego vamos definiendo en base a las tareas que se vayan generando, cuánto de sprint vamos a iniciar o qué va a ser el goal de cada Si va a ser, no creo que sean 20 sprints. Pueden ser sprints donde incluyan varias funcionalidades. Como vimos el martes, pues no hay un tiempo fijo para cada sprint. Puede ser de 2 semanas, 3, 4 semanas. Ahí vamos viendo en base al peso que tenga cada uno de esas funcionalidades. Pero, bueno, el resto lo coordinamos interno contigo y con Martín para ver qué paso siguiente necesitamos para construir ese backwards.

41:22 - Fernando Guerrero 
Perfecto. Talísimo, gracias. ¿No? David. Adelante David. Perdón, disculpa, no, termina ahí. No, no, no, no parte que va a ser el inicio del single sign-on hacia ustedes. Entonces, también para que ya vayan gestionando eso. Y entiendo que va a haber también un cierre de sesión o algo por el estilo ley de la historia del usuario que ya deberían de estar procediendo a implementar el proveedor.

42:09 - Frank Caicedo 
OK. Sí, esto es una referencia del 1 al 20. No es consecutivo. Vemos ahí cuáles son las que tienen más relación. Y ahí se hacen, se consolidan para hacer varias en 1,30. Bacán. Para el resto del equipo, al menos de escala que ya está definido, para, digamos, ir como ahorrando ese tiempo para poder trabajar con el equipo.

42:28 - Speaker 5 
Sí, sí, sí, entre que estamos preparando el backlog y los accesos, ¿no? Solamente eso.

42:56 - Orador no identificado 
Excelente. Sí, buenísimo.

42:57 - Frank Caicedo 
Un buen punto para levantar y hacer tareas en paralelo. Lo vemos interno y ahí lo vamos procesando. Gracias, Diana. No sé si el lado de la vivienda, alguna inquietud más, algo que se deba tratar.

43:17 - Nicolas Leon Perez 
Diana. Entonces más bien más bien ahí como siempre entre tú y Sergio eh vamos revisando y vamos a ir perdón eh poniendo las las agendas y y viendo ahí como lo habíamos hablado en las mañanas siempre para para empezar a

43:33 - Frank Caicedo 
tener esas mesas de trabajo ¿Listo? Vale, seguro. Muchas gracias. Vale. Liliana, ¿No se sigue adelantando la mano otra vez o se te fue la mano? Si me puedes dar una otra duda o algún comentario. Dale, Mobile Computing. ¿Alguna duda adicional, Martín? No, de nuestro lado.

43:53 - Speaker 12 
No, de nuestro lado.

43:55 - Frank Caicedo 
Vale, eso es para todos. Gracias por la asistencia. Continuamos con los siguientes pasos. Ya conversamos y vamos convocando a las sesiones que sean necesarias para continuar con la actividad.

44:09 - Speaker 12 
Gracias y buen día. Dale, gracias. Saludos.

44:13 - Orador no identificado 
Saludos. Gracias.

44:14 - Fernando Guerrero 
Un placer.

44:16 - Frank Caicedo 
Un placer también. Carlos. San. Ajá. Bueno. Esto merece un un PM como tú, que conoce la parte técnica, porque hay momentos en los cuales no No ubico la necesidad que tengan sobre algunos tópicos, ¿no?

44:46 - Fernando Guerrero 
No, pero ahí sí. Lo que toca es ser bien estructurados ahí con el seguimiento y la organización del proyecto. Entendería entonces que los siguientes pasos es, se van a buscar estas dos reuniones, ¿verdad? O esta sesión para el tema de las dependencias.

45:09 - Frank Caicedo 
Sí, no sé qué se refiere con dependencias, no sé si es un término de vivienda o un término AWS.

45:20 - Fernando Guerrero 
Sí, no, dependencias se refieren a, digamos, esta aplicación va a tener que comunicarse con múltiples otras aplicaciones, ¿verdad? Y elementos de la vivienda. Entonces, ese mapa de con quiénes va a interactuar, al menos a alto nivel, porque eso hay que irlo previendo desde un inicio y ejecutando. Y también entiendo yo temas de diferentes funcionalidades de la aplicación, ¿verdad? Qué cosas tal vez ya hace otro elemento y cómo va a interactuar con en la aplicación que van a desarrollar acá, y los flujos de información, etcétera. Más o menos a eso entiendo yo que se refieren, ¿verdad?

46:11 - Orador no identificado 
Sí.

46:12 - Fernando Guerrero 
O sea, es como quebrar esa arquitectura, porque esa arquitectura que nos presenta Jenny es una arquitectura más a nivel de infraestructura, ¿verdad? Pero a nivel de eso, a nivel de aplicación y todo, hay todo un diagrama, unos diagramas de flujos y temas que se tienen que tener bien Entonces, eso entiendo yo qué es lo que se refieren. Y por lo que entiendo, el más, digamos, uno de los que más tienen, uno de los prioritarios ahorita para empezar, es este, el de single sign-on, para entender bien cómo va a ser toda esa interacción y comunicación, ¿verdad?

46:47 - Frank Caicedo 
Y ese flujo de información. Sí, está igual. En la parte de recesos, ¿eh? Sí, bueno, ahí más que dar adelante.

46:54 - Fernando Guerrero 
No, eso es, yo creo que deberíamos de hablar con Jenny, ¿verdad? Para más o menos cómo lo quiere manejar ella, cómo hacemos estas sesiones, invitar a los que tengamos que invitar, o sea, no todo mundo, ¿verdad? Porque en las sesiones cuando hay mucha gente, ¿verdad? Y ver si cómo lo... Y es más fácil cuadrar una sesión con poca gente que con un montón, ¿verdad? Entiendo yo que el resultado esperado de esas sesiones es es todos esos diagramas, esos diagramas que tienen que tener claros los desarrolladores y todo el equipo antes de empezar a trabajarlo, ¿no?

47:32 - Frank Caicedo 
Sí, de hecho ahí, yo creo que era Darwin que comentó, él hablaba de las HU, yo no sé, no quise preguntarlo para no comprometerlo, yo no sé si el lado de la vivienda ya tiene la historia de usuario escrita para cada una de estas funcionalidades. Yo entiendo que sí. Sí, ese sería el paso uno, que ellos nos pasen esas historias de usuarios, pero el paso uno no, uno lo pasa en En base a eso, con Mobile Computing, irles leyendo y que ellos vayan viendo qué información adicional necesitan de la vivienda para complementar ese sector usuario.

48:03 - Fernando Guerrero 
Sí, con ese tema a mí me queda la duda que Mobile Computing dijo que necesita acceso a un Jira. Entonces, no sé si sería el Jira del cliente o un Jira nuestro. No, el nuestro.

48:18 - Frank Caicedo 
Es lo que te comentaba también. Porque ellos también usan Jira, pero hay que explicarle a Sergio que no es que tú vas a trabajar con mi Jira, tú pásame tu plan.

48:32 - Fernando Guerrero 
Eso es lo que están pidiendo ellos, ellos tener acceso a nuestro Jira. De alguna manera sí tiene que haber una forma de que ellos, porque al final son nuestro equipo, o sea tenemos que verlos como desarrolladores, ¿verdad? Entonces ellos tienen que actualizar status, poner comentarios, etcétera. Entonces sí tienen que haber algún mecanismo para que ellos interactúen ahí y habría que analizar si se puede con nuestro JIRA, ¿verdad? Sí, he preguntado eso, ¿no? Yo lo primero lo he preguntado a Obis.

49:07 - Frank Caicedo 
Si se puede hacer que alguien externo entre al JIRA. Yo entiendo que sí se debería poder, ¿verdad?

49:14 - Fernando Guerrero 
Pero es un tema de los que administran nuestro YIRA.

49:19 - Frank Caicedo 
Exacto. Acceso. Acceso. YIRA. Yo trabajaba con otros proveedores, en el banco.

49:25 - Orador no identificado 
Ellos me pasaban su plan.

49:28 - Frank Caicedo 
Ellos tenían su plataforma de proyectos, cualquiera. Me pasaban las tareas y su avance. Y en base a eso, lo ponderaba y lo colocaba en el proyecto del banco. Pero si ellos quieren entrar, y pueden entrar, perfecto. Si no, ellos tendrán que tener su propia gira, sus propias actividades, y nos reportan a nosotros semanalmente cómo va ese plan. O si es difícil entrar en gira para ellos. Entonces, yo le pregunto a Novi, a ver si ella tiene experiencia con algún otro proyecto en el cual se haya hecho todo eso. O si es muy complicado porque no tienen usuario de escala.

50:07 - Orador no identificado 
Sí.

50:07 - Fernando Guerrero 
Lo que pasa es que ellos, entiendo yo que ellos, pues, ellos sí quieren empezar como a, Toda esa información que ellos ya tienen de las historias de usuario, que por lo que le entendía a este, ¿cómo se llama? No, el PM de ellos, ¿cómo se llama? Por lo que le entendía a este Sergio, ellos ya empezaron a trabajar como en desarrollar esas historias de usuario o a revisarlas y como desagregarlas, no sé. Pidiéndoles el acceso al giro para empezar a volcar ahí toda esa información.

50:45 - Frank Caicedo 
Sí. Entonces, yo creo que no sé cómo tuvieron ellos esa historia de usuario. Bueno, o sea.

50:50 - Fernando Guerrero 
Es que hay un documento, hay un documento en el documento de la, de la, de la, donde venía la propuesta y todo eso. Jenny pasó un documento donde ahí están las historias de usuario a alto nivel, ¿verdad? O hay historias de usuario. Sí, pero hay una, hay una, hay un documento donde ya definen ellos una especie de historia lo voy a buscar si quieres y lo vemos.

51:13 - Frank Caicedo 
Yo tengo jefe que son las funcionalidades. No, pero hay un documento más a detalle.

51:19 - Fernando Guerrero 
Yo lo vi y supongo que ese documento ya lo tiene Mobile. Entonces, en base a eso ellos tienen que empezar a quebrar eso, ¿verdad?

51:30 - Frank Caicedo 
Lo que yo recomendaría, que ellos tienen esa documento. La idea es reunirse con, o sea, hacer un refinamiento, porque ellos entienden, todos los que están allí lo entienden como tal, este, el, si el modelo computador tiene todas las funcionalidades como las expresó la vivienda. Correcto. Claro. Sería como el screen planning. Sí, correcto.

52:01 - Fernando Guerrero 
Refinamiento de ¿verdad?

52:03 - Orador no identificado 
Sí.

52:03 - Frank Caicedo 
Hay que reunirnos con Martín y con Sergio. Mira, de estas 20 personalidades, si ya tienen pensado cómo pueden ir agrupando. Luego de eso, invitar sesiones con el cliente, con la vivienda. Miramos hasta trabajar las 2, las 6 y las 12. Ok. Vamos con la vivienda para ver si ustedes entienden, etc. Los usuarios, si tienen dudas. O si tienen consulta, cuando yo tengo, ellos definan que no tienen dudas o esas tres o cuatro funcionalidades, aunque vamos a darle play con el Spring Boot. Sí, creo que sería una buena opción.

52:42 - Fernando Guerrero 
No sé cómo se ve, ¿no? Sí, sería bueno, digamos, también, quizás, o sea, en algún punto creo que sí sería ideal tener alguna SYNC así, tal vez, semanal o bisemanal, solo nosotros tres, o sea, solo nosotros, Sergio y Nicolás, ¿verdad? Como... ¿Nicolás se llama? El PM de... Sí, Nicolás, sí. Ajá, como para ir haciendo un... O al menos nosotros y Sergio, ¿verdad? Para ir viendo cómo...

53:09 - Frank Caicedo 
Sí, primero Sergio... Organizarlo a nivel de PM, ¿verdad? Sí. Por claro, eso que Sergio dijo en la sección no tuvo que haberlo dicho porque eso es algo interno nuestro, ¿no? Sí.

53:21 - Fernando Guerrero 
Sí, sí, sí, sí.

53:23 - Frank Caicedo 
Bueno, capaz que es parte de que somos somos los parientes en todas las cosas. Me gusta así, pero bueno.

53:30 - Fernando Guerrero 
Sí, no, está bien. Lo que hay que estar así, digamos eso. Ya ves que este Sergio creo que le dijo a alguien de debienda. Ah, cuando quieras lo vemos y nos reunimos y eso, ¿verdad? Pero siempre dejarles claro que tenemos que hacerlo nosotros.

53:43 - Frank Caicedo 
Exacto. Nosotros somos los que tenemos que hacerlo. Bueno, de lo que está pendiente, Carlos, no sé qué quieres que haga yo, no sé qué puedas hacer tú.

53:53 - Fernando Guerrero 
No, mira, yo voy a empezar a hacer los canales de Slack, y voy a ver si hacemos el de Teams con el cliente. Ahí, Luis, por lo que comentaron, lo ideal es que lo haga este mismo Nicolás. O sea, que él sea el dueño del canal, porque entonces así él puede invitar a la gente de Costa Rica y él nos puede invitar a nosotros.

54:14 - Frank Caicedo 
OK. Entonces, se le preguntaron hoy lo de Gira y convocó a Sergio para hacer nuestra sesión un tema. O sea, una inicial, pues. A Sergio.

54:23 - Fernando Guerrero 
Sí, sí, sí. Sí, sí, sí.

54:25 - Frank Caicedo 
Sí. Y ahí. Sí, correcto. En esa sesión definimos, se define, vamos a hacer una semanal y que día. Sí.

54:33 - Fernando Guerrero 
Y yo también voy a hablar con Jenny a ver cómo manejamos el tema de las, de las, de la creación de diagramas y eso para ver qué reuniones gestionamos.

54:44 - Orador no identificado 
Ajá.

54:44 - Frank Caicedo 
Bueno, yo le escribo a Sergio. Bueno, lo va a mandar a Sergio, así como hacemos con los clientes. Tres propuestas. Y para hablar sobre su, si ya tienen estimado, el orden de la HU. O sea, la funcionalidad.

54:59 - Fernando Guerrero 
¿Tú no has visto si ellos usan Google o cómo? Miren, no me han dicho nada.

55:05 - Frank Caicedo 
Yo la he invitado por Google Meet y no me han dicho nada sobre eso.

55:11 - Fernando Guerrero 
Ya, ya, ya. Es que si ellos usaran Google sería muy fácil que nos compartiera él, al menos él, su disponibilidad.

55:20 - Frank Caicedo 
Así es fácil. Pero, si quieres, le preguntamos. Y con ellos también hay que crear un canal XT, ¿no?

55:31 - Orador no identificado 
Sí, también.

55:32 - Fernando Guerrero 
También. Tenemos que definir esos, ajá, cómo vamos a manejar los repositorios de. Hagamos un, voy a, una ufole externo y ahí le damos acceso a ellos y a la vivienda.

55:47 - Frank Caicedo 
Voy a querer uno para la vivienda y uno en la misma ruta para MC.

55:53 - Orador no identificado 
Ok, va.

55:54 - Frank Caicedo 
En la sesión, porque a veces hay cosas que van a compartir ellos que no van a caber por un correo. La vivienda y el móvil computer. Vale, se me llevo. Lo de Jira, convocó a sesión con para los pasos iniciales y crear el XT para la vivienda y mover computadoras.

56:15 - Orador no identificado 
Ok.

56:15 - Fernando Guerrero 
Yo me encargo de los chats y voy a ir gestionando la sesión para el tema de los mapas de dependencias. Perfecto. Seguro que sí. Hay un tema ahí que tenemos que ver, que es los accesos a los repositorios. Perdón, los accesos a GitHub y eso. Eso también tenemos que hablar con Sergio.

56:38 - Frank Caicedo 
Eso es lo que dijo, ¿a qué? No fue lo de Ileana, ¿no?

56:42 - Fernando Guerrero 
Sí, lo que dijo Ileana, lo que dijo Ileana.

56:45 - Frank Caicedo 
Eso es las cuentas. Las cuentas, claro, que si va a ser una sola cuenta, por lo que entendí, para todo. A las cuentas, si se da a una sola cuenta, ¿no? A la cuenta, para equipo, pero la cuenta ya está creada, eso fue lo que no me quedó claro.

57:00 - Fernando Guerrero 
Sí, no, lo que tenemos que hacer, bueno, Es el tema de, para el tema de los despliegues y todo, tenemos que tener acceso, el equipo tiene que tener acceso a Github, a Github del cliente. Entonces es una gestión.

57:18 - Frank Caicedo 
Ah, entonces queda la cuenta WS.

57:21 - Fernando Guerrero 
No, no, la cuenta WS las tiene que hacer, las tiene que generar nosotros, las tenemos que generar. Entonces es es otro hilo que tenemos que darle de seguimiento.

57:35 - Frank Caicedo 
Entonces es la cuenta de la vivienda. Sí. Se le pide también a Nicolás. Supongo que todo eso está con Nicolás.

57:44 - Fernando Guerrero 
Entonces nos reunimos con Sergio y de ahí después nos reunimos con Nicolás.

57:50 - Frank Caicedo 
Tenemos que reunirnos con Sergio y con Nicolás. Sí, primero con Sergio para saber todo su enfoque y esto con Nicolás. ¿Con Nicolás solo o con Nicolás y Sergio?

58:02 - Fernando Guerrero 
Mejor primero con Sergio y después con Nicolás.

58:05 - Frank Caicedo 
Sí, pero ¿con Nicolás solo o con Nicolás y Sergio? Pero también Sergio, también Sergio. Ok, buenísimo. Entonces eso lo definimos cuando nos volvemos con Sergio. Buenísimo. Bueno, Carlos, chévere. Dale, bueno. Si te falta una sesión para aplicarte lo de la matriz, esa que te dejé, me dices. Dale, Frank. Vale, pues.


---
