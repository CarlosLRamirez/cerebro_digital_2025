---
type:
  - minuta
IDProyecto: "11052"
date: 2024-09-10
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
2024-09-10

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Segmento publico a los Iseries
	* No se va natear, pero si se va presentar con un direccionamiento distito
	* Pero a Connectria se lo van a presentar en un direccionaniento distitno, van a natear las ips, 

![[Pasted image 20240910093612.png]]

- [x] Conexión para la administración dia a dia de Connectria #followup
	- Conexión con Zero Trust NA, No recibimos la confirmación -- entonces no se necesita??
	- Como van a acceder a Cyberark?
	- Kindryl maneja conexión por Cloudfare o tienen un canal dedicado?
	- Hay proveedores que tienen un canal dedicado
- [x] Puertos para monitoreo de los Iseries, son los mismos de ISeries? #followup
	- Necesitamos llenar el formato para los puertos para el monitoreo
	- Para el monitoreo Bancolombia va enmascarar las IPs de las Iseries
- [x] Nat del trafico de Connectria - Operaciones #followup

![[Pasted image 20240910095027.png]]



![[Pasted image 20240910095207.png]]


![[Pasted image 20240910095222.png]]


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
