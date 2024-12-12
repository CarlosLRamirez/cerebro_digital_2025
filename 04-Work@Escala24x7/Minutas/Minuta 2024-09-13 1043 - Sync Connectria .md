---
type: Minuta
IDProyecto: "11152"
date: 2024-09-13
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
2024-09-13

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* SUFI DDS - SUFI QA
	* Ya tenemos conexión de los usuarios
	* Bancolombia nos va proporcinar un segmento de red para natear la conexión desde conectria para administraciòn y monitoreo
	* Necesitamos empezar a trabajar en los runbooks.
		* How and when to notify for the systems
		* Escalation and Notification requeriements
		* At least some notification path
	* Bancolombia va iniciar a poner al día las maquinas
* SUFI PRO
	* Hoy en la noche se hace en incremento de los 2TB en ASP1
	* Las reglas de FW y el enrutamiento hacia Connectria esta listo, hoy se hizo una prueba, pero la ip en Connecria no respondió.
	* Mañana a las 7am esta aprobado para iniciar la actividad de Mimix
	* El domingo se saca el backup de SUFI PRO
* Direct Connect
	* Ya probamos la conectividad end-to-end de la red de QA
	* No hemos podido probar la conectividad end-to-end en la red PDN, estamos esperando que Bancolombia habilite el ICMP
	* Luego de validar la prueba , el siguiente paso es desplegar el servicio definitvo de Direct Connect
- 
## Temas Discutidos
*  

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta 2024-12-12 0935 - Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
