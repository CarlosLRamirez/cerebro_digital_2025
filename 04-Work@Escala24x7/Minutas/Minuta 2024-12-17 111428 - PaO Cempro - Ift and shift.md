---
created: 2024-12-17T11:14:28
modified: '"2024-12-17 11:24", "2tc/G12T+6"'
date: 2024-12-17
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "10854"
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
2024-12-17

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
- Jonathan Muñoz
- Rafael Rojas
- Alvaro Hernandez

## Agenda
* 
## Temas Discutidos
- [ ] Assessment de seguridad de estos 39 servidores migrados #followup #id10854
- [ ] Sesión de FinOps para ver optimizaciones de los servidores (Saving plan) #followup #id10854 
	- Quedaron unos servidores duplicados, apagados 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
