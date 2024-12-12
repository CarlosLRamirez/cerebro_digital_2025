---
type: Minuta
IDProyecto: "11605"
date: 2024-10-10
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
2024-10-10

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Emóticos y caracteres especiales
	* Hoy hicieron pruebas y no fueron exitosas
	* Van a hacer una prueba en local
* Ajustes en el archivo de salida
	* Ya se hicieron ajustes
	* Esperando pruebas de costa rica
* Base de Campañas de El Salvador
	* No es consistente la notificación: Nelson
* Honduras
	* Pendientes que la filial vuelva a cargar la base de campañas
* Asuntos y Cuerpos del Correo
	* Nelson, esta pendiente que nos confirme
* Pipelines (Infraestructura)
	* El compromiso de la persona de banco es mañana
	* Lina le pidió prioridad, pero aún no tiene respuesta hoy
	* a mas tardar mañana




## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta 2024-12-12 0935 - Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
