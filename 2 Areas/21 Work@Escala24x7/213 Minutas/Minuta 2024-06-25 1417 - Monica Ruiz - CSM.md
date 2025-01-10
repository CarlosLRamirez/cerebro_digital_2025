---
type:
  - minuta
IDProyecto: "10859"
date: 2024-06-25
modified: '"2025-01-09 15:17", "4tc/G1T+6"'
created: '"2024-06-25 14:17", "2tc/G6T+6"'
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

![[Pasted image 20240625141838.png]]

![[Pasted image 20240625141802.png]]
## Puntos de Acción acordados
*  

## Proxima Reunión
*   


- Incidente RDS
	- AWS propone un WAR en dos pilares
	- 
`