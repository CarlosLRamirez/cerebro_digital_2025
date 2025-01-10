---
type:
  - minuta
IDProyecto: "11065"
date: 2024-09-03
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
2024-09-03

## Asistentes

### Cliente
* Miguel Chaparro
* Lina Mantilla
### Escala24x7
- Carlos Leonel Ramírez
- Nelson Mora
- Mario Cruz
- Eva Castaneyra
- Iliana Estupinian

## Agenda
* 
## Temas Discutidos
*  Pruebas de SuperApp
	* Ya levantaron data con URLs, pero no han hecho con MBaSS
	* Estan ambientando la data para que la SuperApp redireccione
* Lina menciona un tema de rechazo cuando no detecta imágenes
	* No lo entiende.. hay que validar la lógica con Nelson
	* Nelson va revisar el código para revisar ese caso
* Estamos esperando el GO para desplegar Laboratorio
	* Ya Mario empezó ha hacer ajustes.. solo esperando el GO
* 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
