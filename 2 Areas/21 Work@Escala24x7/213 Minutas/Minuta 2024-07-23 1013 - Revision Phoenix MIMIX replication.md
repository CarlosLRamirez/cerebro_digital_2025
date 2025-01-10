---
type:
  - minuta
IDProyecto: "11152"
date: 2024-07-23
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
2024-07-23

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Entregar la información a Soon
* preguntarle a Soon si hay que parar el script de la red
* Que Soon haga su análisis y recomendaciones.
* Necesitamos que Soon confirme si la replicación ya esta ok.
* Vamos a hacer un cambio de roles. (debe ser entre hoy y mañana), y Alvaro verificará que los datos estén integros.
* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
