---
type: Minuta
IDProyecto: "11152"
date: 2024-09-19
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
2024-09-19

## Asistentes

### Cliente
* Camilo Chica Vargas
* John Fernando Carmona Cardona
* Juan Camilo Piedrahita Londono
* Didier Giovanni Cairasco Silva
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  La IP y nombre de la maquina de Nacional va cambiar
* Camilo Chica, pregunta si puede haber algo en el medio para decirle a Confianza que vaya a Connectria en lugar de Niquia
* Empezar  a cambiar las aplicaciones???
	* Empezar a recolectar esa información

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[20241231T0801 2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
