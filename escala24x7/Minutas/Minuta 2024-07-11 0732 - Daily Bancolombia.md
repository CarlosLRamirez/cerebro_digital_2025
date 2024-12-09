---
type: Minuta
IDProyecto: "11152"
date: 2024-07-11
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
2024-07-11

## Asistentes

### Escala24x7
- Carlos Leonel Ramírez
- Antonio Florez
- Cesar Perez

## Agenda
* 
## Temas Discutidos
*  Modelo Operativo
	* Se debe abordar con el banco
	* Camilo dice que debe ir mas allá de los Runbooks
* Correo de Antonio a Maria Elsy
	* Ellos tienen que pagar los 105mil de implementación
	* Suma del MRR (incremento)
	* Lo va enviar hoy. (el incremento del storage) - 100GB de Storage
	* Cores, dependiendo del consumo de recursos de Mimix, podemos requerir 2 o 3 Cores
	* Hoy es 6 cores y 300 GB en Mb y 300TB en Memoria
* Alternativa de ASP2, esta por definir
* ASP32 ??
	* Es un arreglo de discos, es como si fuera un filesystem.
* En agosto se pueda re-activar Leasing
* Reunión con Connectria, hoy
	* Se va necesitar el storage, no lo han dicho oficialmente
	* El challenge mas grande es que se defina ya si ellos van a necesitar comprar ese Storage?
* Estimación: sacar el backup el 28/jul
* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`