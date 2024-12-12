---
type: Minuta
IDProyecto: "10854"
date: 2024-07-31
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
2024-07-31

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Mañana se tiene una sesión con AWS
	* Karla quiere auditar como vamos con CEMPRO
	* Presentamos el status report
	* Escalamiento
	* Sesiones coordinadas
	* Status General
	* Bloqueantes, etc.. 
	* Un par de slide.
* Empezar a meter a Alejandra
* Status de los proyectos
	* muy gráfico, como un timeline
	* cuando inicio, cuando esperamos que termine, siguientes pasos, etc..
	* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
Template: [[Minuta 2024-12-12 0935 - Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
