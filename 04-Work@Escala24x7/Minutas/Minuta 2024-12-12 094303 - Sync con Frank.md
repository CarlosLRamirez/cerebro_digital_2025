---
created: 2024-12-12T09:43:03
modified: '"2024-12-12 09:47", "4tc/G12T+6"'
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "11236"
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
2024-12-12

## Asistentes
### Escala24x7
- Carlos Leonel Ramírez
-  Frank Caicedo

Sync con Frank Caicedo
- Prekickoff interno con Mobile Computing:
	- Al dia de hoy no hay ningun SOW firmado, ni MSA ni NDA, el SoW es lo mas importante ⚠
	- Aún no tienen el equipo armado completo: el Lunes pasado fue que asignaron al PM (el dia del Prekicoff - Sergio Bonano)
	- En el prekickoff dijeron que aún no tienen el equipo de desarrollo.. el acuerdo es ir haciendo las tareas que no dependan de desarrollo  - Esto no se le ha dicho al cliente
	- Se le envió un plan a MC, para crear un Roadmap, con hitos y fechas.
		- Tener equipo de desarrollo
		- etc...
	- Ese riesgo lo asume Maria Fernanda y Mobile Computing - no tener el equipo completo - Frank le pidio a MC el plan de mitigación.
	- Tambien hay un cambio de compañia: este es otro riesgo.
	- El canal de Slack todavia no esta creado.
	- Nicolas es el PM de Davivienda


Pendiente de definir:
	- Estrategia de comunicacion:
		- Sync Semanal - bi-semanal ???
		- Sync interno con MC
	- Elaborar plan de trabajo
	- Herramiente comunicacion directa
	- Matriz RACI entre Escala y Mobile

![[Pasted image 20241212094609.png]]


![[Pasted image 20241212091508.png]]


*   

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
