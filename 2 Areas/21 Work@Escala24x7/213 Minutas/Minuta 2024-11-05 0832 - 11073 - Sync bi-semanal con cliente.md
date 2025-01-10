---
type:
  - minuta
IDProyecto:
  - "11073"
date: 2024-11-05
modified: '"2025-01-10 14:45", "5tc/G1T+6"'
created: '"2024-12-16 08:13", "1tc/G12T+6"'
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
2024-11-05

## Asistentes

### Davivienda
* Maria Jose Guzman
* Brandon Osvaldo Cordova
* Jose Yerlis Jiron Casares
* Kimberly Salas
### Escala24x7
- Carlos Leonel Ramírez
-  Joel Solis
- Ruth Ardon
- Julio Pestana
- Yaxer Palacios

## Agenda
* 
## Temas Discutidos
* Fin de desarrollo roles y ajustes
	* Se espera tenerlo al final de esta semana (miercoles 13)
	* Para desplegar en QA
* Paralelamente  vamos a necesitar
	* El nombre del sitio en QA - Davivienda 
		* retailcloud-prd.daviviendacr.com ✅
		* retailcloud-qa.daviviendacr.com ✅
	* Desplegar los ALB - Yaxer
		* Compartir el nombre - Yaxer
		* Compartir el nombre - Yaxer
	* Registro CNAME - Davivienda
	* Generar certificado - Yaxer
	* Bucket S3  - Desplegar - Yaxer
	
	
## Puntos de Acción acordados
- 

## Proxima Reunión
*   

#leccionaprendida Aolocitar los urls, cnames, etc para todos los ambientes desde un principio. No solo desarrollo, y luego qa, y luego prod.

---
🎶
Author: Carlos Ramírez - 2024
