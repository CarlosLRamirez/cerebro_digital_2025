---
type:
  - Minuta
IDProyecto: "11206"
date: 2024-10-15
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
2024-10-15

## Asistentes

### Cliente
* Sandra Milena Ojeda
* Edwin Perilla Fino
* Edisson Vivas
### Escala24x7
- Carlos Leonel Ramírez
-  Jenny Rodriguez
- Ivan Gil
- Oscar Eduardo Gonzalez

## Agenda
* 
## Temas Discutidos
*  Se mantendrá CCM por un tiempo
* Se deben mantener ambos componentes desplegados
* Microservicios embebida configuración de Redis
* 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
