---
created: 2024-12-18T08:04:37
modified: '"2024-12-18 08:20", "3tc/G12T+6"'
date: 2024-12-18
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "11236"
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
2024-12-18

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
* Ya nos enviaron los nuevos HU
* Los diagrams de flujo los esta trabajando arquitectura DAV, y se espera tenerlos el 3 de Enero
	* El diagrama lógico de la funcionalidad
	* Necesitaríamos priorizar los flujos de autenticación (single-sign on y cierre de sesión)
	* El siguiente seria la integración de los usuarios de las bancas.
* Pantallas
	* Ayer se hizo la solicitud  a fábrica (Daniela) , normalmente se toman una semana )
* Estimacion
	* Vamos a revisar las HU, es especial los de login - Confirmar lectura: mañana podemos hacer un check
	* Necesitamos los prototipos (schedule)
* Que necesitamos para empezar a construir campo a campo de los servicios?
	* Lo primero que necesitamos es el token
	* Sergio dice que pueden avanzar (sin necesidad de infraestructura) es pantallas
	* [ ] Definición de Jenny de autenticación y servicios que están expuestos  #id11236 #followup
		* Tenemos que involucrar a Fabian Zambrano
* Gestión de accesos a DevOps

Resumen
- DevOps y eso
- Definir primer entregable hito
- Formalización de Jenny
- Pantallas

- Usuarios de DevOps
- 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
