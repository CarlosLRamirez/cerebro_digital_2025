---
type: Minuta
IDProyecto: "11188"
date: 2024-09-20
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
2024-09-20

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Raul Aquino
- Jose Figueroa
- Jhon Asuaje

## Agenda
* 
## Temas Discutidos

1. Cambios de aplicaciones:  
	* Tronador  (.jar)
	* SimonQuotation (web)
	* Si Salud (.NET)

No vemos impacto en el camio
Compromiso, de mantener los tiempos , dado que el cliente es quien instala las acciones.

2. Dejar claro que un solo single-sign on no se puede
	- Autenticacion y autorizacion de Appstream a travez del IDP (NetIQ) a travez de SAML
	- Siempre y cuanto se tenga claro que la aa es para la autenticacion de appsteram y que soporta SAML 2.0
	- 

	1. Configurar dos flotas
		1. Si se puede hacer, confirmado
		2. No tiene impacto
		3. Con la imagen vamos a hacer dos modos de visualicación

Con el objetivo confirmenos cual esea la fuente 







5. Lo de tener 2 flotas no va



## Puntos de Acción acordados 

## Proxima Reunión
*   

---
Template: [[Minuta 2024-12-12 0935 - Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
