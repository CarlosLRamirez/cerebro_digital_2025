---
type:
  - minuta
IDProyecto: emx-davivienda
date: 2024-09-02
modified: '"2025-01-10 14:51", "5tc/G1T+6"'
created: '"2024-12-16 08:13", "1tc/G12T+6"'
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
2024-09-02

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Lillibeth Alvarez
- Hector Martínez

## Agenda
* 
## Temas Discutidos


*  Magdalena:
	* Hay un tema que hasta Alejandro se metió
	* Lillibeth dice que Ingenio es que es 0 consola AWS, cualquier cosa que haya alli lo hicimos nosotros.
	* Hasta hace nada era el cliente que pagaba mas soporte de todo Escala
	* Lillibeth ha levantado muchas veces casos de mala practica.
	* El cliente le dijo que esta cansado de que algo, se lo hace Escala24x7????
	* Alejandro literal escribió: "Oscar Pedrozo de Ingenio Magadalena me esta buscando, hay una molestia con un par de tickets."
	* Cuanto facturan ellos? 36mil USD en servicios AWS
	* Ahora están un plan de 3 meses
	* El 31 de agosto hay un incremento en AWS Config.


![[Pasted image 20240902101015.png]]


![[Pasted image 20240902101021.png]]


![[Pasted image 20240902101028.png]]


![[Pasted image 20240902101107.png]]


![[Pasted image 20240902101117.png]]


Rol del CPSM:
- El Service Delivery Lead va hacer la asignación de los CPSM (Novys)
- Se mantienen con los clientes de Cloud EMX, pero Novys tiene que dar la indicación.
- 


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
