---
type: Minuta
IDProyecto: "11152"
date: 2024-07-25
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
2024-07-25

## Asistentes

### Cliente
* Juan David Vergara
* Maria Elsy Giraldo
### Escala24x7
- Carlos Leonel Ramírez
-  Cesar Perez
- Alejandro Planas

## Agenda
* 
## Temas Discutidos
*  Cuales son los requerimientos de storage que están pidiendo?
	* el SoW de Fiduciaria contempla Flash (Compatible con FIDU)
	* Al meterle las otras aplicaciones el IOPS se multiplica, por lo que el requerimientos del storage cambia.
	* Los recursos adicionales se activaban por demanda.
	* La partición tiene hoy en día 32cores, y la maquina tiene disponibles 90+ cores, con Kindry el sistema es sencillo.
* Maquina fresh en Connectria
	* Richar pidio un documento con el detalle del alcance de la PoC - Antonio lo esta trabajando

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
