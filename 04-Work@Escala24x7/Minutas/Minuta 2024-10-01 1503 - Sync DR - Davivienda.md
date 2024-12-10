---
type: Minuta
IDProyecto: emx-davivienda
date: 2024-10-01
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
2024-10-01

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos

Tres objetivos
1.  Quieren revisar el cronograma el viernes
	* Se necesita darle a los países una fecha de salida
	* La prioridad es El Salvador
2. David necesita repasar la arquitectura, para estar seguros lo que se va levantar a Ohio
	1. De la ultima sesion se vio que ya se tenia una shared services
	2. La expectativa es que ellos tengan una cuenta privada de Seguridad
	3. En la de Networking, que converga las telecomicaciones
		1. Se le pidió a Escala eliminar lo que se habia desplegado (Shared Services)
		2. No se ha creado la nueva cuenta?
		3. Se necesita crear una nueva cuenta y mover el Direct Connect a esa cuenta
	4. En que estado esta el Direct Connect??
		1. Se contrataron dos enlaces:
			1. uno de Bogota (CCI) a AWS a Virginia/Ohio
				1. eso se vio con Diego Ortegon
				2. Esto ya se configuró? estamos enviando trafico por alli? eso necesitamos verlo con Franklin
				3. A que cuenta esta llegando?
				4. que factible es pedirle que este Direct Connect se mueva de cuenta.
			2. uno de Medelling a AWS a Virgina/Ohio, ese todavia no esta por un tema de respacio en Rack

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
