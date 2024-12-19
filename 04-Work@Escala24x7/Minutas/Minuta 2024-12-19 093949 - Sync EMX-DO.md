---
created: 2024-12-19T09:39:49
modified: '"2024-12-19 10:53", "4tc/G12T+6"'
date: 2024-12-19
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - PMO
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
2024-12-19

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Ticket escalado de Grupo Ramos - Robert Santos

## Puntos de Acción acordados
- [ ] Robert Santos menciona que no tiene acceso a los tickets, sugiere la creación de un tablero o tener algún instrumento #followup #PMO 
	- 19/Dic: Se creo un [dashboard](https://escala24x7.atlassian.net/jira/dashboards/10237) preliminar y se compartió en el canal de EMX-RobertSantos 
- [ ] 
- [ ] 

## Proxima Reunión
*   

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
