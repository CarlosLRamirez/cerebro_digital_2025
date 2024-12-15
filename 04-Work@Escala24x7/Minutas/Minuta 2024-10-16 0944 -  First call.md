---
type:
  - Minuta
IDProyecto: "11210"
date: 2024-10-16
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
2024-10-16

## Asistentes

### LE
* Nick Getchman
* Nancy Vargas
* Daniel Valverde
* Roy Flowers
### Escala24x7
- Carlos Leonel Ramírez
-  Jorland Delgado
- Jorge Ovalle
- Camilo
- Eduardo
- Juan Paz
- Cesar Gomez
- Gustavo Rojas
- Jose Raborg
- 

## Agenda
* 
## Temas Discutidos
*  Introduction
* Operating model
	* Tier1: Escala
	* Tier2/3: LE
	* We need to build a RACI for AIX, RACI for IBM exists
	* Jorge Ovalles will take the responsablity to build the RACI???
	* LE: Connectria Tier1/Tier2/Tier3 at the beginning
	* We need to engage the client, to understand the client expectation
	* SOW: expectation March 2025 Escala will take Tier1 support
* Engagement Language
	* Jorland/Cesar take the conversation in spanish
	* Meeting properly prepared prior with LE
	* Structured Agenda, in spanish, Escala lead the meeting: a request from the customer
* Camilo/Daniel Valverde roles
	* Take lessons to replicate to other engagement
	* Escalation from both teams
* Close eye on any change request
* AWS planning with IBM planning (alignment)
* On site visit
	* Richard Dolewsky proposal
	* Initial review planning with LE/Escala24x7
	* Bogota, Colombia
	* Client will assume the cost, it is in the SoW
* Next Step
	* Have the project plan, framework of the plan end of  the next week
	* Design and connectivity in place
	* Start with non-production systems
	* Priority list of the systems, the first five #followup 
		* Test
		* DR
	* November, December, focus on operations.
	* Nick will send me a SoW Summary, non formal
	* 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
