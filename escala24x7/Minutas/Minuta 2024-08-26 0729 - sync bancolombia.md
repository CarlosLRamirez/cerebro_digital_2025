---
type: Minuta
IDProyecto: "11152"
date: 2024-08-26
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
2024-08-26

## Asistentes

### Connectria
* Josh
* Nancy
* Roy
### Escala24x7
- Carlos Leonel Ramírez
-  Eduardo
- Antonio
- 

## Agenda
* 
## Temas Discutidos
*  Backup for Nacional 
	* What TAPE is (FIDU)
	* SUFI (FSS on LTO), what the tape media
	* Additional Storage?
	* Networking in place?
	* Mimix Configuration on Friday - When is the Maintenance Windows
* This week we will request the additional storage for Sufi PRO
	* Customer expectative is to travel next Monday with LTO tapes. (SUFI and FIDU backup, on LTO tapes)
	* The sync to VTL
* Send the invite early.
* 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
