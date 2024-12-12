---
type: Minuta
IDProyecto: "10854"
date: 2024-11-19
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
2024-11-19

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Este fin de semana para esta el pase a producción a Marcajes
	* Probablemente a las 8PM
* Servicio Consumo NAS, no nos han reportado ningún issue
* 

## Puntos de Acción acordados
- [x] Actualizar cuadro de servidores 📅 2024-11-19 ✅ 2024-11-19
- [x] Responder correo a Hugo Bran 📅 2024-11-19 ✅ 2024-11-19
- [x] Agendar sesión para PaO #followup
- [x] Propuesta Comercial sobre Modernizacion y SFTP, y carpeta de minutas #followup
-
## Proxima Reunión
*   

---
Template: [[Minuta 2024-12-12 0935 - Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
