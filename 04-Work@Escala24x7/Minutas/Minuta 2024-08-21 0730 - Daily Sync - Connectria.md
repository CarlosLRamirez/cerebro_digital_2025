---
type: Minuta
IDProyecto: "11152"
date: 2024-08-21
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
2024-08-21

## Asistentes

### Connectria
* Josh Patterson
* Nancy Vargas
* Rob Cross
* Roy Flowers
* Jason Waller
### Escala24x7
- Carlos Leonel Ramírez
- Eduardo Franco
- Jose Rabord

## Agenda
* Se está revisando porque podría haber una oportunidad de generar el backup en cintas lto
* Vamos a programar reunión con kyndryl y connectria para establecer los requisitos para replicacion entre vtl
## Temas Discutidos
*  New Environment to migrate to Connectria (CALIDAD)
	* Left all the information
	* A new quote, today we have a meeting at 2pm to sync everything up
	* We need Connectria team on this call
* Backup on SUFI PRO
* Two system are restored
* Tony questions are answered
* { } Is there any space available on the SAN, we need to ask for this 
	* 70% is the recomendation
	* We need to ask this to Kindryl
	* Lower the utilization - allocate a couple of volumes
	* 


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta 2024-12-12 0935 - Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
