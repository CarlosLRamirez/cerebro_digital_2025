---
type:
  - minuta
IDProyecto:
  - "10933"
modified: '"2025-01-10 14:18", "5tc/G1T+6"'
created: '"2024-06-24 07:59", "1tc/G6T+6"'
---
#minuta 
#id10933 

> Agregar aqui el resumen de follow ups del proyecto
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
2024-06-24

## Asistentes

### BAM
* Jean-Paul Magermans
* Diego Rodolfo Noj
* Alberth Isai Bautista
* Hilberth Josue Perucho
* Manuel Alejandro Hernandez
### Escala24x7
- Carlos Leonel Ramírez
- Ruth Ardon  

## Agenda
* Daily Sync Modulo de Facturación BAM
## Temas Discutidos
*  Despliegue de las 5 lambdas
	* Falta hacer unas pruebas de MAC y SENGRID 
	- [x] El viernes compartieron los links correspondientes, no se puede acceder desde la maquina local. Ruth propone hacer el despliegue de una vez hoy. #followup
* Contenedor XML
	* El viernes tuvieron una reunion Anibal, esta al 90%.
	* Faltan pruebas unitarias 
	* El servicio que los consume es el API Gateway de las 5 lambas.
* Lambda 50 Concurrencias
	* Se aclararon varias dudas sobre la lógica.
* Lambda Trigger CSV
	* No iniciada
* [x] Lambda Firmar URL S3 #followup
	* Esperando feedback de Anibal 
* Persona de QA
	* Se le esta dando onboarding,  y se empezará a integrar a los dias.
* El viernes y lunes es festivo para BAM 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

`