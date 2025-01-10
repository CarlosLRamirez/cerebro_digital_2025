---
type:
  - minuta
IDProyecto: "11152"
date: 2024-12-10
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
2024-12-10

## Asistentes

### Cliente
* Monica Maria Martiez
* Fabio Alonzo Zapata
* Cesar Augusto Villegas
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  

## Puntos de Acción acordados


1. Tener acceso desde la operación a las maquinas de connectria
2. Solucionar el tema de la latencia que hoy tenemos con controlm para poder ejecutar los jobs de salvado.
3. tener los menús dentro del perfil de computo que usariamos para el manejo de la vtl
4. Tener una capacitación para cada uno de los casos de uso que hoy tenemos con la vtl
5. Validar si estos cambios no afectan la aplicación PRI que es la que maneja el maestro de la información historica
6. interactuar con la VTL, realizar pruebas
7. Migrar las mallas de DDS y QA, para garantizar la operación en producción



## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
