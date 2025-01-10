---
type:
  - minuta
IDProyecto: "11152"
date: 2024-08-20
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
2024-08-20

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Antonio habló con Pastor, y tienen una LTO que ya no esta conectada con Leasing
* Van a validar si ese HW se puede usar
* Alternativas: Sacar el backup en la VTL y luego pasarlo al formato en LTO
* Vamos a buscar una reunion con Kindryl y Connectria
	* Para conectar las VTL, para ver que necesitan cada uno.
	* Pastor nos dira la disponbildiad de Kindryl

## Puntos de Acción acordados


## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
