---
type:
  - minuta
IDProyecto:
  - "11065"
date: 2024-11-20
modified: '"2025-01-10 12:11", "5tc/G1T+6"'
created: '"2024-12-16 08:13", "1tc/G12T+6"'
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
2024-11-20

## Asistentes

### Cliente
* Miguel Leonardo
* Lina Milena
### Escala24x7
- Carlos Leonel Ramírez
- Jhonathan
- Cori
- Iliana

## Agenda
* 
## Temas Discutidos
*  Tema de la comunicación de SuperApp luego del re-despliegue
	* Miguel Leonardo es el lider de SuperApp
	* Nelson pidió una prueba que no le apuntaran al DNS sino a la dirección específica
		* Esa prueba ya lo hizo Miguel ayer
	* Jhonatan cree que el tráfico no esta llegando en la cuenta Shared
	* Jhonatan dice que lo mejor es que se haga una reunión con Technysis
	* Jhonatan cree que Technysis todavía tiene mapeadas las antiguas IPS, sin embargo el si ve el trafico llegar en las IPs nuevas
	* Technysis tiene un tercero que administra la infraestructura en Azure
	* Desde Shared al Endpoint el camino si llega
	* La petición es que prueben conexión desde Azure hasta el endpoint
	* Miguel no nos puede dar una fecha, porque es un proveedor de Technysis
	* Antes funcionaba a una sola IP, hacia el DNS nunca ha funcionado, se quemo en la tabla de host.
	* [x] Jhonathan propone implementar una solución en Route53 para el tema de la resolución DNS de SuperApp - #id11065 #closed pedirle que lo envie por correo; 10.231.225.162 Todo lo que va a *.execute-api.us-east-1.amazonaws.com ---> 10.231.225.126, 10.231.225.150

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
