---
type:
  - minuta
IDProyecto:
  - "10854"
date: 2024-07-09
modified: '"2025-01-10 13:11", "5tc/G1T+6"'
created: '"2024-07-09 10:37", "2tc/G7T+6"'
---
#id10854 
#minuta

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
2024-07-09

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Jhonatan Muñoz
- Gerardo Calderon

## Agenda
* 
## Temas Discutidos
*  Definición de casos de uso
	* El viernes se tuvo la sesión, se entiendo la necesitad técnica del cliente
	* Sin embargo pidió costos (GB), y compararlo con on-premise, Jhonatan tuvo una sesión con Arquitectura y comercial
	* Juan Carlos se comprometió enviar la información a Cempro
		* Jonathan espera la resolución de Cempro con respecto a los costos
	* Seria FSX y Storage Gateway
	* EFS ya no iría
	* Jonathan podria trabajar sin el diagrama de Arquitectura para agilizar
* AWS Transfer Family (SFTP)
	* Se tuvo una sesión ayer, se envió un correo con el enlace de la documentación.
	* Con el correo quedo cerrado el tema, se pidió contestar el correo con el OK
	* Jonathan cerro las tareas en JIRA
	* [x] Hay una tarea en JIRA sobre lo de Cognito, Gerardo le mostró como se implementaba el WAF y como se atachaba al userpool, darle seguimeinto para ver si lo damos por cerrado, ellos quedaron de definir las reglas #followup
* Migración del servidor de impresion
	* Se cerraron las tareas en JIRA
	* Se cerraron las tareas en el RAID Log
	* El servidor ya se pasó a testing para que Cempro realize pruebas (05/07), la pelota esta en ellos.
	* El siguiente paso es pasarlo a producción.
* Migración lift shift
	* Hoy confirmaron que llenaron el cuadro en Excel (hasta hoy!!!),  Jenny lo revisará
	* Jenny tiene una sesión hoy con Cempro para la depuración.
	* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`