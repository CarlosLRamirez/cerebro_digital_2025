---
type:
  - minuta
IDProyecto: "11152"
date: 2024-07-24
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
2024-07-24

## Asistentes

### Cliente
* Carlos Verbel
* Didier Giovanni
* Jose Miguel Jimenez
* Martha Isabel Mayo
* Pastor Fernando de los Rios
### Escala24x7
- Carlos Leonel Ramírez
-  Antonio Flores

## Agenda
* Daily célula BCOM
## Temas Discutidos
*  Estrategia de 2 olas o BigBang
	* El viernes Escala envió el documento con los pro/contras
	* Para tomar la decision dependemos de resolver los retos que tenemos, los resumimos en 4 retos.
	* Se espera tener resolución de esos retos antes del 15 de Agosto y la expectativa es que Connectria disponbilice la maquina 
* Se detendrá el salvado de Opción 21 el domingo (Nacional)
* El backup de SUFI si continua
	* Debe ser un domingo por las noches
* Accesos SUFI por Cyberark
	* Esta semana hablamos con Walter, Kindryl ya tiene usuario, Connectria debe tener otro usuario.
	* Catalina nos tiene que decir como hacerlo. 
	* Didier se lleva la tarea y lo consulta con Walter y Maria Elsy. (Kindryl)
* Direccionamiento Interno
	* 10.8 y 10.9 pero en calle 100 somos 10.60
	* Vamos a tirar la pregunta en el espacio con Cyber
* 


## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
