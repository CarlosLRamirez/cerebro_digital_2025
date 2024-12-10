---
type: Minuta
IDProyecto: "11152"
date: 2024-11-19
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
2024-11-19

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* BCOM Checkpoint
## Temas Discutidos
1.  La decision que se toma es que este fin de semana no salimos, motivos
	* El fin de semana no se pudo hacer cambio VRS,  por esto no se pudo probar
		* Sterling
		* MQ
		* LZ
		* Control M
	* Algunas pruebas que si se hicieron pero no funcionaron durante la sesión,
		* Control M
		* Manejo de VTL
	* Ademas hay otros pendientes que evidencian que este fin de semana no es posible salir
2. Replantear el plan y enfocar en las cosas que están pendientes
	- Prueba en diciembre? es complejo pero puede ser posible
3. Pendientes
	- NAT de monitoreo para PROD
		- Jason nos confirma para cuando esté
	- Control M / VTL
		- Finalizar el etiquetado de las VTL
		- Habilitar los Menus
		- Capacitación
	- Backups de SUFIDDS y SUFIQA via BRMS
	- QSECOFR directo por CyberArk
		- Evaluar que perfiles deberían tener ese permiso
	- Prueba de acceso por CyberArk para los 3 ingenieros de LE
	- Cifrado del Direct Connect
		- Tatiana respondió que no se puede
	- Aplicación de Novedades
		- Eso lo tiene Antonio
	- HA: Automatización de Kro
	- HA: Prueba de LPM
		- Enviar invitación y enviar pre-requisitos
		- Vale la pena hacer la prueba del LPM?
	- 

  
## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
