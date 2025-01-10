---
type:
  - minuta
IDProyecto: "11152"
date: 2024-07-12
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
2024-07-12

## Asistentes

### Cliente
* Astrid Jimenez
* Byron Martinez
* Carlos Verbel
* Daniel Ramirez
* Didier Giovanni Cairasco
* Erwin Hidalgo
* Luis Fernando Zamudio
* Maria Elsy Giraldo
* Pastor Fernando de los Rios
* Santiago Garcia Restrepo
* Walter Anibal Duque
### Escala24x7
- Carlos Leonel Ramírez
-  Antonio Flores
- Camilo Villamil

## Agenda
* Status Report Semanal del proyecto NEON, lidera Didier de Bancolombia
## Temas Discutidos
- PSeries ya no va para Connectria
- Leasing están refactorizando, pero tienen el GO para que vaya a tambien a Connectria - SI VA **
![[Pasted image 20240712083808.png]]

- Mesas de Trabajo Conectividad y Ciber.
![[Pasted image 20240712084202.png]]


![[Pasted image 20240712085149.png]]
## Puntos de Acción acordados
*  

## Proxima Reunión
*   
