---
type:
  - minuta
IDProyecto: "11152"
date: 2024-07-29
---


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
2024-07-29

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


I would need to download my tool (MIMIX_BLD).  This will allow me to perform journal and PTF analysis.  This tool will be used in the future to do configuration but initially is only used for the analysis portion.

- Necesitamos el detalle de los comandos que va correr.
- 


- This is a SAVFL, hay un FTP server, Dropbox, Sterling, 
	- 

- Evaula si se neceistan PTFs adicionales

- Si tiene unos PTF no muy viejos, debe hacer un journal analisys.


==Direct Connect==
- AWS Account ID
- Networks in AWS




## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
