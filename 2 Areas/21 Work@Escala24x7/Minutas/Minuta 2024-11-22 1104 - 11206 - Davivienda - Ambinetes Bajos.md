---
type: Minuta
IDProyecto: "11206"
date: 2024-11-22
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
2024-11-22

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  

## Puntos de Acción acordados
- Enviar listado actualizado de recursos desplegados en CR
- Enviar propuesta para reuniones de networking
	- Lunes 25 - 10AM - 11AM
	- Lunes 25 - 11AM - 12AM 
	- Martes 26 - 10:30AM - 11:30AM (cubre nuestra sesión de seguimiento)
	- Martes 26 - 2PM - 3PM
	- Miercoles 27 - 10AM - 11AM
	-  Jueves 28 - 9AM - 10AM
	- Jueves 28 - 10AM - 11AM
	- Jueves 28 - 2PM - 3PM
	- Viernes 29 - 10:30AM - 11:30AM (cubre nuestra sesión de seguimiento)
	- Viernes 29 - 11AM - 12PM
	- Viernes 29 - 3PM - 4PM
## Proxima Reunión
*   

---
Template: [[20241231T0801 2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
