---
type: Minuta
IDProyecto: "11152"
date: 2024-08-01
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
2024-08-01

## Asistentes

### Cliente
* Andres Camilo Carmona
* Didier Giovanni Cairasco
* Paula Yulieth Ospina
* Antonio Florez
* Pastor de los Rios
### Escala24x7
- Carlos Leonel Ramírez
## Agenda
* Revisar alternativas para sacar el backup de SUFI
## Temas Discutidos
*  Connectria propone hacer el backup en modo restringido y save while active
	* a las 2pm se coloca el sistema en estado restringido y se inicia el backup
	* Terminado se libera el sistema y luego se saca un save while active de las librerias de usuario.
	* A las 6pm que empiezan los usuarios a ingresas, van a enfrentar el riesgo de tener algo bloqueado.
* La segunda opcion implica aprovisionar recursos sin embargo tomaría mas tiempo
	* La segunda opción implica provisionar un flash-copy, lo cual puede incluir un costo
	* depende que Kindryl tenga los recursos para presentar los discos, normalmente toma varios dias, hasta 20. 🚩
	* Igual tenemos que validar si implica poner estado restringido
	* Debemos preguntarle a Kindril cuanto se tardarian en aprovisionar y presentar el storage a la máquina.
	* [x] AP: Pastor va buscar una reunion con Ariosto de Kindryl #followup
	* Necesitamos tener metricas de tiempos por Tera, y que bloqueos genera el flash copy?
	* [x] AP: Luego de la sesion con Aristo, podemos programar un espacio con Connectria #followup
* El 11 Agosto hay programado un IPL de SUFI 🚩 
	* Podríamos empezar la ventana hasta las 8AM
	* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   



---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
