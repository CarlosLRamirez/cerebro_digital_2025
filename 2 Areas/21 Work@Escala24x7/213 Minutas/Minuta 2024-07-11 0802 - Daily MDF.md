---
type:
  - minuta
IDProyecto:
  - "10933"
modified: '"2025-01-10 14:19", "5tc/G1T+6"'
created: '"2024-07-11 08:02", "4tc/G7T+6"'
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
2024-07-11

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Despliegue del Contenedor
	* Alberth esta trabajando en el tema, probablemente se deba agregar una task
* Step Function (PR)
	* Se esta consultando con Carlos Calmo por tema de aprobadores, para poder incluir a alguien de la célula del equipo.
* Lambda generar póliza
	* Se va buscar un espacio hoy con Hilbert
* Creación de nuevos Repos
	* Hoy lo ve Alberth
* Generación de la póliza
	* Se modificó el contrato y se tuvo una reunión con los usuarios
* Lambda de S3
	* Pendiente que Alberth cree en repositorio
* Lambda Guardar
	* Anderson lo esta viendo con Ruth
* FrontEnd
	* Jean Paul esta buscando conseguir un FE, había uno pero ya no está disponible
	* Espera tener mas información para mañana. 
	* Mientras tanto podemos empezar a trabajar con los mockups.
	* La idea que tiene Anibal es diferente a lo actual de Escritorio BAM
	* Jean-Paul va reunirse con Anibal y Alberth para ver el tema de las pantallas.

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`