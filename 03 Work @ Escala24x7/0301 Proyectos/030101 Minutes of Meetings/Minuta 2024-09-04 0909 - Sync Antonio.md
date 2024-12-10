---
type: Minuta
IDProyecto: "11152"
date: 2024-09-04
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
2024-09-04

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  9/Sep: Incremento de disco en SUFI PRO: 
	* Pastor ya pidió el Disco
	* 50-55% utilización del disco
* 12/Sep: Instalación de Mimix en SUFI PRO:
	* Ese día se inicie los journals
* 14/Sep  Sistema Operativo
* 15/Sep: Sabado y domingo: el backup de SUFI PRO:
	* Opción 22 y data de usuario
	* Nunca recibimos usuario de Josh Patterson, sobre el comando, para salvar la data de usuario
* 16 y 17:
	* Adecuaciones de Cinta y DUCTAPE
* 17 viajar en la noche y 18 entregar la cinta
* Que el mismo 18 empiecen a trabajar en el LPAR
* 20/Sept: hacemos la planeación del cutover (tareas pre-cutover y cutovoer)
* 22/Sept: Tener la maquina y empezar a replicar los Journals
* 30/Sept: Maquina sincronizada
* Primera Semana de Octubre: 
	* Pruebas y Auditorias
* Segunda Semana de Octubre:
	* Cutover


NACIONAL:
- Vamos a hacer una reunion con Pastor para planear eso.

- En paralelo estamos trabajando en las VTL sincronizadas.
	- Necesitamos la IP de Ellos
	- Para mandar las reglas de FW

4 al 9 de Octubre:
- Antonio va pedir esos dias.


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
