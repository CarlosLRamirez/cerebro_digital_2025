---
type: Minuta
IDProyecto: "11152"
date: 2024-08-26
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
2024-08-26

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
- [x] Reglas bi-direccionales en el FW (excepción) #followup
*  Tatiana pide que entregamos alguna documentación donde indique que los puertos se necesitan de forma bi-direccional
* La forma que lo hacen es que ellos habilitan una sola dirección, y si observan un bloqueo, entonces tienen evidencia que se necesita bi-direccional, y en ese caso es que hacen una excepción
- Las ventanas para hacer cambios en los Firewalls a la 1pm-2pm, 5pm-6pm, y 10-11 pm.
- 10.9.2.150 o 10.10.229.150 - Confirmar si esa es la IP con la que sincronizara hacia Connectria.
- Permisos actuales en Connectria

![[../attachments/Pasted image 20240826102249.png]]
## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
