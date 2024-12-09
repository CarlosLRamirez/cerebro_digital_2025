---
type: Minuta
IDProyecto: emx-davivienda
date: 2024-08-20
---
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
2024-08-20

## Asistentes

### AWS
* Monica Ruiz
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* Sync mensual con Monica
## Temas Discutidos
*  Migración Cyberbank
	* Hubieron unas optimizaciones y el consumo bajó
	* ![[../attachments/Pasted image 20240820141204.png]]
	* ![[../attachments/Pasted image 20240820141222.png]]
	* Tema del DR
		* La vez pasada hablamos sobre: Se iba tener una reunión con el equipo, para ver estrategia de pilot light
	* La última vez Jenny pidio apoyo en actualizar la plataforma el OLA
	* También se estaba viendo incluir otras oportunidades
* DR Update
	* No han dicho nada
* Ambientes Bajos Update
	* Esta de lado de compras Davivienda, se iba a subir a Ariba
* Otros proyectos
	* Whitelist & NetRetail
	*  ![[../attachments/Pasted image 20240820141302.png]]
	* [x] Validar si los recursos de Whitelist y NetRetail pueden aplicarse el Tag de MAP. mas 10% de Analitica   📅 2024-08-20
	* https://s3-us-west-2.amazonaws.com/map-2.0-customer-documentation/included-services/MAP_Included_Services_List.pdf](https://s3-us-west-2.amazonaws.com/map-2.0-customer-documentation/included-services/MAP_Included_Services_List.pdf)
	* [x] Validar si el Direct Connect de Cyberbank Davivienda esta tageado  📅 2024-08-21


## Puntos de Acción acordados
-
## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
