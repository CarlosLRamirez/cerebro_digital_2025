---
type:
  - minuta
IDProyecto: "11105"
date: 2024-07-17
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
2024-07-17

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
* Emiro dice que no esta de acuerdo en algunos temas, lo va escalar con Francisco
* Emiro ya están trabajando en la configuración del cierre que van a enviar desde Colombia
	* Quieren hacer un cierre sin Mimix, para validar el cierre y porque la maquina tiene menos recursos. Eso el Viernes.
	* 🚩 Necesitan bajar Mimix, necesitamos consultarle a Soon. que nos envíe el instructivo para bajar Mimix 🚩
	* No se ha identificado la necesidad de modificar ningún LV
	* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`