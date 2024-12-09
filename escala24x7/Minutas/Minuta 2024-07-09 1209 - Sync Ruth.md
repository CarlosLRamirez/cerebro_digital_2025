---
type: Minuta
IDProyecto: "10933"
date: 2024-07-09
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
2024-07-09

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Desarrollo Lambdas
	* Según Ruth deberían terminar esta semana el desarrollo, pero el despliegue sigue teniendo complicaciones
	* El despliegue no va dar tiempo de terminar este sprint
	* La de poliza quizá quede pendiente por una definición de BAM
* Despliegues
	* Ah sido temas en conjunto, algunas han costado desplegar, hemos necesitado ayuda de BAM
	* En algunas cosas se han tardado
*  Ruth siente que Anderson esta algo lento
	* Y no esta equitativo, le esta llevando mas tiempo recomenzar la parte de Anderson.
	* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`