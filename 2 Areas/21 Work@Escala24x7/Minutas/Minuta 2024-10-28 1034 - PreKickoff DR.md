---
type:
  - Minuta
IDProyecto: "11221"
date: 2024-10-28
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
2024-10-28

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
- Riesgos
	- pruebas failover/failback
	- Seguridad perimetral
- Backlog inicial
	- Template Ohio
	- 
- Prerequisitos
	- VPC de Shared, y las de los ambientes (CIDR)
	- La seguridad permietra lista para que el equipo pueda hacer las pruebas
	- Ellos nos tienen que dar un cronograma de pruebas
	- 
	- 

Estrategias de DR (para los 4 paises)
1. RDS Nativo (Cross Region replication), si no se puede estrategia de Snapshot
2. Estrategia para autoescalado, una AMI diaria de la semillla para pasarla con Orbis a la otra region
3. DRS para lo demas
4. CMM no lleva DRMS
	- La instancia debe ser deplegada y configurada por Danvivienda

🚩 En algun punto va llegar Director a sustituir a CMM, ellos van a desplegar su DR (eso viene con ESC)

CMM: Manejador de colas (broker)

- Prueba piloto de Cyberbank configurando el default domain y DNS en cada servidor - Que lo metan como horas de soporte, instancias quemadas en el archivo de host.


## Proxima Reunión
*   

---
Template: [[20241231T0801 2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024
