---
created: 2024-12-26T08:02:50
modified: '"2024-12-26 08:27", "4tc/G12T+6"'
date: 2024-12-26
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
2024-12-26

## Asistentes

### Cliente
* David Santiago Bohorquez
* Diego Felipe Garcia
* Nicolas de Leon
### Escala24x7
- Carlos Leonel Ramírez
- Jenny Rodriguez
- Sergio Bonanno (MC)

## Agenda
* Empalme Diario proyecto PER 
## Temas Discutidos
- Incorporación de Diego Felipe (PO Regional) quien estaba de vacaciones
* Login de CC
	* Con el diagrama de Jenny esta bastante claro
* Login de BEL
	* Los clientes de Miami no van a utilizar el SSO, estos clientes ingresan dese otra banca en linea (CO o PA), 
	* Diego explica el flujo esperado, se espera que al moverse de una BEL a PER, se cierre la sesion de BEL e ingrese a PER, si necesita regresar debe autenticarse nuevamente.
	* Los usuarios de CECA deben tener activado el Softoken.
	* Debe aparecer un mensaje de advertencia al usuario que se está yendo del a BEL, y debe cerrar la sesión en BEL
	* [ ] El flujo del Softoken lo debemos definir con David Romero para entregar los consumos a Escala #id11236 #followup
* Logout
	* 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
