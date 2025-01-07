---
type:
  - Minuta
IDProyecto: "11152"
date: 2024-11-07
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
2024-11-07

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  On-premise a RDS (AWS) . para PROD
	* 2 millones: 8min 49sseg
	* 1 mill 300: 5min 30 seg
	* 6 millones:  12min
* On-premise a DB2 (Connectria) para QA
	* 1millones 700: 14min
	* 15 millones: 1h 35min

ping desde la IP .90 (LZ on-premise) hacia Connectria (SDWAN):
![[../attachments/Pasted image 20241107094604.png]]

traceroute desde la ip (.90)(LZ on prem) hacia Connectria
![[../attachments/Pasted image 20241107094756.png]]

ping desde la 10.8.112.23 (LZ-onprem) hacia AWS:




## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[20241231T0801 2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
