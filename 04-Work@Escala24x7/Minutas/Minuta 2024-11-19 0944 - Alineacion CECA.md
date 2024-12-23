---
type: Minuta
IDProyecto: INT-CECA
date: 2024-11-19
modified: '"2024-12-13 12:06", "5tc/G12T+6"'
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
2024-11-19

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* [ ] Debemos enviar todos los meses la horas a finanzas, Novys tiene un formato #followup   ⏫ 
* [x] Revisar presentaciones de EMX de este mes #emx 📅 2024-11-19

[[2024-11-19 Dashbord de Quicksight de Escala|2024-11-19 Dashbord de Quicksight de Escala]]



## Temas Discutidos
*  

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
