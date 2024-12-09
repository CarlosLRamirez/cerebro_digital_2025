---
type: Minuta
IDProyecto: "11152"
date: 2024-07-24
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
2024-07-24

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Hay una soluciòn tempral y una definitiva
	* Lo que se esta implementando con Cisco aplicaria cuando la solución multicloud salga a producción
	* Mientras tanto la tecnología que se va utilizar es la tecnología VERSA que ya se tiene una instancia en Connectria
	* Al proveedor de Cirium ya se hizo la solicitud sobre el enlace dedicado.
	* Se habia solicitado una LOA (donde se especificara que sitio), Connectria respondio quien deberia proporcionar eso es Cirum. Cirium esta en la entrega de ese SOA. El proceso ya esta andando para entregar esos canales internacionales, se espera que esta semana se entregue esta información. La otra semana podriamos pensar que el enlace ya esté puesto.
	* Los enlaces son Capa 3
	* Riesgo: la solucion de Cisco todavia esta en implementacion, para poderle cumplir al proyecto se debe hacer con VERSA.
- Jefferson describe la arquitectura de la solución de SDWAN Cisco	
	- ![[../attachments/Pasted image 20240724102737.png]]
	- Next Step: 
		- Fred lo revisará con el equipo de arquitectura. Roy se encargará de un adendum para considerar los recursos en Connectria.
		- Proveer las especificaciones de los Firewallls, lo cual se verá mañana.
		- Jefferson compartira a Jhon para que nos comparta el diagrama
		- Compartir un diagrama de la arquitectura de transisión
			- Direccionamiento diferente a nivel de WAN, a nivel de LAN es el mismo.

![[../attachments/Pasted image 20240724104150.png]]

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
