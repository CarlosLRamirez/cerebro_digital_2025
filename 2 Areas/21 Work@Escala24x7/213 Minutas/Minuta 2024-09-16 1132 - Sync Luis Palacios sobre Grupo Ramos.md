---
type:
  - minuta
IDProyecto: EMX-Grupo Ramos
date: 2024-09-16
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
2024-09-16
## Asistentes

### Escala24x7
- Carlos Leonel Ramírez
-  Luis Palacios

## Agenda
* 
## Temas Discutidos

Grupo Ramos
- Nosotros hicimos un MAP Assess muy Light
	- No hubo MRA
	- No hubo sesiones de intercambio
	- Solo recibimos un inventario con excel, no se instaló herramienta
	- No hubo interacción con el cliente practicamente
	- La interacción ha sido entre comercial y AWS
	- AWS esta empujando mucho por este cliente
	- Ellos tenian sus cuentas con otro Partner, se transfiró el token a Escala24 con la promesa de hacer un PPA
	- La transferencia de cuenta ya se hizo
- Y se aceleró mas el hecho del cambio al MAP 3.0
- AWS a sido participe y ha impulsado todo esto con el cliente
- El ciliente tiene la particularidad de que vino por un evento de seguridad que no se tiene mas detall (perdida de información)
- Se inició con un proyecto de Workspace para darles maquinas a los consultores externos, eso ya se hizo, el proyecto ya se entrego (50 Workspaces aprox)
- Ahora tenemos
	- Una PoC de Quicksite
	- Análisis de cesta: sin un cliente compra mantequilla, probablemente compre harina y leche, a veces son estacionales. Se hizo un análisis que ni siquiera va por ML sino es mas básico, Eso lo esta haciendo Jose Vasquez, eso ya se facturó.. fueron unas horas de consultoria.
- Lo que queda por organizar, es el tema de Mobilize, hay una aprobaciòn de 200,000 dolares (2300 dolares aprox.)
	- Cloudfoundation, agregando las cuentas stand-alone que tienen ahorita
	- 2 o 3 PoC que están alli
- Luis le dice a Robert que no hagamos el mobilize como hicimos el Assess, se hizo sin la participación de la PMO
- El cliente no es muy dado a reunirse
- Se le han hecho muchas cosas, IMMD, Seattle, en este punto ya deberia haber confianza
- El PMO debe sentarse con Luis y con el cliente, y llevarlo como tiene que llevarse
- Pedro es AWS, Robert es el Account Manager

Que debemos hacer
- Arrancar un Proyecto


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
