---
type:
  - minuta
IDProyecto:
  - "10933"
modified: '"2025-01-10 14:18", "5tc/G1T+6"'
created: '"2024-07-09 08:07", "2tc/G7T+6"'
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
2024-07-09

## Asistentes

### Cliente
* Alberth
* Carlos Avila
* Manuel Hernandez
* Hilberth Perucho
* Ronaldo Lopez
### Escala24x7
- Carlos Leonel Ramírez
-  Ruth
- Anderson

## Agenda
* 
## Temas Discutidos
- Generación de Pólizas
	* [x] Se necesita involucrar a algún funcional (Wilson Ottoniel o los encargados de facturar masivamente), * Necesitamos buscar un espacio con esta persona, Manuel esta coordinando esta sesión  #followup
	* Según Manuel, debería funcionar de la misma manera que se hace hoy en día, es una modernización, pero no debe haber una evolucion de la funcionalidad.
	
* Ya nos enviaron la plantilla de SendGrid
	* Segun Alberth ellos nos deben dar los parámetros

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`