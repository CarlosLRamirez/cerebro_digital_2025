---
created: 2024-12-18T10:01:03
modified: '"2025-01-06 10:00", "1tc/G1T+6"'
date: 2024-12-18
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - 11245-swift
---
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
2024-12-18

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Francisco Brito
- Iliana Estupinian
- Maria Fernanda Juarez
- Nelson Mora
- Oscar Romeo Ramírez

## Agenda
* 
## Temas Discutidos
- Resumen del Proyecto
	- mensaje a travez de GoAnywhere para su posterior transferencia a la plataofrma final
	- DEspliegue de la infraestructura: Desarrolo Laboratorio y Produccion
	- Desarrollo de componentes de Back y Frontend
	- Funcionalidaades
		- Canje
		- Tesoreria
		- Comext
* Roles:
	* Se intentó copiar los roles de MC
	* Analista Tecnico: Levantar requerimientos (no identificado)
	* Líder Técnico: No identificado
	* Backend: Osmar Romeo Ramirez
	* Infraestructura: Francisco Brito
	* Front End: Ruth Ardon 
	* UI/IUX: Jose Ayala
	* QA: Nosotros probamos  (no identificado)
* Horas
	* 3 meses
	* 1850 horas
	* cuadro de estimación
* % de allocation
	* solo es referencia
- HUs
	- importante!!! ⚠ 🚩 
* Davivienda Costa Rica
	* Va dentro de la organización de CAM
* No se expone publicamente
	* Conectividad parecida a NetRetail
	* Se consume desde on-premise (usuarios por VPN)
* Autenticación
	* La aplicación debe tener un modulo para autenticar los usuario 💡❓
* CI/CD
	* Terraform
	* Azure DevOps (No Github) -- lo evaluamos si no lo trabajamos con lineamentos regional 💡 ❓ o servicios AWS CodeX
	* Pedir lineamientos, si no nosotros ponemos la referencia
- Kickoff con Kimberly
- Tagging??


## Puntos de Acción acordados
- [ ] Leer y compartir documento tecnico - Scope Swift - V3 #id11245 📅 2024-12-30


## Proxima Reunión
*   

---
