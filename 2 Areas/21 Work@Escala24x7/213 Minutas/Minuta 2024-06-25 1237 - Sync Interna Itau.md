---
type:
  - minuta
IDProyecto: "11105"
date: 2024-06-25
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
2024-06-25
## Asistentes
### Escala24x7
- Carlos Leonel Ramírez
-  Cesar Gomez
- Cesar Perez
- Carlos Ramirez
## Agenda
* 
## Temas Discutidos
*  Dos reuniones
	* Una con Connectria:
		* incluir a Nancy
	* Reunion con el Banco
		* aclarar el sizing.
		* 

## Puntos de Acción acordados
*  Una reunion con Connectira
	* Senbilibzacion d ela situación acttual
	* Alineación tema del SoW
	* Necesitamos la maquina 2 ya
* Una reunión con el Banco
	* para entender porque necesitan 490GB
	* 

## Proxima Reunión
*   

`