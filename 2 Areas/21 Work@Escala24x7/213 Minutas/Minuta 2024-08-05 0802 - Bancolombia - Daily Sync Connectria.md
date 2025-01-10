---
type:
  - minuta
IDProyecto: "11152"
date: 2024-08-05
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
2024-08-05

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos 
- Ya recibimos la información definitiva del FW, Roy estarán trabajando con Nancy con el addendum para la SoW
- Accesos a Connectria
	- Daniel Valverde recibió un correo, lo está revisando
	- Cesar Perez preguntó al banco con quien podemos tener una sesión con Connectria, Esperando para agendar dicha sesión a travez de Nancy.
	- Una alternativa es usar a Cesar Gom

- [x] Solicitar OVAs a Bancolombia para los Firewalls 📅 2024-08-05 ✅ 2024-08-20
* [x] Seguimiento a Cesar para reunion con Banco para ver tema de accesos con el VP de Seguridad de Connectria #followup

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
