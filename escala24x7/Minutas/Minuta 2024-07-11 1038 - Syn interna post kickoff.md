---
type: Minuta
IDProyecto: "11152"
date: 2024-07-11
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
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Camilo Villamil
- Antonio Florez

## Agenda
* 
## Temas Discutidos
*  Salir con Nacional con todo
* Migrar Sufi primero.
* Modelo Operativo
* Networking?
	* Definiciones de Networking
* [x] Requerimiento Boveda de datos en Connectria #followup  #pre-proyecto

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`