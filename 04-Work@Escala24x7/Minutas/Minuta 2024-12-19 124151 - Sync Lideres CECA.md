---
created: 2024-12-19T12:41:51
modified: '"2024-12-19 12:53", "4tc/G12T+6"'
date: 2024-12-19
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - PMO
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
2024-12-19

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos

* Tuvieron una reunion con arquitectura, Jenny muy abierta a mejorar, habran reuniones periódicas, por el mometno no estan los CPSM
	* Han habido muchas quejas de Luis Palacios
		* Grupo Ramos: la solución no funciona por un tema de DNS. Eso no lo evaluó el arquitecto, metieron a Jacobo. Luis se puso a la defensiva.
		* Tambien pasa con Adela.
	* [ ] Lecciones aprendidas / Retrospectiva - ya no se continuó #PMO #followup
* Asignaciones
	* Las asignaciones se hacen en equipo, se revisa el dashboard de quicksight
	* Esta pendiente el de grupo Ramos, (equipo Nelson y yo como CPSM), aún no ha arrancado, esta para el 9 de enero. Ya llegó el correo de Notificación. 
		* Estamos tratando de organizar todo, dentro de EMX. Yo seria el candidato 1.
		* 
## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
