---
type:
  - minuta
IDProyecto: "11105"
date: 2024-06-25
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
2024-06-25

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Second LPAR resources
	* Nick need to confirm how much RAM we have for the second LPAR.
	* CPU?
* LPAR DR
	* Only 256GB, Richard says will be willing to increase RAM to 512GB for testing
	* Complete in two weeks, from when they deliver the DR LPAR (start 27/Jul + July/12th) if we go beyond that, we will have an invoice.
* Calls with Soon
	* Any coordination with  Soon, need to go through Nick.
	* Nick doesn't have availablity tomorrow.
	* Sean suppose to be shadowing for everything Soon does.
## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`