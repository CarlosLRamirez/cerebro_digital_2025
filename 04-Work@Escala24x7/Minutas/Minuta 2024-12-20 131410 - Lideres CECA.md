---
created: 2024-12-20T13:14:10
modified: '"2024-12-20 13:36", "5tc/G12T+6"'
date: 2024-12-20
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - PMO
  - CPSM-CECA
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
2024-12-20

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Asignaciones pendientes BAC Latam
	* Alex Campos 
	* Franklin envió un correo, esperando respuesta
	* Este cliente lo llevará el equipo de Franklin
	* Franklin debe pasar un cliente para Rafa
		* Según Franklin NIU y Cuscatlan no tienen dependencia a nivel administrativo y de equipos
	* Rafael  se queda con NIU y Tarjeta de Credito de Occiidente
* Asignación para DevOps de Davivienda
	* Necesitan hacer un ambio del de Seguridad a DevOps (al 100% o 75%)
		* por la creación de un 4to ambiente
		* Extension hasta febrero
		* Github Actions
		* 

## Puntos de Acción acordados
- [ ] Seguimiento pendientes SDL (Novys) #followup #pmo #cpsm-ceca

## Proxima Reunión
*   

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
