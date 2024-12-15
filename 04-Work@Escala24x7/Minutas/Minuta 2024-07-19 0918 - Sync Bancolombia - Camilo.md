---
type: Minuta
IDProyecto: "11152"
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
-  

## Agenda
* 
## Temas Discutidos
* [x] Enviar documento (PPT) a Didier, para sustentar los argumentos para irse con una sola OLA 📅 2024-07-19
* [x] El punto de la transferencia de los 800 GB diarios es critico para los lideres del banco y necesitamos resolverlo @Carlos Ramirez  démoste prioridad a esto y un seguimiento muy estricto y documentado en conjunto con Connectria.  @Carlos Ramirez  debe hacer parte de esas discusiones  @Antonio Florez - Medellin, COL #followup **Outcome esperado:** se debe confirmar una tecnología que resuelva ese tema. (Antonio/Connectria)
* [x] Sesión de Modelo Operativo follow up con Jason 📅 2024-07-19
* [x] La copia que sacaría el banco NACIONAL, el 28/07, cuando se saca? Hay unos riesgos operativos, esos riesgos se tienen que llevar al liderazgo - Hacer matriz de riesgos. **Outcome: conversación para socializar los riesgos del backup, tener la fecha, y que dependencias** #followup
* [x] @Antonio Florez - Medellin, COL  por favor envía asap las preguntas a Connectria con respecto al escenario de replica de archivos usando **global mirror** en reemplazo de Mimix según lo conversado - ¿DR o replica migracion? #followup con Antonio.
* [x] Correo para alinear tema de comunicaciones pre-sales/proyecto .. incluir a Richard/Alejandro Planas. ✅ 2024-08-20


## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
