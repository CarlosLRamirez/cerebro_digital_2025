---
type:
  - minuta
IDProyecto:
  - "10854"
date: 2024-09-23
modified: '"2025-01-10 13:12", "5tc/G1T+6"'
created: '"2024-12-16 08:13", "1tc/G12T+6"'
---
#minuta 
#id10854
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
2024-09-23

## Asistentes

### Cliente
* Carlos Mendez
* Eduardo Catalán
* Ernesto Herrera
* Oseas Gonzalez
* Pedro Gabriel
* Rudy C
* Wilfred Alvarez
### Escala24x7
- Carlos Leonel Ramírez
- Jose Abzum
-  Rafael Rojas

## Agenda
* Mesa bi-semanal para trabajar en puntos de acción en la Modernización de 3 aplicaciones piloto
## Temas Discutidos
*  

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
