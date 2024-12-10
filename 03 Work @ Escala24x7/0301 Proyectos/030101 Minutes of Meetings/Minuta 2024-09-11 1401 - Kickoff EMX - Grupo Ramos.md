---
type: Minuta
IDProyecto: "11152"
date: 2024-09-11
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
2024-09-11

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Jhon Asuaje - Operaciones
- Robert Santos
- Nelson Mora
- Luis Palacios

## Agenda
* 
## Temas Discutidos
* Grupo Ramos
* 2 cuentas (2 organizaciones)
* Usuario tipo Ultra
* Tienen Ples
* 50 horas contratadas
* TAM:
	* Pendiente definir si es Carolina Madera o KEvin Molina

- El mayor retailer en Dominincana
- Infra en:
	- AWS
	- On premise
	- Azure
- Noostors arrancamos con workspaces
- lo que tenian con el otro partner (carga sap, mas otras cuentas (networking, base de datos) y otra cuenta que tambien viene (sirena go)), esas son las cuentas que notros vamos a manejar con ellos
- Uno de los aspectos principales que tenemos que arrancar eso
	- Meejorar la arqutiectura
	- rightiszing
	- aplicar instancias reservadas
- Proyectos que vamos a arrancar
	- Cloud Foundation. ya estan los fondos, no lo podemos arrancar hasta que tengamos la vision bien clara
	- Datalace
	- Poc
		- Quicsksing
		- Demand Forectas
		- Evaluacion Canastas
	- PPA* deberia estar antes o despues del Cloud Fondation
	- Ya hicimos un MAP Assess. definimos unas olas de migración, seria parte del contrato de PPA (migracion de carga en premisas)
		- El MAP incluye el Cloud Fondation, el Datalake y un par de PoC
	- Tenemos que organizarlo como proyectos
	- Necestamos centralizar la gestiòn de esto, como tiene que ser
- Evaluacion de Canastas ya tiene un trabajo del equipo de Data
- No hay proyecto activo en este momento
- Jorge Encarnacion comentario:
	- El partner anterior tenia alguna interaccion con GBM en temas de SAP
	- Que lo definamos en la primera presentacion con ellos
	- entender si ellos requieren algo de nosotros con otros proveedores
- 
![[../attachments/Pasted image 20240911140645.png]]

![[../attachments/Pasted image 20240911141428.png]]

![[../attachments/Pasted image 20240911141452.png]]

![[../attachments/Pasted image 20240911141621.png]]

- :ojo: politicas de taggeo, encendido automatico

![[../attachments/Pasted image 20240911141939.png]]

![[../attachments/Pasted image 20240911141943.png]]

![[../attachments/Pasted image 20240911142003.png]]

- Assessment de seguridad
- Etiquetado: Definir politica
- 
## Siguiente Pasos
- Definir el TAM
- Rober santos enviara un correo al cliente, para definir fecha del kickoff
- EMX - Sessiones multidiciplinarias

## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
