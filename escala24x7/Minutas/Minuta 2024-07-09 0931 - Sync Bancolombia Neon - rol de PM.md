---
type: Minuta
IDProyecto: "11152"
date: 2024-07-09
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
2024-07-09

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
- Antonio Florez
- Cesar Perez
- 

## Agenda
* Sesión para dar visibilidad y explicar a Carlos el proyecto desde la perspectiva de los crecimientos que el banco espera solicitar en el corto y mediano plazo, recibir recomendaciones de PMO al respecto y prepararnos para abordar las complejidades relacionadas.
## Temas Discutidos
*  Se firmaron 2 SoW de cara al banco
	* Migración Fiduciaria: 
		* Fue lo que se probó en la PoC
		* iba ser FIDU primero y SUFI despues, y en paraleo se estaba trabajando en el credicimento de Fidu. Pero va pasar a Nacional
		* En resumen es un Big Bang
* Traernos a todos (Operaciones)
* El jueves tenemos una reunion con Connectria
* 100% Carlos
* Hay PoC dentro del proyecto
* Antonio hizo un backlog
* Antonio pide que primero se pregunte a el, antes de preguntarse al Banco, no dar la sensación al Banco que no estamos alineados. 
* Sync diario con Antonio
* Diseño de Comunicaciones
	* hoy a las 11:00 se tiene una conversación con Josh
	* VLAN extendidas? cual es la experiencia de Connectria.
* DEADLINE DURO: 1era SEMANA de Noviembre
	* SIN FALLOS
* Connectria: Kickoff  - Jason Weller
	* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`