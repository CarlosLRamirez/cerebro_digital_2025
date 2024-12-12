---
type: Minuta
IDProyecto: 
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
*  App Ruteo
	* Se identificó el problema de porque no cargaba el Mapa, el tema estaba relacionada con EFS.
	* Todavía esta el tema de la cámara que no abre con Brando. Ya estan identificados.
* Consumo NAS 
	* Hay una sesión para mañana a las 3pm, donde vamos a ver lo del CI/CD, para ver si contenerización de los Wordpress (esto es para todas las de Wordpress)
* Marcajes 
	* Seguimos haciendo unas pruebas, el viernes esperamos tener una sesión.
* Apoyo Wordpress
	* Carlos Mendez dice que cree que no va ser necesaria
	* Alejandro: dice que sigamos caminando con el apoyo, que el tambien esta pensando como un outsourcing.
* Modernizacion de Storage
	* Hay un tema de redes.. no tenian visiblidad completa de un AD, no habia un retorno. se esta gestionando, de lado de Cempro ya desplegaron. 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta 2024-12-12 0935 - Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
