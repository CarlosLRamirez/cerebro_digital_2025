---
type: Minuta
IDProyecto: "11073"
date: 2024-07-10
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
2024-07-10

## Asistentes

### Cliente
* Mario Hernandez Vargas
* Alexia Maria Molina
* Elizabeth Umana
* Jose Allan Rodríguez
* Kimberly Salas
* Maria Jose Guzman
* Wendy Quezada Brenes
* Kimberly de los Angeles
### Escala24x7
- Carlos Leonel Ramírez
-  Jose Ayala
- Ruth Ardon

## Agenda
* Presentación de Prototipos según las HU
## Temas Discutidos
*  La persona que crea las campañas actualmente es el Líder (Jose Pablo Cardenas), no los usuarios de NetRetail (Elizabeth Umana)
	* Según Mario Vargas, los usuarios de NetRetail (negocio) deberían crear las campañas.
	* Wendy Indica que hay campos que deben proveerlo TI (servidor, ip)
	* Según Mario eso lo proveerá TI
* [x] Lista de campañas por usuario? #followup
	* Actualmente esta general
	* Se podría implementar cuando se defina el IDP (login/autenticación) y los roles.
	* 🚩 Si existe la necesidad según los usuarios, de tener segmentación de roles 🚩
* [x] Detalle vs Bitacora de la campaña #followup
	* Son dos archivos diferentes
* [x] Incluir en la proxima sesión al equipo de infra, por la integración con SES ✅ 2024-08-20
* [x] Integración con GoAnywhere #followup


*  

## Proxima Reunión
*   

`