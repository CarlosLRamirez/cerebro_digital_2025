---
type:
  - minuta
IDProyecto: "11065"
date: 2024-10-28
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
2024-10-28

## Asistentes

### Cliente
* Carlos David Robayo Murcia
* Julian Alberto Mejia
### Escala24x7
- Carlos Leonel Ramírez
-  Cori Arenas
- Nelson Mora
- 

## Agenda
* 
## Temas Discutidos
*  Accesos
	* Nelson Mora tiene bloqueado el acceso pero ya lo esta revisando internamente
	* Cori ya tiene accesoa Github, pero le faltan unos accesos a repositorios -- Ya Carlos David Robayo le esta apoyando
* Plan de Actividades:
	* Migración módulos dynamoDB (Nelson): Avance el 85% 
	* Migración módulos SNS (Iliana):  100%
	* Migración módulo S3 (Iliana): 100%
	* Restructurar componentes Black/Front
	* Migración de módulos Eventbridge (Cory): 
* Debemos destruir la infra actual para probar
	* Los países deben de parar de hacer cargas
* Hoy podriamos hacer el re-despliegue de los recursos
	* Sin la carpeta de modules
	* 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
