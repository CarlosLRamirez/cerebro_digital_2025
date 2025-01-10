---
type:
  - minuta
IDProyecto: "11152"
date: 2024-07-11
modified: '"2025-01-09 15:17", "4tc/G1T+6"'
created: '"2024-07-11 09:32", "4tc/G7T+6"'
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
2024-07-11

## Asistentes

### Cliente
* Vance Hollingsworth - IBM engineers
* Mike Becker - IBM engineers
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
- Tuneles VPN
- Expectative to have the backups July 28th (option 21)
	- Generate the tapes 

![[Pasted image 20240711093224.png]]
## Puntos de Acción acordados
*  

## Proxima Reunión

![[Pasted image 20240711093535.png]]

`