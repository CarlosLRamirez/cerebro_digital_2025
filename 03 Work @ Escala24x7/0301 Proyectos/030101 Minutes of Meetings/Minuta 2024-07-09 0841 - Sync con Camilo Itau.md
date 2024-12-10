---
type: Minuta
IDProyecto: "11105"
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
* Camilo
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Ya se cerró el caso 1, hoy deberia estar cerrado el caso 3
* Hay un tema de la RAM con San Jose
	* la RAM a 512
* La data que esta en SJ es del 22 de junio, el banco no ha dicho esxplisitamente si necesitan la data de un día X
	* Podriamos darlos por extiso?
	* Necesitame que ellso digan que fecha que digan que presentemos data.
	* Un failover simulado
	* Necesitamos cerrar HOY ese caso, si o si..
* Mimix
	* nos piden 3 semanas haciendo pruebas
	* Necesitamos ver el plan
	* Necesitamso hacerle seguimento en los dailys, incluir a Camilo
	* Tenemos que cerrar este negocio en mediados de Agosto.
	* Primeras migraciones en Septiembre
	* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`