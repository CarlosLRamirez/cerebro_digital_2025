---
type: Minuta
IDProyecto: EMX-Grupo Ramos
date: 2024-09-18
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
2024-09-18

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
- [x] Agendar una sesion para presentación de Orbis - Jhon Asuaje #followup
- [x] Arquitectura de los recursos actuales en AWS - Junior Vega #followup
- [x] Validar si tienen Control Tower - Junior Vega #followup
- [x] Validar politica de Tag - Kevin Molina #followup
- [x] Pendiente ejecutar Assessment de Seguridad - Jhon Asuaje #followup
- [x] Assesment de Skills (Conocimientos) - Luis Palacios #followup
	- Pedro Rivera ya tiene un resultado del analisis de conocimiento en AWS
## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
