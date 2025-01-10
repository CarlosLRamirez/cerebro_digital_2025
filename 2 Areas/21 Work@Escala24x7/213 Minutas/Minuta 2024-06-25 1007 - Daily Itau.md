---
type:
  - minuta
IDProyecto:
  - "11105"
date: 2024-06-25
modified: '"2025-01-10 13:16", "5tc/G1T+6"'
created: '"2024-06-25 10:07", "2tc/G6T+6"'
---
#minuta
#id11105 

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
2024-06-25

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
* Brenda vuelve a preguntar sobre la reunion para la configuración de Mimix 
	* 2:30 pm
	* I am in PDT time zone.  I am available today after 2pm and all day Wednesday.
* Alvaro dice que necesita el apoyo de soporte de Phoenix 


![[Pasted image 20240625103228.png]]
 - DR: Replication is in place
 - Van a tener otra copia del flash y se la van a presentar al LPAR en San Jose
	 - Stand-up the LPAR DR mañana en la tarde
	 - Agregar  256GB en la LPAR del DR

![[Pasted image 20240625104239.png]]
## Puntos de Acción acordados
*  

## Proxima Reunión
*   




###  Cempro

- Completar sheet de Ambientes , hacer una sesion de trabajo




## NGINX
- Validar si la infra de NGINX de Shared esta apagada.
	- Hacerlo de forma controlada minimizar el riesgo
	- Jueves 27  tentativa ventana.
		- [x] Enviar correo para ventana para de apagado ✅ 2024-08-20
- Darle cierre a la fase
- Pase a Operaciones
	- Actualizar el diagrama (HN no esta listo)
	- Jose debe esperar que termine Mario y Johan para actualizar el documento
- Reservar IPs para NLB (DR)
	- Cyber no genera politicas en vacío
- Crear los pipelines para los componentes de comunicaciones