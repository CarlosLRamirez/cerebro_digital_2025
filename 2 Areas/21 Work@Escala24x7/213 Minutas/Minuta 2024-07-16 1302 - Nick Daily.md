---
type:
  - minuta
IDProyecto: "11105"
date: 2024-07-16
modified: '"2025-01-09 15:07", "4tc/G1T+6"'
created: '"2024-07-16 13:02", "2tc/G7T+6"'
---

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
2024-07-16

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  AWS connectivity to LPAR
	* Confirm communication (FW rules on Connectria)
	* Pendiente prueba desde AWS hacia el LPAR a Connectria
* The test says is that the test should be done on business hours
	* Muy poca anticipación
	* Connectria no garantiza que se este disponible después de las 5
* DR test back to Colombia
	* This need preparation
	* DR test is not included in the scope.
	* We need to satisfy the requirements from the SoW
* Muy poca anticipación, minimo 2 semanas de antipicación
* Que hable con Camilo, y le diga lo de la prueba de regreso. #actionpoint
* Que lo pongan por escrito, aquí y en Colombia #actionpoint
* Necesitamos permisos que lo incluyan en lo scope, y necesitamos mas de tres días. #followup 
* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`