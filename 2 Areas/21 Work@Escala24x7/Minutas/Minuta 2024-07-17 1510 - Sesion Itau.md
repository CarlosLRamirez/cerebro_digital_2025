---
type: Minuta
IDProyecto: "11105"
date: 2024-07-17
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
2024-07-17

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  El tema Mimix reverso no se va hacer
* Se va hacer el viernes la actualización de datos y el lunes hacen el cierre
* Necesitamos el instructivo de Soon para bajar los servicios de Mimix, y para subirlos.
	* El viernes van a detener Mimix.
* La hora para inicio de Cierre:  8AM para revisar, y si todo ok 9AM o 10AM enviar el cierre, antes de eso que Soon entré y valide que todo se ve.
* Ya no se haría un cambio de roles el martes.
* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`