---
type:
  - minuta
IDProyecto: "11152"
date: 2024-08-05
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
2024-08-05

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos

![[Pasted image 20240805131008.png]]

- Connectria debe ver la IP de administración
DR (Calle 100)
![[Pasted image 20240805131135.png]]

- IPs del DR
	- Connectria recomienda que sean IPs diferentes
	- Andres Felipe: Por DNS no, porque los DNS no reflejan inmediatamente, demoran hasta 72horas, Tatiana dice que eso es cierto en Internet, pero DNS local no toma tanto tiempo.
- Despliegue de FWs y Configuracion de Axity
	- se toman 5 dias según Tatiana una vez se tenga la aprobación económica
	- 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
