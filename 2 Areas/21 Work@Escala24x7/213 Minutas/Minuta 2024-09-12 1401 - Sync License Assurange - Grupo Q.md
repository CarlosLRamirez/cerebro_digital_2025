---
type:
  - minuta
IDProyecto: "11189"
date: 2024-09-12
modified: '"2025-01-09 14:59", "4tc/G1T+6"'
created: '"2024-12-16 08:13", "1tc/G12T+6"'
---
#minuta 
#id11189

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
2024-09-12

## Asistentes

### License Assurance
* Adonay Artigas
### Escala24x7
- Carlos Leonel Ramírez
-  Raul Aquino
- Jenny Rodriguez
## Agenda
* Sync con License Assurance
## Temas Discutidos
*  El cliente esta asignado por Cloudamize
	* El documento lo generó
	* El cliente esta muy intersado el cliente en una migracion de 16 y 20 servidores, pero tiene un ecosistema mas grande (mas de 150 servidores)
	* Cloudamize puede reflejar la dependencia a nivel de aplicacion y ME lo puede hacer a nivel de red.
* Todo es on-premise
* Ellos vienen referenciado por Amazon
* Para los dos es un cliente nuevo
* Participación de License Assurance:
	* Que nos acompañen desde el kickoff
	* Explicar el proceso
	* Que nos ayuden con la instalacion y enrolamiento de los servidores
	* Analisis de Licencias, etc..
	* Entrega de clase de negocio
	* Opcional: tambien puede presentarle al cliente
* La herramienta tiene dos metodologias, con agente y sin agente
	* La opción sin agente tambien muestra el mapeo de aplicacones
	* La instalaciòn con agente es mas fácil
* Base deDatos
	* SQLServer ?
	* Vamos a necesitar el NMS, importante tenerlo antes de la fecha final de recopilación.
	* En el inventario hay 5 base de desatos (SQL Server 2017/2019)
* Cloudamize no trabaja con hipervisor

## Next Steps
- Pedirle disponiblidad del cleinte y luego agendar con Adonai
- https://outlook.office365.com/book/LicensingAssuranceLLC@NETORG686527.onmicrosoft.com/

![[imagen.png]]


![[Pasted image 20240912141555.png]]

https://support.cloudamize.com/kb/installation-troubleshooting

https://support.cloudamize.com/kb/installation-troubleshooting

https://support.cloudamize.com/kb/installation-troubleshooting


[bryan.aquino@escala24x7.com](mailto:bryan.aquino@escala24x7.com "mailto:bryan.aquino@escala24x7.com")


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
