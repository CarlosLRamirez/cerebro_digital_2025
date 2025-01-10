---
type:
  - minuta
IDProyecto: "11152"
date: 2024-07-22
---

``

### Seguimiento temas previos

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
2024-07-22

## Asistentes

### Cliente
* Erwin Hidalgo Cardenas
* Pastor Fernando De Los Rios
* Walter Aníbal Duque
* Maria Elsy Giraldo
* Didier Giovanni Cairasco
### Escala24x7
- Carlos Leonel Ramírez
- Camilo Villamil
- Antonio Jose Florez

## Agenda
* Discusión sobre la estrategia de migración de Nacional
## Temas Discutidos
 - Cuales son los riesgos de Fidu solo
	 - Los deltas se tienen que llevar por Mimix
	 - Se deben configurar los DataGroups en Mimix considerando el acomplamiento entre las aplicaciónes
	 - Existen aplicaciones transversales como el menú dinámico
	 - Van ha haber objetos del SO que podrían cambiar y podrían no estar iguales en las dos maquinas
	 - En un momento dado tendríamos unos DG replicando en diferentes vías.
	 - Los usuarios tendrían que conectarse a dos máquinas.
	 - Si hacemos una sola OLA, solo tendríamos que usar un DNS.
	 - Walter dice que esos riesgos ya estaban superados y estaban aceptados.
	 - Antonio dice que desde el comienzo dijeron que se fuera en una sola Ola, y Walter indicó que era mejor comerse el elefante en pedacitos.
	 - Maria Elsy, Walter y Antonio discuten 
	 - Walter enfatiza los retos a superar
	 - Didier tiene una lista con los retos a superar, el principal la sincronización diaria como superar falta de superacación.
	 - Riesgos:
		 - Ampliación de Cronograma
		 - Impacto a usuarios, cantidad de soporte por hacerlo como BigBang
		 - 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
