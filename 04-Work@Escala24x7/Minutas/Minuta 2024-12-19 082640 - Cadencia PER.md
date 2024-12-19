---
created: 2024-12-19T08:26:40
modified: '"2024-12-19 08:36", "4tc/G12T+6"'
date: 2024-12-19
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto: 
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
2024-12-19

## Asistentes

### Cliente
* David Santiago Bohorques
* Darwin Gabriel Arellano
* Nicolas Leon Perez
* 
### Escala24x7
- Carlos Leonel Ramírez
- Jenny Rodriguez
-  Sergio Bonano - MC
- Nahuel Moyano - MC
- Juan Galeano - MC

## Agenda
* 
## Temas Discutidos
- Se reviso el portal de flujo del Login
* Technysis aún esta trabajando en el cierre de sesión de Banca En Linea

## Puntos de Acción acordados
- [ ] Login: usuarios de prueba - Davivienda #followup #id11236
- [ ] Login: nombre de servicios y endpoints - Davivienda #followup #id11236
- [ ] Login: contratos y documentación de los servicios #followup #id11236
- [ ] Jenny ajustara el diagrama de Login y enviará a Davivienda (mapeo de servicios) #followup #id11236

## Proxima Reunión
*   

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
