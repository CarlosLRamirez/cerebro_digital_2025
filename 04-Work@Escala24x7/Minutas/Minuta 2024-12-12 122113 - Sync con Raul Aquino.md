---
created: 2024-12-12T12:21:13
modified: '"2024-12-12 12:31", "4tc/G12T+6"'
date: 2024-12-12
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
2024-12-12

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Raul Aquino

## Agenda
* 
## Temas Discutidos
*  

## Puntos de Acción acordados
- DR
	- DR estamos esperando las pruebas
	- No se va replicar hasta que se tenga una imagen lista 9.4
	- Hasta el 10 de Enero se tiene un freeze, para poder desplegar el networking on-premise 
- Ambientes Bajos
	- El viernes se unió Edisson, están trabajando en el despliegue de la infraestructura
	- Necesitamos que Fernando nos ayude a avanzar.
	- Nuestros recursos se están viendo afectados, Raul levanto la mano suavemente con el riesgo de suspension
	- Raul envió un correo sobre los dos proyectos, Fernando respondió que están trabajando, estábamos pidiendo un plan de pruebas. Fernando dijo que no tenían un plan muy detallado de pruebas, sino solamente un script.
	- En la llamada del Martes se unió David Chaparro y Erwin, estas actualizaciones las envió Raul en un correo.

Hay poca participación en las llamadas, por solicitud de Francisco (Axity) Martes y Jueves para cubrir los dos proyectos.



## Proxima Reunión
*   




---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
