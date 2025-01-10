---
type:
  - minuta
IDProyecto: "11065"
date: 2024-10-15
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
2024-10-15

## Asistentes

### Cliente
* Carlos David Robayo
* Julian Alberto Mejia (Scrum Master remplazo de Lina durante vacaciones)
* Migule Leonardo Chaparro
* Lina
### Escala24x7
- Carlos Leonel Ramírez
-  Alberto Madrid
- Iliana Estupinian
- Nelson Mora

## Agenda
* Sync Semanal
## Temas Discutidos
*  Tema Pipelines
	* Con el último repositorio que nos dio Andres, podemos ver el ejemplo
	* El parámetro de arquitectura, solo aplica para el módulo de Lambda
	* Iliana va hacer las modificaciones y nos notifica
* Despliegue en Laboratorio
	* Carlos Robayo pregunta si podemos hacer los despliegues en laboratorio?
	* Una vez desplegado, compartir los datos de infra que compartilo Nelson pero en Laboratorio.
* Ajustes en Integración
	* 1. Correos electróncios:
		* Nelson ya hizo los cambios 
		* Deben verse reflejados en las cargas de mañana
	* 2. Emojis (Caracteres especiales)
		* Se descubrió cuando se pierden los emojis en MSSQL (Colate)
		* En las pruebas en local, no hubieron problemas
		* Hoy nos dimos cuenta que en el servidor donde están los datos, no tiene todos los collates que se requieren, sin embargo si exporta bien los emojis.
		* Elda sigue haciendo pruebas. 
	* 3. Discrepancia en cantidad y nombres de de registros importados
		* Ya se hicieron correcciones
		* Estamos esperando el despliegue del pipeline
		* Seria bueno tener un despliegue desde los repositorio
	* 4. Correo con direcciones IPs de ENIS y nombre 
		* Ya Nelson respondió el correo



## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
