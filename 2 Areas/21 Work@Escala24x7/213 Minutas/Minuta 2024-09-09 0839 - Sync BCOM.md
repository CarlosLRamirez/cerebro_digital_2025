---
type:
  - minuta
IDProyecto: "11152"
date: 2024-09-09
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
2024-09-09

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Hoy sesión para lo de los Journals
* Tema de DevOps
	* Antonio dice que no operan nada en los IBMi
* Antonio hará la prueba de S3 Storage
* VTL con Connectria
	* Antonio lo esta viendo
* Sergio esta viendo el tema de la tarjeta virtual que esta pidiendo Tatiana, para revisarlos a nivel de arquitectura
	* VNIC adicional que Tatiana mencionó y Tatiana lo escaló con arquitectura y con cyber, para ver la posición de Bancolombia
	* Autentic y Atalas ???

===
* Antonio quiere que el fin de semana, instalar Mimix
* Tiene que ser en ventana, haga de cuenta que es un IPL
* 
===

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
