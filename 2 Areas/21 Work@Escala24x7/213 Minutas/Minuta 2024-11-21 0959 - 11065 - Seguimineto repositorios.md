---
type:
  - minuta
IDProyecto:
  - "11065"
date: 2024-11-21
modified: '"2025-01-10 14:42", "5tc/G1T+6"'
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
2024-11-21

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
- [x] Cori tiene problemas con el MFA de Davivienda para el Github #id11065
	- Se necesita pedir soporte al cliente
- Comunicacion SuperAppç
	- Ellos tienen que arreglar el enrutamiento, agregar los IPS
- Reorganizaciond el codigo
	- Iliana ayer reportó un error, darle seguimeinto  
- Ajustes cosmeticos que estaa haciendo Nelson
	- Nelson ya completó los ajustes, falta que ellos los prueben.
- Problemas de comunicacion con GoAnywere?
	- Lina no esta revisando.. debemos dar seguimiento
	- El problema es el cambio en la ruta de Destino, ya Lina lo solicitó y esta esperando confirmacion




- Ambinete de integracion para SuperApp
	- van a hacer unas pruebas nuevamente en DEV
- DEspliegue el LaboratoriO
	- van a volver a probar, incluido MBaaS
- Desplieuge en PROD
	- 


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
