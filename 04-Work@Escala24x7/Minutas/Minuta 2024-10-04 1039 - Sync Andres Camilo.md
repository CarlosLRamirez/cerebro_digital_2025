---
type: Minuta
IDProyecto: "11152"
date: 2024-10-04
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
2024-10-04

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Ya hay conexión entre AWS y el Servidor en Connectria
* Cuando estuvieron subiendo el aplicativo, los sockets sufrieron una calda, en una segunda prueba no paso, y funciono
* En desarrollo sigue pasando, si certificación esta bien, luego lo podemos revisar
* Lo que ven, es que en tierra eso hace una actualización de unos archivos, en tierra se demora 3 minutos, en Connectria se demora 6 minutas.
	* Ellos lanzan un servicio en AWS, y el manda una petición al iSeries, esas reglas están dentro del iSeries, el iSeries le manda la respusta en AWS, y empieza a actualizar las reglas.
* Andres bajo todos los servicios en ambos (iSeries y AWS) y volver a lanzarlos.
* Andres esta ensayando en QA.
* 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
