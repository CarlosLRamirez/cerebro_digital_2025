---
type:
  - minuta
IDProyecto: "11152"
date: 2024-07-29
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
2024-07-29

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Tiene que estar Juan David  Leon o Mayra
* Los conectores ya existen, seria agregar un nuevo usuairo
	* Mayextra

## Puntos de Acción acordados


![[Pasted image 20240729101637.png]]


1. Crear una cuenta de Conexión (pedir los accesos que se requieren)
	- Reunion con Jessica para contextualizarla
	- Dispositivo (token)?
![[Pasted image 20240729102331.png]]

2. Crear un nuevo Perfil en CyberArk
	- Nombre del perfil
	- Descripición y Dueño del Perfil
		- grppiconnectria
		- Administradores Connectria iSeries
		- ehidalgo@bancolombia.com.co (a el van a llegar las solicitudes del pefil, se debe contextualizar)

3. Agregar los usuarios finales al perfil en cyberark
	- Con usuario de red banco

4. Registrar ese usuario de conexión a Cyberark 


- A cyberark se autentica con MFA de Azure
- 



## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
