---
type:
  - minuta
IDProyecto: "11065"
date: 2024-08-22
---
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
2024-08-22

## Asistentes

### Cliente
* Lina Milena Mantilla
* Miguel Leonardo Chaparro
### Escala24x7
- Carlos Leonel Ramírez
- Nelson Mora
- Mario Cruz
- Iliana Estupinian
## Agenda
* 
## Temas Discutidos
*  Estamos bloqueados por el tema del nombre en los módulos, por la rama que se borro, en la rama nueva hay otro requerimientos en los nombres de archivos.
* [x] Vamos a poner un nombre temporal en el modulo de Terraform, pero no es el correcto según los lineamientos de Davivienda #followup
* [x] Hay un solapamiento de IPS en el ambiente DEV de Mbaas #followup
	* El equipo de networking tiene una reunion el dia de mañana 22/Agosto.
- [x] Tambien esta el tema de la resoulcion de DNS para Canales #followup
	- Actualmente se esta haciendo con el archivo de host
## Puntos de Acción acordados
- 
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
