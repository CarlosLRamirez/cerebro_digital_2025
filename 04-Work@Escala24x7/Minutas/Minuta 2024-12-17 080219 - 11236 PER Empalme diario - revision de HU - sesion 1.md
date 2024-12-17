---
created: 2024-12-17T08:02:19
modified: '"2024-12-17 08:09", "2tc/G12T+6"'
date: 2024-12-17
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto: 
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
2024-12-17

## Asistentes

### Cliente
* David Santiago Bohorquez Rodriguez
* Nicolas Leon Peres
* Darwin Gabriel Arellano Varas
* Daniela Arias Brinez
* Francisco Javier Medina Cordoba
### Escala24x7
- Carlos Leonel Ramírez
### MC
- Nahuel Moyano - Business Analyst 
- Sergio Bonano
- 
## Agenda
* Revision de Historias de Usuarios - 
## Temas Discutidos
* Necesidad de Prototipos
	* Ya compartimos los correos, Nicolas esta gestionando el acceso
	* Tienen las pantallas en un documento, pueden compartir eso mientras tanto
	* Con eso el FE puede ir adelantando el trabajo en local.
* Cambios de Historias de Usuario
	* Es probable que las HU haya cambiado, ya que ellos han hecho refinamientos 🚩
* Necesidad de contar con un Login de usuarios que no acceden del SSO, sino de una Banca
	* Igual el Logout, se debe dejar en la pagina de Login
	* Queremos confirmar si esa necesidad la tenemos?
	* La HU de SSO esta clara

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
