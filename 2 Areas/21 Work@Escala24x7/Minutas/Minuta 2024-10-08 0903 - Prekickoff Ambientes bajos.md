---
type: Minuta
IDProyecto: "11206"
date: 2024-10-08
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
2024-10-08

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
- Frankin Garcia
- Ivan Gil
- Oscer Eduardo Gonzalez


## Agenda
* 
## Temas Discutidos
*  

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[20241231T0801 2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
