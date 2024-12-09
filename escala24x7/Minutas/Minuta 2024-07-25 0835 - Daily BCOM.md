---
type: Minuta
IDProyecto: "11152"
date: 2024-07-25
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
2024-07-25

## Asistentes

### Cliente
* Pastor de Los Rios
* Carlos Verbel
### Escala24x7
- Carlos Leonel Ramírez
-  Antonio Flores

## Agenda
* Daily BCOM
## Temas Discutidos
- [x] Redes ✅ 2024-08-20
* Mascara /24
* Pastor debe entregar la información
* [x] (SUFI) Configuración de Mimix #followup
* Tener una sesión de verificación para empezar a definir las acciones a tomar.
* Hay un tema SLA con otro proveedor.
* [x] Cyberark usuarios Connectria #followup
* Debemos verlo con Didier (Catalina Botero)
* Debe ser usuario banco? `@bancolombia.co`
- [x] SUFI RMM VPN #followup
- Podemos natear las redes de Connectria?
- [x] Accesos para equipo Escala/Connectria #followup
- Necesitamos validarlo con el equipo Connectria



## Puntos de Acción acordados
*  

## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
