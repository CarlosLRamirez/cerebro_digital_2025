---
created: 2024-12-18T07:06:57
modified: '"2025-01-07 10:24", "2tc/G1T+6"'
date: 2024-12-18
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "11236"
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
2024-12-18

## Asistentes

### Cliente
* David Romero
* Vanesa Hernandez
### Escala24x7
- Carlos Leonel Ramírez
- Jenny Rodriguez
- Johan Blanco

## Agenda
* 
## Temas Discutidos
* La conexión con Colombia en PROD es por DX, pero en otros ambientes es por VPN
* Conexión directa entre nubes por tema de latencias (DataPower)
* DX de CAM???? (tanto para Virgnia como Ohio)
* Tenemos VPN contra los 4 paises

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
