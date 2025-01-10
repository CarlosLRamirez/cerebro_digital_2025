---
type:
  - minuta
IDProyecto:
  - "10854"
date: 2024-10-01
modified: '"2025-01-10 13:13", "5tc/G1T+6"'
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
2024-10-01

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
- [x] existe un tag que se tiene que corregir Jonathan (tab de base de datos) #followup
- [x] Se va correr una herramienta para validar los tags a partir del 1 de julio de 2023 #followup

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
