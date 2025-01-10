---
type:
  - minuta
IDProyecto: "11152"
date: 2024-08-28
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
2024-08-28

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
- 
![[Pasted image 20240828144326.png]]

- [x] Coordinar ventanas con anticipacion #id11152
 - [x] Tema de los usuarios #id11152
- Tratemos que en septiembre ya tengamos todo

Post-reunion: Sync con Antonio

- Necesitamos decirle a Connectria si llevamos las cintas el 9, que el 10 y 11  creen las maquinas.
- Si logramos tener  la maquina el 12, SUFI puede crear el delta con Mimix para el 20
- Antonio ve viable que el cutover sea en Septiembre
- Nacional: Presionar ventana de backup el 9 (data de usuarios)
	- Que se vaya por VTL (presionar a Pastor - Maria Elsy)
	- 


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024



```
interface range fa0/21-24
no switchport trunk native vlan 10
no switchport trunk allowed vlan 2-4
```