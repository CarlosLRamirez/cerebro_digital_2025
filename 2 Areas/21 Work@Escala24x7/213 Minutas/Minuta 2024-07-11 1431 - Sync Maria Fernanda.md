---
type:
  - minuta
IDProyecto: "10652"
date: 2024-07-11
---
``

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
2024-07-11

## Asistentes

### Escala24x7
- Carlos Leonel Ramírez
- Maria Fernanda Juárez
- Jenny Rodriguez

## Puntos discutidos

- Mafer la otra semana se reúne con Sandra
- Quiere enfocar el reporte de las horas en dos puntos
	- [x] Actualizar el documento a las horas actuales #id10652  📅 2024-07-11
		- Pidió que quitara unas cosas - 8 horas en no se que vaina
		- Quitar las cosas que no puedan ser justificables
	- [x] Cuantas horas más necesitamos para el DR #followup


