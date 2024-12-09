---
type: Minuta
IDProyecto: "11105"
date: 2024-06-24
---
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
2024-06-24
## Asistentes

### Itaú
* Juan Camilo Garcia
* Liliana Canon Reyes
* Ruben Dario Avendano
* Brenda Catalina 
* William Castr
### Escala24x7
- Carlos Leonel Ramírez
- Jeremy Enciso
## Agenda
* 
## Temas Discutidos
* [x] Pruebas Cierre #followup
	* El sábado corrieron el cierre de producción, salieron unas actividades que no se cerraron, hoy a las 2pm tienen una sesión, luego de este análisis lo vuelven a correr
	* El tiempo que están viendo: 5h 14min, 5h 12min (Connectria) vs 5h 1min (on-premise)
* [x] Tiempo de la PoC #followup
	* Correo del 17 y 21 de junio 
	* Necesitan mas tiempo? deadline 5 de julio
* [x] VPN San Jose #followup
	* Enviamos el Formulario el 21 de junio
- Si envían hoy el formulario, podemos coordinar la actividad en horas d en la mañana, 9am a 10am
	- [x] Confirmar Dispnilibdad de Fred mañana a las 9am Connectria.   📅 2024-06-24 #id11105
*  Configuración Mimix #followup
	* Enviamos un correo solicitando cierta información el 20 de junio
	* [x] Confirmar Disponiblidad de Connectria para configuración de Mimix  📅 2024-06-24 #id11105
- [x] Pregunta sobre quitar memoria para pasarselo al LPAR 2  📅 2024-06-24 #id11105

## Puntos de Acción acordados
*  

## Proxima Reunión
*   


---
## Otros apuntes
