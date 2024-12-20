---
created: 2024-12-17T08:02:19
modified: '"2024-12-20 15:59", "5tc/G12T+6"'
date: 2024-12-17
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "11236"
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
* Necesidad de contar con un Login de usuarios que no acceden del SSO (usuarios del banco)
	* Igual el Logout, se debe dejar en la pagina de Login
	* Queremos confirmar si esa necesidad la tenemos?
	* La HU de SSO esta clara
	* Lo que podriamos hacer es una pantalla de inicio para poder logearse 🤔
	* Como acceder al módulo regional, sin venir de una banca?? 
	* Darwin Gabriel Arellano dice que eso NO VA -- El unico ingreso es de las bancas en linea
	* Aun no esta el desarrollo del canal
	* [ ] El SSO no se va poder implementar en este momento, porque el proveedor no lo tiene todavia 🚩 ⚠️ #risk #id11236 #followup
	* Portal táctico?? 🤔
	* Necesitamos revisar el tema del Sign On con Jenny 
	* El backoffice (control center) ese si va con usuario y clave
	* Sergio dice que necesita confirmar si eso implica tener otro login??? 
	* David Santiago se llevara la consulta para aclararlo con Erick y Jenny.
	- ![[Pasted image 20241217081714.png]]
	- Aclaración de Jenny:
		- hay 2 escenarios: usuarios BEL y usuarios Banco (backoffice - Control Center)
		- Necesitamos a David Bohorquez para aclararlo
		- La duda es que si necesitamos proveer un login para backoffice o es otro SSO?? ❓
		- La HU:8 habla de Control Center - se debe proveer usuario y clave
			- los usuarios banco seria con EntraID (Active Directory), genera token
			- Para los usuarios de CECA, solo seria con el web service, no genera token.
			- Esto requiere otra pantalla de login, pero la HU no menciona una pantalla de Login para CC
			- ![[Pasted image 20241217083226.png]]
			- Necesitamos una nueva HU para este login, y referenciar al usuario que vino de una banca (cliente) y un usuario del banco
			- HISTORIA NUEVA, NUEVA PANTALLA  🚩
				- Erwin dice que no es necesaria una nueva HU
			- Tambien necesitamos un UI/UX para el Control Center 🚩, dicen que lo crea Escala24x7??
				- 🧠 entiendo que estan diciendo que ellos no van a hacer el prototipo del modulo administrativo
- Dudas HU: Cliente multidestinos
	- El cliente multidestino se debe determinar desde el modulo regional con una replica del usuario
	- Se debe migrar de la base de datos de technisys a la de PER
	- El servicio es multilatino por la replica de usuarios, con el modelo de datos de una replica
- Dudas HU: URL a la banca local
	- Es una URL unica y luego re-dirige a los pases: R/ es una URL distinta para cada pais
	- Porque cada uno es un portal diferente
	- El usuario debe retornar, se hace cierre de la sesión y vuelve al modulo regional.
	- Debe volver al login que lo origino
- Hoja de Ruta (Roadmap) preliminar
	- Nicolas pregunta si tenemos una hoja de ruta?
	- Sergio dice que tomando las HU del MVP, se iniciaría con:
		- la 1
		- la 2 Single Sign-on
		- la 3 Home 
		- La parte de Logout (no hay una HU que lo especifique)
		- Proposito: tener ida y vuelta de inicio de sesiones, y el nuevo login de CC.
		- David Bohorques, dice que se debe socializar con Fabian Zambrano (seguridad).

## Conclusiones
- Si se necesita una nueva pantalla de login para los usuarios internos banco

## Puntos de Acción acordados
- [x] Necesitamos la ultima version de HU  #followup #id11236
- [ ] Esperamos una nueva HU (o ajuste) para el login de Control Center #followup #id11236
- [x] Compartir los prototipos de las pantallas a desarrollar (incluido al modulo administraivo) #followup #id11236
- [ ] Necesitamos una HU que haga referencia a logout #followup #id11236
- [x] Confirmar espacio para revisar diagrama de dependencias de comunicaciones  #followup #id11236


![[Pasted image 20241217085615.png]]


## Proxima Reunión
*   18/Dic/2024

## Resumen enviado al cliente
Buenos días a todos, gracias por su tiempo el dia de hoy:

Comparto los puntos principales discutidos y los puntos de accion:

##Temas Discutidos
- Necesidad de contar de los prototipos de UI/IX
- Cambios recientes en las HUs
- Login para usuarios internos del banco
- Consultas sobre cliente multidestinos
- Consultas sobre URLs de banca local
- Mapa de ruta preliminar

## Puntos de Acción 
- Compartir  la última versión de HU - Davivienda
- Agregar una nueva HU o ajustar existente para el login de Control Center (Backoffice) - Davivienda
- Compartir los prototipos de las pantallas a desarrollar (incluido al módulo administrativo) - Davivienda
- Agregar una HU que haga referencia a logout - Davivienda
- Confirmar espacio para revisar diagrama de dependencias de comunicaciones  - Davivienda


---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
