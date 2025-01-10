---
type:
  - minuta
IDProyecto:
  - "10933"
modified: '"2025-01-10 14:18", "5tc/G1T+6"'
created: '"2024-06-26 08:02", "3tc/G6T+6"'
---
#minuta 
#id10933 


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
2024-06-26

## Asistentes

### Cliente
* Carlos Andres Avila
* Manuel Alejandro
* Hilberth Perucho
* Alberth Bautista
### Escala24x7
- Carlos Leonel Ramírez
-  Anderson Ferreira
- Ruth Ardon

## Agenda
* Daily Modulo de Facturación
## Temas Discutidos
*  Despliegues de las 5 lambdas
	* Aun no se ha desplegado
	* 🚩 Inconvenientes: versiones de serverless, temas de tagging
	* Ayer logro pasar el pipeline en Azure DevOps y hoy el tema esta en AWS, hoy estarán revisando
* Lambda Autorización CSV
	* 90%
	* Consulta con Anibal sobre el tema del Secret
* Lambda Consulta Lotes
	* Hoy iniciar
* Lambda Concurrencia
	* Hoy sube Anderson lo ultimo
* Contenedor XML
	* El código ya esta 100%
	* Pendiente Despliegue del Contenedor
*  Balanceador
	* La plantilla traer un ALB
	* Alberth revisará el proceso
	* Se mencionó involucrar a Jonathan y Ronald de Escala 24x7
  

## Puntos de Acción acordados
*  

## Proxima Reunión
*   



  
=AND($H5<HOY()`