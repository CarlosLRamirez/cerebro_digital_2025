---
type: Minuta
IDProyecto: "10854"
date: 2024-08-13
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
2024-08-13

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Jhonatan Muñoz
- Jose Abzum
- Gerardo Calderon
- Juan Pedro Gonzalez

## Agenda
* Sync Interno equipo BAM
## Temas Discutidos
*  **Lift & Shift**
	* Vemos dos servidores replicando (1 de 1TB), ya esta listo para testing para testing, el segundo
	* Siguen instalando agentes
	* El servidor sigue en testing, Williams tiene que delegarlo al equipo para que hagan pruebas.
	* Ya hicimos la sesión para mostrarles el proceso de pasar a testing.
* **Storage**
	* Jhonatan tuvo una sesión el viernes, esta trabajando en el Cloudformation para FSX, no se va dejar con CI/CD, solo se les va entregar el CloudFormation, esta semana ETA para entregar el Stack Set.
	* 🚩 Ellos tienen la tarea de crear una cuenta de servicio en su AD 🚩🚩
	* Next Step: La idea es que luego se conecte al AD de ellos, y mostrar que se conecten a otro servidor y que creen la unidad de FSX, probarlo con recurso de ellos.
* **Modernización**
	* AppRuteo y ConsumoNAS ya se envió email para que hagan pruebas de funcionalidad
	* Marcajes:
		* En la sesión van a ubicar a las personas que conocen la aplicación para ver la funcionalidad. 🚩
		*  Tanto el API como el FO son publicas, Cempro va investigando para corregir esa deuda técnica, se va evaluar si esto puede ser realizado desde el Load Balancer.
		* La documentación ya esta avanzada.
		* En QA solo esta desplegada la Infra.
	* Ayer se hizo un cambio en el DNS Resolver (Cempro estan haciendo pruebas en TEST -QA-, para ver si impacta )
* **Seguridad**
	* Gerardo esta trabajando en una plantilla que desplegó Dennys Tezen, eso es para la aplicación de AppRuteo y para Marcajes donde se va aplicar ese WAF.
	* Se va desplegar en todas las cuentas, y tambien para cognito.
* 

## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
Template: [[20241231T0801 2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
