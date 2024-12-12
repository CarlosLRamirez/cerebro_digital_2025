---
type: Minuta
IDProyecto: "11152"
date: 2024-10-07
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
2024-10-07

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


![[attachments/Pasted image 20241007113739.png]]

replication throttle set override destination CONNS630_974178.connectria.dc11a.connpriv.com 1Mbps


o control throttle on source: 


replication throttle set override destination CONNS630_974178.connectria.dc11a.connpriv.com 1Mbps

to start:  replication initialize rctx://19


replication add source mtree://dd9900m.bancolombia.com.co/data/col1/CNTRNAL destination mtree://CONNS630_974178.connectria.dc11a.connpriv.com/data/col1/CNTRNAL_mirror

  

replication initialize mtree://CONNS630_974178.connectria.dc11a.connpriv.com/data/col1/CNTRNAL_mirror

===

Both source and target DDs:

replication add source mtree://dd9900m.bancolombia.com.co/data/col1/CNTRNAL destination mtree://CONNS630_974178.connectria.dc11a.connpriv.com/data/col1/CNTRNAL_mirror

  

Source only:

replication throttle set override destination CONNS630_974178.connectria.dc11a.connpriv.com 100Mbps

replication initialize mtree://CONNS630_974178.connectria.dc11a.connpriv.com/data/col1/CNTRNAL_mirror

  or

"replication show config" and get the ctx number on the source. and "repl initialize rctx://<your number>"





replication throttle set override destination CONNS630_974178.connectria.dc11a.connpriv.com 100Mbps


====

John Kim


![[attachments/Pasted image 20241007130538.png]]

![[attachments/Pasted image 20241007130544.png]]



## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta 2024-12-12 0935 - Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
