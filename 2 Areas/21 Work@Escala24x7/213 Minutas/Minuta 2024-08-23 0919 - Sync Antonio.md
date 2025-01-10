---
type:
  - minuta
IDProyecto: "11152"
date: 2024-08-23
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
2024-08-23

## Asistentes

### Cliente
* 
### Escala24x7

- Este fin de semana ellos tienen un espacio para trabajar en el DR, podemos aprovechar
- Podemos hacer este SAVSYS este fin de semana? sin tener instalado Mimox,
- Luego instalamos Mimix para replicar unamiente librerias de aplicacion de Fiduaciones
- 

## Agenda
* 
## Temas Discutidos
*  Como en nacional solo vamos a guardar la POC

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
