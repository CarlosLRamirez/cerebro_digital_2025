---
type: Minuta
IDProyecto: "11206"
date: 2024-11-19
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
2024-11-19

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  EC2
	* Control Center i-09af5c1762eec2995 ami-0d27167c0c3d1515b No  ✅
	* InfraServices i-0335640884543226d ami-0b4d8d6d928f28d2d No  ✅
	* Techlog i-0116482cf1dc2ab44 ami-04aed7f7fced5bfb5 No  ✅
	* CMM i-07e5c769888152dc6 ami-09fca5a52cfe9becb No ✅
* EC2 - ASG
	* Ebanking-Semilla  i-0250a61f9d2117ee7 ami-056b0c943fcd2500e Si ✅
	* Perfilamiento i-0f535079a014516bd ami-0d58b74cd7910aea6 Si ✅
		* en costa rica si esta con ASG, en las demas filiales no esta
* RDS
	* p01-belcronlinerds-p02

El de la discordia es Banking Server = SuperApp  
- Lleva grupo de auto-escalado? en este momento no tiene?
- Necesitamos ver cuando esto afecta la balanza en costo
- Oscar dice que en ASG se puede dejar en 1 solo instancia, o 0 en horas determinadas.
- SuperApp no tiene ASG en Costa Rica
	- Rol: App-BankingServer
	- ID en Prd: i-0d898eb17f3302a5e
- 



### Según Calculadora Jenny
- El servidor de NGINX es la EC2 no 25, pero esa ya no va...
## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
