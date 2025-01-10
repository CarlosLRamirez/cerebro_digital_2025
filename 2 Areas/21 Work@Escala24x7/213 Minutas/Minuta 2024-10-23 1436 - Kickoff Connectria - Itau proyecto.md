---
type:
  - minuta
IDProyecto: "11210"
date: 2024-10-23
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
2024-10-23

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
- Environments
	*  Production (AZ1)
	* HA (AZ2)
	* DR (San Jose, CA)
* MKSYSB and Tape for iIBM??
* Precisely
	* AIX Mimix
* 30 days after the project planning
	* a partir de que fecha?
	* Nick envisiona tener todo listo (networking) para AZ1
		* Then in AZ2
		* Then in DR
* 19 system before Christsmas!
	* What is the driver!?
* Sterling
	* Risk: la otra vez demoro mucho, garantizar
	* el BW


![[Pasted image 20241023143844.png]]

![[Pasted image 20241023143935.png]]

![[Pasted image 20241023150619.png]]


![[Pasted image 20241023153210.png]]

![[Pasted image 20241023153253.png]]

![[Pasted image 20241023153943.png]]


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
