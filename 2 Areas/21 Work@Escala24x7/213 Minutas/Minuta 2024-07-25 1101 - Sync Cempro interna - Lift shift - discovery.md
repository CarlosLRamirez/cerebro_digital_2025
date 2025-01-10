---
type:
  - minuta
IDProyecto:
  - "10854"
date: 2024-07-25
modified: '"2025-01-10 13:13", "5tc/G1T+6"'
created: '"2024-12-16 08:13", "1tc/G12T+6"'
---
#minuta 
#id10854
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
2024-07-25

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Jonathan tuvo una reunión con Williams
	* Ellos sacaron una hojita donde dicen que todos los servidores van por rehost, porque la mayoría son SAP y que la base de datos esta pegada al computo.
	* Aproximadamente 87 servidores
	* Ellos crearon 3 prioridades (los cuales serían OLA1 , OLA2, OLA3)
* El primer servidor todaviá no esta replicando
	* Alejandro pidió que solo mostremos el proceso pero todavía no esta replicando (bloquearon el puerto 1500)
* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
