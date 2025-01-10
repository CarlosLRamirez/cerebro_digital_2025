---
type:
  - minuta
IDProyecto:
  - "10933"
modified: '"2025-01-10 14:19", "5tc/G1T+6"'
created: '"2024-12-16 08:13", "1tc/G12T+6"'
---
#minuta 
#id10933 


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
2024-07-30

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Jean Paul informa que la EVC no tiene recursos, ya que tienen demasiadas tareas, probablemente no nos darán esos dos recursos.
	* Arquitecto: se esta evaluando la opción de integrar a otro arquitecto, pero Abner debe contextualizarlo a este nuevo arquitecto.
	*  
## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
