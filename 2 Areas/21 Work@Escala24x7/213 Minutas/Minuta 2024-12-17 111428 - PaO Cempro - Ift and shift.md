---
created: 2024-12-17T11:14:28
modified: '"2025-01-07 10:23", "2tc/G1T+6"'
date: 2024-12-17
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "10854"
---

#minuta 
#id10854

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
- [x] Assessment de seguridad de estos 39 servidores migrados #closed #id10854 ✅ 2025-01-10
	- Esto se completo
- [x] Sesión de FinOps para ver optimizaciones de los servidores (Saving plan) #closed #id10854 ✅ 2025-01-10
	- Quedaron unos servidores duplicados, apagados 
	- Se informó a Carolina Madera el 17/Diciembre
- [x] Agentes de CloudWatch y System Manager, seguimento con el cliente #closed #id10854 ✅ 2025-01-10
	- Se puede priorizar los top servers
	- Ya se cerro el tema con Jhonatan Muñoz