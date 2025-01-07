---
type: Minuta
IDProyecto: "11065"
date: 2024-10-08
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
2024-10-08

## Asistentes

### Cliente
* Carlos David Robayo
* Lina Milena Mantilla
* Luisa Fernanda Chilla
* Miguel Leonardo Chaparro
### Escala24x7
- Carlos Leonel Ramírez
-  Nelson Mora
- Alberto Madrid
- Iliana Estupinian

## Agenda
* Sync del proyecto
## Temas Discutidos
- Pipelines #issue #blocker 
	- Existe un fallo en los módulos (VPC, lambdas, etc..)
	- Ciber esta revisando los cambios para aprobarlos, luego nos indican que cambios debemos hacer nosotros en los módulos
	- Lina indica que el tema esta escalado en Davivienda y se espera tener respuesta esta semana
*  Tema Emojis quedan como caracteres especiales en el popup #issue
	* Todavia no esta
	* La ultima prueba que se lanzo la semana pasada, se incluyo desde SQL de una vez la codificación de los emojis
	* Debemos pasarle la prueba a Miguel (Canal) y validar si funcionó o no funcionó
	* La solucion propuesta es hacer un cambio que implica cambiar todo a HTML
		* El canal debería aplicar un renderizado HTML en los datos que recibe
	* [x] Nelson no apoye ambientar los datos nuevamente y pasarlos a Miguel #followup
	* [x] Pedir un espacio con Elda e involucrar un ingeniero de Escala24x7 #followup
		* Pedirle ejemplos de archivos que genera Excel o SQL, o buscar alternativas con Google Sheet -- ella lo hace con un software de banco, que lo envia directo a CSV 
*  Correo de Novedades #issue
	* No es consistente lo que dice el texto con las tareas exportadas
* Columna en el archivo de exportaciones #issue 
	* Se va necesitar otro campo de control
	* de MBaSS ya esta definido en la estructura, Nelson debe aplicar un cambio para guardarlo y que se refleje en la salida.



## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[20241231T0801 2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
