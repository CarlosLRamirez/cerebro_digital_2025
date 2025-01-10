---
type:
  - minuta
date: 2024-11-05
modified: '"2025-01-08 12:03", "3tc/G1T+6"'
IDProyecto:
  - "11206"
---
#minuta 
#id11206

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
2024-11-05

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
* [ ] Backups, pendiente definir periodicidad #followup #id11206 
* [ ] Revisar temas de balanceo #followup #id11206
	- Con cleafy ya no es extrictamente necesario el NGINX
- [ ] Sesiones para socializar con los paises davivienda el SLA de DR #followup #id11221


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

