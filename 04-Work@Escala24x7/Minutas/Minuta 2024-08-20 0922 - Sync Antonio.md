---
type: Minuta
IDProyecto: "11152"
date: 2024-08-20
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
2024-08-20

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Antonio Flores

## Agenda
* 
## Temas Discutidos
- [x] NEcesitamos empezar a  ver el tema del modelo Operativo #followup
	- El banco tiene un area que se llama Controles de Accesos
		* El banco controla los usuarios privilegiados
		* El banco debiera seguir con el control de esos usuarios , eso dicen esos contratos
	* Tema de Monitoreo 
		* El banco tiene un área que se llama el CoES
			* que les vamos a compartir? que van a poder ver? como podemos integrar el monitoreo con esta gente
	* Tema de DR/Automatización #followup
		* Que cosa vamos a automatizar
		* Ya nos vamos a tener un SW llamado CRO (IBM resilliency orchestration)
		* Necesitamos empezar a tener esas conversaciones con Connectria 
	* Pruebas de DR, failover 1 semana luego retornar #followup
		* El banco cuando prueba el DR opera 1 semana en el DR 
	* Reportes, periodicidad #followup 
	* Rol de DBA #followup
		* Como podemos proveer reportes, asesorias, relacionadas con BD



## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
Template: [[Minuta 2024-12-12 0935 - Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
