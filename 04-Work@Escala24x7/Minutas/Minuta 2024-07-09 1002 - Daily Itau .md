---
type: Minuta
IDProyecto: "11105"
date: 2024-07-09
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
2024-07-09

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* Prioridad - Cierre Caso de Uso 3
* 
## Temas Discutidos
*  Mimix
	* Inconveniente que se presento: Connectria esta trabajando en algunos parámetros de configuración en el sistema Target.
	* Se propone crear un espacio mañana 9:30 Colombia, confirmar con Connectria.
	* Connectria necesita apoyo de Banco? Cuando esperan tenerlo resuelto?
* Caso No. 1
	* Se cierra con el correo
* Caso No. 3
	* La semana pasada les pidieron hacer un poco mas de efásis
	* El día 26 se entregó el ambiente DR mediante un correo, la ip es xxxxx
	* Hasta el momento está trabajando normal, 
	* Se hizo lo siguiente:
		* Subir el motor (logró subir)
		* El equipo de soporte de Phoenix brindo unas consultas básicas y se probaron y se tuvo coherencia de la data.
	* Itaú tiene unas consultas.
		* Fecha de despliegue de la máquina, como funciona la replica, como se presenta la data.
		* Quieren conocer la coherencia con las fechas, y como va ser el modelo a futuro.

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`