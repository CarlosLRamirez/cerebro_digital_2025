---
created: 2024-12-13T10:31:55
modified: '"2025-01-07 10:23", "2tc/G1T+6"'
date: 2024-12-13
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "11206"
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
2024-12-13

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Raul
- Oscar

## Agenda
* 
## Temas Discutidos
*  Ambientes Bajos 11206:
	* No se tienen las imagenes en Redhat 9, vamos a tener que refrescar Costa Rica cuando estén listos
	* Los segmentos de red no van a cambiar, solo cambian las IPs,  solo va cambiar el SO d ela instancia
	* podemos ganar tiempo haciendo las pruebas de  telecomunicaciones, ya que el segmento es el mismo
	* Erwin esta haciendo verificaciones en los grupos de seguridad clonados en ambientes bajos.
* DR ID 11221:
	* Nosotros ya desplegamos VPC en la región de Ohio
	* Para DR no vale la pena replicar imagenes con el SO, hasta que este el nuevo SO
	* [ ] Podriamos iniciar con la replica de Oracle #followup #id11221

## Puntos de Acción acordados
- [x] Ajustar las cadencias para Martes y Jueves, incluir a David Chaparro y Daniel Bernal #id11206 ✅ 2024-12-13
	- Dejar la del martes para un proyecto
	- Y la del Miercoles para le otro proyecto


## Proxima Reunión
*   

---
