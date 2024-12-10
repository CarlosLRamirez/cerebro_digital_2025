---
type: Minuta
IDProyecto: "11152"
date: 2024-08-22
---
`

### Seguimiento

```dataviewjs
let projectID = dv.current().IDProyecto;

// Función para filtrar tareas según las condiciones comunes
function filterTasks(tasks) {
   return tasks
        .where(t => t.tags.includes("#followup"))
        .where(t => !t.tags.includes("#backlog"))
     .where(t => !t.completed)
        
}

// Obtener todas las páginas que tienen tareas relacionadas con el ID del proyecto
let tasksByProperty = filterTasks(dv.pages().where(p => p.IDProyecto === projectID).file.tasks);

// Obtener todas las tareas que tienen el tag del ID del proyecto
let tasksByTag = filterTasks(dv.pages().file.tasks.where(t => t.tags.includes("#id" + projectID)));

// Combinar ambas listas de tareas y eliminar duplicados usando un Set
let combinedTasks = [...new Set([...tasksByProperty, ...tasksByTag])];

// Mostrar la lista de tareas
dv.taskList(combinedTasks, { asOf: dv.date("today") });
 ```
## Fecha de Reunion
2024-08-22

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Antonio Florez

## Agenda
* Sync
## Temas Discutidos

- Gestion de accesos con privilegios para Connectria
	- En Bancolombia existe un área que se llama "Control de Accesos" quienes son los que controlan el acceso para los usuarios provilegiados
	- En el banco funciona asi: si usted necesita un QSOCFR o un ALLOJECTS, usted tiene que solicitarlos por Cyberark y Control de Accesos es quien debe autorizarlo
	* Hoy Kindryl lo hace de esta manera
	* La pregunta es que si en Connectria podria funcionar de esta manera.

* Monitoreo de las maquinas en Connectria 🚩
	* Actualmente el banco tiene un área que se llama CoES (es un centro de monitoreo, donde ellos tienen peronal 24x7 por cada proveedor. Con los equipos en Connectria no va ser a asi
	* El banco  saber que tipo o plataforma de monitoreo van a tener acceso y como se podria integrar al CoES, por ejemplo tener acceso a un dashboard, o si ellos pueden integrar a su propio dsahboard a tarvez de un API, etc..
- Herramientas de Monitoreo de 3ros actuales:
	- Actualmente en las máquinas hay un SW de monitoreo que utiliza Kindriyl llamado Nimbus, ese se tendria que deshabilitar.
		- El banco necesita que tipo de alertas se van a tener, por ejemplo hay evento que debe estar monitoreado y es cuando los archivos de un usuario empiezan a llenarse, lo cual suele pasar, esto debe ser alertado.
	* Tambien actualmetne tienen instalado IBM iDoctor 🚩
		* Con eso monitorean Full Open Close - Activation Groups - Bloqueos en base de datos
		* Con esto tienen un inventario actualizado,  y un conjunto de herramientas a muy bajo nivel para monitorear ciertas cosas que pasan en la maquina
		* La pregunta es: si no tenemos ese SW como podemos monitorear lo que actualmente hace iDoctor?

* Automatizaciones durante un DR
	* Hoy en dia Bancolombia utiliza CRO, CRO es una herramienta que se las dio Kindryl por el servicio del DR (IBM Cloud Resiliency orchetration)
	* Esa herramienta es capaz de controlar (automatizar) todos los pasos para swichearse al DR, ellos antes tenian un paso a paso, ahora todo lo hace CRO
	* El banco quiere saber como lo vamos a hacer en el DR que ya no vamos a tener CRO. Nos vamos a devolver a hacerlo manual nuevamente o que herramientas tienen Connectria
	* Necesitamos empezar a revisar las tareas que hay que hacer y ver como lo automatizamos. 
* Pruebas de DR
	* Hoy en dia cuando el banco hace una preuba de DR, el proceidmiento es que opera en el sitio alterno durnate un tiempo determinado (por. ejemplo 1 semana) 
	* La expectativa del banco es que esto se mantenga igual en Connectria
	* De acuedo con el equipo comercial esto ya se definio que no es posible en Connectria, debemos alinear como vamos a responde resto al cleinte.
* El banco va instalar Dynatrace
	* Eso puede ser un alma de doble filo, debemos alinear esto con Connectria
* Respaldos en Connectria 🚩
	* Debemos conversar con Connectria sobe como va funcionar.
	* El cliente va utilizar PRI para hacer los backups en VTL
* Crecimiento de recursos adicionales de Nacional
	* Ahi es donde viene el tema del DS
* Reportes mensuales
	* Debemos mostrarle al Banco cuales son los reportes que vamos a incluir, como punto de partida
	* Tambien hay reportes quincenles que al Banco le interesan
	* Debemos acordar con el Banco cuales van a ser los reportes y la periodicidad. 
	* Debemos incluir al equipo Operaicones Escala24x7
* Infomrme de SOCKS
	* 




---




## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
