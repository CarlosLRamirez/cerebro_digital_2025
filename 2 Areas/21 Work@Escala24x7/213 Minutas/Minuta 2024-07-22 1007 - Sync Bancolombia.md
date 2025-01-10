---
type:
  - minuta
IDProyecto: "11152"
date: 2024-07-22
modified: '"2025-01-07 13:47", "2tc/G1T+6"'
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
2024-07-22

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Sincronización de 300GB diarios
	* IDR
* Proyecto grande para Bancolombia, proyectos dentro del proyecto
	* Fiduciaria (BigBang)
	* Sufi
	* Crecimientos... (no existe formalizao entre las partes)
		* Replicación
		* Licencias
* Modelo Operativo 

- Jason
	- Networking
		- Replication VPN Tunnel
		- 





## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
