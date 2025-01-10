---
type:
  - minuta
IDProyecto:
  - "11065"
date: 2024-11-12
modified: '"2025-01-10 14:43", "5tc/G1T+6"'
created: '"2024-12-16 08:13", "1tc/G12T+6"'
---


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
2024-11-12

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Todavía no esta desplegada el ambiente de integración, errores en el apply
	* Escala team revisara el error
	* El entorno de cargar datos, ese flujo ya lo podemos ir activando
	* Faltan los flujos de consultas de endpoints y exportaciones de datos.
* Ajustes a nivel de desarrollo - Nelson
	* 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
