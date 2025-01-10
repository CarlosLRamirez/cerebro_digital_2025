---
type:
  - minuta
IDProyecto:
  - "10933"
modified: '"2025-01-10 14:18", "5tc/G1T+6"'
created: '"2024-07-11 07:07", "4tc/G7T+6"'
---
#minuta 
#id10933 


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

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Portafolio
	* Pendiente entregable de Edgar Lange (DMS), sobre como quedarian las base de datos
	* Pendiente: Sesión de Preguntas y Respuestas con Luis Higuera
	* Cadencia interna - eliminarla
	* Cadencia con cliente, volver a ponerla.
* Migración de aplicaciones*
	* [x] Necesitamos hacer push con el front-end  de MDF #risk #followup
	* [x] Historias de Usuario: necesitamos involucrar a los funcionales #followup
* Liz pidió una linea de tiempo de lo que falta, lo que hemos hecho, los desafios. #followup 
* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`