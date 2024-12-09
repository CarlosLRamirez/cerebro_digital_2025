---
type: Minuta
IDProyecto: "11152"
date: 2024-08-08
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
2024-08-08

## Asistentes

### Cliente
* Antonio Florez
* Pedro Navarro
* Walter Duque
* Pastor de los Rios
* Jonathan Alvarez
* Maria Elsy Giraldof
* Jhon Serna
* Erwin Hidalgo Cardenas
### Escala24x7
- Carlos Leonel Ramírez
-  Josh Patterson
## Agenda
* 
## Temas Discutidos
*  They are discussing the maintenance windows time we will require they are talking about he first option (restrict state and save while active)
* Walter is asking why we're not starting with non-productive environments
* Antonio is saying the plan is to send the tapes from the 3 machines at the same time
* Walter is proposing to make the backup of non-prod before, due will be more easy to get the approval
* Aug/11 it's already scheduled an IPL on SUFI PROD
* Walter is proposing this weekend for non-prod environments (QA and DS) and Aug/17 take backup on SUFI PROD
* Walter is asking why not to sent the non-prod tapes first,  not to wait for all the tapes
* Maria Elsy is saying we should  deploy non-prod first in Connectria
* Erwin is saying that developers should have connectivity to Connectria, so they can merge information to Connectria they mention somethin about RTC that I don't understood
* Antonio propose send missing libraries through FTP they are defining dates:
	* SUFI QA and DDS: Saturday Aug/10th after 6pm,  pickup tapes on Sunday Aug/11th
* The media will be 3592

== Post meeting ==
- Las cintas se irian a St. Louis
- El viaje lo paga escala y luego lo factura a Bancolombia
- 
## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
