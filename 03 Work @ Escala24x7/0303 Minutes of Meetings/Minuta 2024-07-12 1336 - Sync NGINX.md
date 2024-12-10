---
type: Minuta
IDProyecto: "11100"
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
* Sandra Ojeda
- Fernando Guerrero
- Edwin Perilla
- Edisson Vivas
### Escala24x7
- Carlos Leonel Ramírez
- Alberto Madrid
## Agenda
* Sesión se seguimiento de proyecto
## Temas Discutidos
*  Aún persiste un issue con SuperApp, y no se descarta que tenga relación con el cambio de los NGINX
* Aún no esta el GO para apagar la infraestructura anterior.
* Se espera que hoy se tenga una definición. 

## Puntos de Acción acordados
* [x] A pagar  la infraestructura proximo martes 16, mas no destruirla 📅 2024-07-15  #followup

## Proxima Reunión
*   

`