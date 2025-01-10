---
type:
  - minuta
IDProyecto: "11152"
date: 2024-07-15
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
2024-07-15

## Asistentes

### Escala24x7
- Carlos Leonel Ramírez
- Antonio Florez
- Camilo Villamil
- Cesar Perez
- Alejandro Planas

## Agenda
* Sync diario 
## Temas Discutidos
* Estamos esperando una linea de tiempo del Banco
* Esta semana se dispara Leasing
	* Son 4 LPARs mas (Son máquinas pequeñas)
* Antonio tiene una reunión hoy en la tarde con el equipo que va migrar la maquina de Desarrollo y QA de Medellín (Esto es oootro SoW)
* Tema licencias de terceros?
* Antonio pide apoyo de Carlos para dar seguimiento a los temas con Maria Elsy
	* Alejandro comenta que eso deberian ser conversaciones con el comercial
	* Debería haber un punto de encuentro con el comercial, para que centralize todos los requerimientos de Bancolombia
* Antonio dice que hay un backlog de cosas (IDR, licencias)
* Walter sacó el tema en una reunión,
## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`