---
type: Minuta
IDProyecto: "11236"
date: 2024-11-22
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
2024-11-22

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Portal empresarial regional (PER)
* El proyecto buscar tener la parte regional de Davivienda (incluir Colombia y USA)
* 3 grandes hitos
	* Implementacion de la infraestructura dentro de la organizacion de Davivienda CAM
		* muy similiar a Whitelist
		* 🚩 Incluir a Alan: como vamos a distribuir los costos, taggig?
		* PER Produccion si consumio X, se divide en 6 filiales
		* La implementacion tambien se divide en 6
	* Desarrollo
		* Con Mobile Computing, la diferencia es que aqui Escala es la cara de lado de Davivienda
		* Nosotros somos los responsables
	* Soporte y Consumos de AWS
* Esta divido en tres fases
	* MVP:  la primera parte funcional
		* Luego vienen de los incrementos
		* 🚩 El MVP es uno solo.. no es por país (Solo se despliegua una sola vez)
		* Es un Portal regional que se integra con todos los CORE de los países.
	* Primer Incremento
		* Camara de compensacion
	* Segundo Incremento
		* La siguiente parte de PER: 
* Va ser largo
	* 18 meses aprox de alto nivel, según el cliente para las 3 fases
	* 🚩 tenemos ese cronograma? lo podriamos optimizar
	* Tiene 👀 por todos lados.
* El proyectos se trabajo con aprobaciòn de las altas gerencias
	* Fix price con base al alcance de la oferta técnica
	* Las horas estas super dimensionadas, uno de los que mas va consumir horas es el PM
	* MC va tener un scrum master con el que yo tengo que hablar
	* Todos somos un mismo equipo!
	* Porque contratamos a MC, porque no tenemos la capacidad de desarrollo



* Proyecto en JIRA Colombia?
* Horas:
	* Infra y acompañamiento (PM): 1600h
	* 
* Product Owner?
* PM de Davivienda
	* Nicolas Leon Perez  (nileon@davivienda.com)
* Stack:
	* FE: Angular
	* BE: 
* CI/CD:
	* Github Actions
	* Terraform
* Consumo privado, MBaSS lo expone
* Mobile Computing
	* Hacer un prekckoff con Mobiles
	* Martin, contacto desde la parte técnica
	* MC tiene una celulla completa de desarrolo


Next step
- Definir horas con Mafer
- Coordinar primer acercamiento con equipo de MC (pre kickoff)
- Hacer una RACI y definir gobernanza del proyecto (comunicaciones, escalaciones etc..) entre Escala y MC
- Kickoff con el cliente con el acompañamiento de MC



## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
