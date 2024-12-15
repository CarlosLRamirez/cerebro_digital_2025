---
type: Minuta
IDProyecto: "11152"
date: 2024-07-24
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
2024-07-24

## Asistentes

### Cliente
* Andres Camilo Carmona Lopez
* Carlos Gustavo Verbel
* Tatiana Sanchez Londoño
* Didier Gionany Cairasco
* Pastor Fernando de Los Rios
* Martha Isabel Mayo
* Sergio Quintero Angel
* Andres Felipe Ramírez
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  El salvado se obtendra de la máquina de DR, el riesgo es que durante este tiempo no se tendría sincronización por Mimix.
	* Andres debe validarlo con el equipo de SUFI
* Ventana viable, domingo antes de las 8AM, podemos pensar en domingo 3 de agosto.
* [x] Consultar a Connectria sobre el salvado con la opción 21 con Mimix #followup

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
