---
type: Minuta
IDProyecto: "11152"
date: 2024-07-10
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
2024-07-10

## Asistentes

### Escala24x7
- Carlos Leonel Ramírez
-  Camilo Villamil
- Antonio Florez

## Agenda
* 
## Temas Discutidos
*  Tema de Direccionamiento IP
	* Vamos con Direcciones IP diferentes en Connecftria. decision tomada
* Vamos en 2 olas con Nacional
	* 1er tiempo - Fiduciaria  (mediados octubre)
	* 2do tiempo --- + 30 App (principios noviembre)
	* 
![[../attachments/Pasted image 20240710080204.png]]
* Tenemos dos SoW (Fiduciaria y SUFI)
* SUFI (migrar 4 migraciones) -
	* 1 de Sufi: DEV, QA, PROD, y DR
	* [x] Buscar el SOW de SUFI 📅 2024-07-10 ✅ 2024-07-19
	* Validar storage de Sufi  ?? 
* Fiduciaria (Fue la que se probó en la POC)
	* Eso fue ampliando hasta llevarnos toda la LPAR de Nacional
	* En esa LPAR esta Fidu y aprox 40 aplicaciones más
	*  Necesitamos 130Tb de arranque (pero Sufi no ocupa los 130TB) (Producción y DR)
	* 🚩 Almacenamiento 🚩
* Diagrama general ![[../attachments/Pasted image 20240710073839.png]]
- Los costos de la maquina para el appliance  para el SD-WAN no estan incluidos
- El banco no ha entregado el diseño final de comunicaciones. 
- Plan de comunicaciones
	- Daily interna 8:30am (Antonio, Camilo, AP)
	-  Hay una sesión diaria con Josh a las 11am (Connectria y Bancolombia)
	- Antonio tiene sesiones en su celula dentro de Bancolombia (Daily)
	- [x] Responder correo de Cesar #followup ✅ 2024-07-19



`