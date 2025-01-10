---
type:
  - minuta
IDProyecto: "11105"
date: 2024-07-16
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
2024-07-16

## Asistentes

### Cliente
* Erick Giancarlo Ruiz Lopez
* Brenda Catalina Reyes

### Escala24x7
- Carlos Leonel Ramírez
-  Nancy Vargas
- Josh Patterson
- Roy Flowers

## Agenda
* 
## Temas Discutidos
*  ![[Pasted image 20240716094145.png]]

![[Pasted image 20240716095155.png]]

![[Pasted image 20240716095325.png]]

![[Pasted image 20240716095406.png]]


## Puntos de Acción acordados
*  

## Proxima Reunión
*   


`