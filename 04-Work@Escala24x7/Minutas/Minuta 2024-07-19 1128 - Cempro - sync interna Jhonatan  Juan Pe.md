---
type: Minuta
IDProyecto: "10854"
date: 2024-07-19
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
2024-07-19

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
## Agenda
* 
## Temas Discutidos
*  Juan Pedro no tiene ese dato, porque no tiene la cantidad exacta de servidores de servidores que se van a migrar?
	* Eso es el excel? al final van a ser menos de 80
	* Williams Coro se llevo esa tarea
* Instalar agentes lo podemos hacer
	* Vamos a grabar y que ellos lo siguen
	* Meter todos los servidores en la regla del Firewall.
	* Tenemos que enviar el comando
* Servidor de impresión SVICR
	* Si esta cerrado, lo re-abrimos y se lo pasamos a operaciones
	* https://escala24x7.atlassian.net/browse/ESC-25535
* Cloud Foundation Assessment 
	* Ya se lo pasamos a AWS (Martin)
	* Ya lo completamos el 6 de junio
*  Conexiones que no se vean
	* [x] Hacer una reunión con el cliente  para las conexiones que no se ven 📅 2024-07-19



## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
