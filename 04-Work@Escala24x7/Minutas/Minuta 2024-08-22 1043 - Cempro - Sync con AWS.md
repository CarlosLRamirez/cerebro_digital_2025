---
type: Minuta
IDProyecto: "10854"
date: 2024-08-22
---

> ESTA LLAMADA NO ES DE PROYECTO - ES DE PREVENTA

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
-  

## Agenda
* 
## Temas Discutidos
*  
![[../attachments/Pasted image 20240822105757.png]]

Puntos fundamentales: 
	1, 2, 4, 5 los otros son un nice to have
	
## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta 2024-12-12 0935 - Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
