---
type:
  - minuta
IDProyecto: "11152"
date: 2024-08-21
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
2024-08-21

## Asistentes

### Cliente
* Andres Felipe Ramirez
* Diego Fernando Angarita
* Jhan Gaviria
* John Carmona
* Oscar Morales
* Jossie Piza
* Leon Rojas
* Juan Suarez
* Tatiana Sanchez
### Escala24x7
- Carlos Leonel Ramírez
-  Jason Weller

## Agenda
* 
## Temas Discutidos
*  Interfqaces independientes
	* Crecer las interafaces
	* vn0/5 
	* vn0/6 
- 1:30pm a 2pm
	 - 

![[Pasted image 20240821082324.png]]

- 



## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
