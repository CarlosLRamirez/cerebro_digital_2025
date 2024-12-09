---
type: Minuta
IDProyecto: "11152"
date: 2024-09-04
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
2024-09-04

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  ![[../attachments/Pasted image 20240904103649.png]]



![[../attachments/Pasted image 20240904103656.png]]

![[../attachments/Pasted image 20240904103741.png]]


![[../attachments/Pasted image 20240904103758.png]]


![[../attachments/Pasted image 20240904103813.png]]

![[../attachments/Pasted image 20240904103851.png]]

![[../attachments/Pasted image 20240904103915.png]]





![[../attachments/Pasted image 20240904104325.png]]
- Debemos preguntar si podemos tener una Linux VM? Jason Waller debe confirmar.
- ![[../attachments/Pasted image 20240904104523.png]]
- 10.11.0.0/29 y 10.11.0.8/29 se quedarian en la conexión final
- ![[../attachments/Pasted image 20240904104843.png]]

169.254.0.204/31 
169.254.0.206/31



## Puntos de Acción acordados

- 

## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
