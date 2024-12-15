---
type:
  - Minuta
IDProyecto: "11152"
date: 2024-11-05
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
2024-11-05

## Asistentes

### Cliente
* Evelin Franco Caballero
* Oscar Mauricio Morales
* Joan Sebastian Uribe
* Pastor de los Rios
* Julian David Diossa Gallego
### Escala24x7
- Carlos Leonel Ramírez

## Agenda
* 
## Temas Discutidos
- ORIGEN  (On-premise)
	- 10.8.71.90  
	- 10.8.71.91  
	- 10.8.71.92  
	- 10.8.71.93
- Destino (Connectria)
	- 10.11.12.136 

- Necesitamos ver el MSS negociado dentro de la trama.
- 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
