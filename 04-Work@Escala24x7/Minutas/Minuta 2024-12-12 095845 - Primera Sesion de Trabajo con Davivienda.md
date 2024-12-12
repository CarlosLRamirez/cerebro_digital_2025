---
created: 2024-12-12T09:58:45
modified: '"2024-12-12 11:54", "4tc/G12T+6"'
date: 2024-12-12
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
2024-12-12

## Asistentes

### Cliente
* David Alejandro Romero - Arquitecto de DAV supongo
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
* Levantamiento de infraestructura
* Lineamientos de DevOps
* Accesos
* Comunicaciones
* 

## Puntos de Acción acordados
- Organizacion de recursos en cuentas y distribución de costos: #followup
	- Sandra dice no usar cuentas Shared
	- El objetivo es desplegar sus propias cuentas (3 para PER por ambiente (DEV,LAB,PROD), y 3 para Camara Compensacion (una por ambiente) - Total 6 cuentas
	- Las cuentas compartidas son por paises
	- Los porcentajes ya estan establecidos, tanto para la ejecucion, como para los consumos
		- Esta Tareas deberia ser de Nicolas. dice que ya se hizo
		- Colombia es la que va pagar mas.
		- Involucrar a FinOps?
		- Estrategia de Tagging??
	- Todos los componentes son una sola solucion...no se puede taggear por tasks.
	- El consumo lo debe gestionar la aplicacion 🚩
		- A futuro!! en este momento la estrategia debe ser fija
	- Sesion de Etiquetado #followup
	- Conclusion: sesiones nuevas, por ambiente (6 en total)
- Darwin Gabriel Arellano pide sesiones para revisar la infraestructura. Diferencias entre laboratorio y producción. #followup
	- Hay componentes que no son iguales entre ambientes (F5, etc..)
- Infraestructura de seguridad perimetral #followup ⚠ 🔺 🚩 🚩
	- Esto es administrado por Cyberseguridad Colombia


- Unidad organizativa Regional
	- Allí crear las cuentas
	- Definir el nombre de las cuentas

Principales actividades
1.  Definir mapa de dependiencias (conexiones)
	1. David Alejandro Romeri dice que ya existe un mapeo de dependiencias generales #actionpoint
	2. Se puede hacer diagramas más específicos segun sea requerido
	3. Son dos diagramas/sesiones: Uno de interrelacion de funcionalidades y flujos y otro de conectividad
	4. Se deberia empezar a trabajar con el de Single-Sign On
		1. Dependencia con el proveedor 

2. Herramienta de DevOps
	- Accesos: Jhonan y Francisoco aùn no tienen acceso al Tenant
	- Modulos
	- Pipelines
- Se solicita que se tenga alguna persona asignada de DevOps y Seguridad al proyecto

3. Lineamientos de seguridad #followup

- Definicion de Historias de Usuario con el analista funcional (Rerfinamiento de Backlog)
	- MC pide acceso a JIRA - en cual Jira #followup
	- MC tambien pide los prototipos
	- Con eso pueden empezar a volcar los HU


### Siguientes Pasos
1. Mapa de Dependencias
























## Proxima Reunión
*   

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
