---
type:
  - minuta
IDProyecto: "11152"
date: 2024-10-28
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
2024-10-28

## Asistentes

### Cliente
* Jhon Serna
* Monica Maria  Martinez
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* Revision de Runbooks para SUFIPRO y SUFIDDS
## Temas Discutidos
*  Jhon Serna indica que debemos involucrar a quienes toman esa decision, dice que el toma la información solo como informativa: Umbrales de monitoreo.
* Las politicas de PRI las debemos ver con Erwin Hidalgo
* Podemos tener un listado de todos los backups que se hacen en SUFIDDS y SUFIQA
* 
## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
