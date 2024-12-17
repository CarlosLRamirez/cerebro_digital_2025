---
created: 2024-12-17T08:02:19
modified: '"2024-12-17 08:21", "2tc/G12T+6"'
date: 2024-12-17
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto: 
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
2024-12-17

## Asistentes

### Cliente
* David Santiago Bohorquez Rodriguez
* Nicolas Leon Peres
* Darwin Gabriel Arellano Varas
* Daniela Arias Brinez
* Francisco Javier Medina Cordoba
### Escala24x7
- Carlos Leonel Ramírez
### MC
- Nahuel Moyano - Business Analyst 
- Sergio Bonano
- 
## Agenda
* Revision de Historias de Usuarios - 
## Temas Discutidos
* Necesidad de Prototipos
	* Ya compartimos los correos, Nicolas esta gestionando el acceso
	* Tienen las pantallas en un documento, pueden compartir eso mientras tanto
	* Con eso el FE puede ir adelantando el trabajo en local.
* Cambios de Historias de Usuario
	* Es probable que las HU haya cambiado, ya que ellos han hecho refinamientos 🚩
	
* Necesidad de contar con un Login de usuarios que no acceden del SSO, sino de una Banca
	* Igual el Logout, se debe dejar en la pagina de Login
	* Queremos confirmar si esa necesidad la tenemos?
	* La HU de SSO esta clara
	* Lo que podriamos hacer es una pantalla de inicio para poder logearse 🤔
	* Como acceder al módulo regional, sin venir de una banca?? 
	* Darwin Gabriel Arellano dice que eso NO VA -- El unico ingreso es de las bancas en linea
	* Aun no esta el desarrollo del canal
	* El SSO no se va poder implementar en este momento, porque el proveedor no lo tiene todavia 🚩 ⚠️
	* Portal táctico?? 🤔
	* Necesitamos revisar el tema del Sign On con Jenny #followup #id112363
	* El backoffice (control center) ese si va con usuario y clave
	* Sergio dice que necesita confirmar si eso implica tener otro login??? 
	* David Santiago se llevara la consulta para aclararlo con Erick y Jenny.
	- ![[Pasted image 20241217081714.png]]
- Dudas HU: Cliente multidestinos
	- El cliente multidestino se debe determinar desde el modulo regional con una replica del usuario
	- Se debe migrar de la base de datos de technisys a la de PER
	- El servicio es multilatino por la replica de usuarios, con el modelo de datos de una replica
- Dudas HU: URL a la banca local
	- Es una URL unica y luego re-dirige a los pases: R/ es una URL distinta para cada pais
	- Porque cada uno es un portal diferente
	- El usuario debe retornar, se hace cierre de la sesión y vuelve al modulo regional.
## Puntos de Acción acordados
- [ ] Solicitar ultima version de HU  #followup #id11236

## Proxima Reunión
*   

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
