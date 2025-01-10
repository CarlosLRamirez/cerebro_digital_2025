---
type:
  - minuta
IDProyecto:
  - "11118"
date: 2024-11-08
modified: '"2025-01-10 14:44", "5tc/G1T+6"'
created: '"2024-12-16 08:13", "1tc/G12T+6"'
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
2024-11-08

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  

## Puntos de Acción acordados
- ProjectID: 11118
- Automation Anywhere - Bots
- Arranco en Mayo de 2024
- Proyecto especial:
	- Iba ser un MAP, pero no era un MAP
	- Lo que se queria entrar en Davivienda Colombia, y quien habia ganado el proyecto era AE, nosotros entramos por atras, por la cocina, ellos nos estaban dando la apertura
	- Nosotros vamos a hacer el MAP (Migrate), Vamos a arrancar con la actualizacion de unos bots, y luego la migrar unos bots
	- AE queria los créditos de todo
	- Novys les decía que ella no sabia nada, que eso lo debian habla con Mafer
- Luego arranco el proyecto de Bancolombia
	- Ese si arranco mas rapido
	- Lo llevaba Novys y luego lo cedió a Jorland
	- Se estuvo dos meses trabajando con Bancolombia y AE
	- Ahi nos dimos cuenta que ellos nunca son los que dicen la capacidad que debe tener la capacidad que debe tener el servidor, esos generalmente se los da el cliente, ellos solo instalan en agentes.
	- La duda es, en que momento arrancamos nosotros?
	- Se hicieron una mesas donde AE está haciendo laboratorios, con ingenieros de Escala (Natasha, Jhon Blanco, Marko Lozano, Elbano, Carlos Moreno)
- El proyecto de Davivienda se arrancó
	- Estan haciendo el levantameitno de la información sobre los bots que se van a migrar
	- Ellos avisan de un dia para otro.
	- Esta semana han tenido tres reuniones, todas le chocaban a Novys
	- Iggy quiere que nosotrso participemos, pero quien deberia participar es alguien de arquitectura para estimar la infraestructura requerida.
	- Quienes instalan los agentes es el cliente
	- Ha participado Elbano y Erick directamente. Jenny participó en la generación del SoW para el MAP
	- No se sabe quien es el contacto de Davivienda, de AE el contacto es Antonio Marquez 

Organizar mejor:


## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
