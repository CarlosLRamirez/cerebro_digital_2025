---
type:
  - proyecto
IDProyecto:
  - "11073"
statusProyecto:
  - activo
cssclasses:
  - wide-page
tags:
  - Escala24x7
modified: '"2024-12-31 10:57", "2tc/G12T+6"'
---

> [!multi-column]
>
>> [!tip]+ Do Today
>> ```dataviewjs
>>let projectID = dv.current().IDProyecto;
>>
>>// Función para filtrar tareas según las condiciones comunes
>>function filterTasks(tasks) {
>>   return tasks
>>        .where(t => !t.tags.includes("#followup"))
>>        .where(t => !t.tags.includes("#backlog"))
>>     .where(t => !t.completed)
>>        .where(t => t.due && t.due <= dv.date("today"));
>>}
>>
>>// Obtener todas las páginas que tienen tareas relacionadas con el ID del proyecto
>>let tasksByProperty = filterTasks(dv.pages().where(p => p.IDProyecto === projectID).file.tasks);
>>
>>// Obtener todas las tareas que tienen el tag del ID del proyecto
>>let tasksByTag = filterTasks(dv.pages().file.tasks.where(t => t.tags.includes("#id" + projectID)));
>>
>>// Combinar ambas listas de tareas y eliminar duplicados usando un Set
>>let combinedTasks = [...new Set([...tasksByProperty, ...tasksByTag])];
>>
>>// Mostrar la lista de tareas
>>dv.taskList(combinedTasks, { asOf: dv.date("today") });
>>```
>
>> [!abstract]+ Do Tomorrow
>> ```dataviewjs
>>let projectID = dv.current().IDProyecto;
>>
>>// Función para filtrar tareas según las condiciones comunes
>>function filterTasks(tasks) {
>>   return tasks
>>        .where(t => !t.tags.includes("#followup"))
>>        .where(t => !t.tags.includes("#backlog"))
>>     .where(t => !t.completed)
>>        .where(t => t.due && t.due > dv.date("today"));
>>}
>>
>>// Obtener todas las páginas que tienen tareas relacionadas con el ID del proyecto
>>let tasksByProperty = filterTasks(dv.pages().where(p => p.IDProyecto === projectID).file.tasks);
>>
>>// Obtener todas las tareas que tienen el tag del ID del proyecto
>>let tasksByTag = filterTasks(dv.pages().file.tasks.where(t => t.tags.includes("#id" + projectID)));
>>
>>// Combinar ambas listas de tareas y eliminar duplicados usando un Set
>>let combinedTasks = [...new Set([...tasksByProperty, ...tasksByTag])];
>>
>>// Mostrar la lista de tareas
>>dv.taskList(combinedTasks, { asOf: dv.date("today") });
>>```
>
>> [!warning]+ Follow UP
>> ```dataviewjs
>>let projectID = dv.current().IDProyecto;
>>
>>// Función para filtrar tareas según las condiciones comunes
>>function filterTasks(tasks) {
>>   return tasks
>>        .where(t => t.tags.includes("#followup"))
>>        .where(t => !t.tags.includes("#backlog"))
>>     .where(t => !t.completed)
>>        
>>}
>>
>>// Obtener todas las páginas que tienen tareas relacionadas con el ID del proyecto
>>let tasksByProperty = filterTasks(dv.pages().where(p => p.IDProyecto === projectID).file.tasks);
>>
>>// Obtener todas las tareas que tienen el tag del ID del proyecto
>>let tasksByTag = filterTasks(dv.pages().file.tasks.where(t => t.tags.includes("#id" + projectID)));
>>
>>// Combinar ambas listas de tareas y eliminar duplicados usando un Set
>>let combinedTasks = [...new Set([...tasksByProperty, ...tasksByTag])];
>>
>>// Mostrar la lista de tareas
>>dv.taskList(combinedTasks, { asOf: dv.date("today") });
>>```

--- 

> [!multi-column]
> 
>>[!Example]+ Backlog
>> ```dataviewjs
>> let projectID = dv.current().IDProyecto;
>>
>> // Función para filtrar tareas según las condiciones comunes
>> function filterTasks(tasks) {
>>    return tasks
>>         .where(t => !t.tags.includes("#followup"))
>>       .where(t => t.tags.includes("#backlog"))
>>       .where(t => !t.completed);
>>         //.where(t => t.due && t.due > dv.date("today"));
>>}
>> 
>> // Obtener todas las páginas que tienen tareas relacionadas con el ID del proyecto
>>let tasksByProperty = filterTasks(dv.pages().where(p => p.IDProyecto === projectID).file.tasks);
>> 
>> // Obtener todas las tareas que tienen el tag del ID del proyecto
>>let tasksByTag = filterTasks(dv.pages().file.tasks.where(t => t.tags.includes("#id" + projectID)));
>> 
>>// Combinar ambas listas de tareas y eliminar duplicados usando un Set
>> let combinedTasks = [...new Set([...tasksByProperty, ...tasksByTag])];
>> 
>>// Mostrar la lista de tareas
>> dv.taskList(combinedTasks, { asOf: dv.date("today") });
>>```
>
>>[!Danger]+ Risks
>> ```dataviewjs
>> let projectID = dv.current().IDProyecto;
>>
>> // Función para filtrar tareas según las condiciones comunes
>> function filterTasks(tasks) {
>>    return tasks
>>         .where(t => t.tags.includes("#risk"))
>> 
>>       .where(t => !t.completed);
>> 
>>}
>> 
>> // Obtener todas las páginas que tienen tareas relacionadas con el ID del proyecto
>>let tasksByProperty = filterTasks(dv.pages().where(p => p.IDProyecto === projectID).file.tasks);
>> 
>> // Obtener todas las tareas que tienen el tag del ID del proyecto
>>let tasksByTag = filterTasks(dv.pages().file.tasks.where(t => t.tags.includes("#id" + projectID)));
>> 
>>// Combinar ambas listas de tareas y eliminar duplicados usando un Set
>> let combinedTasks = [...new Set([...tasksByProperty, ...tasksByTag])];
>> 
>>// Mostrar la lista de tareas
>> dv.taskList(combinedTasks, { asOf: dv.date("today") });
>>```

> [!Example]+ Minutas
> ```dataview
> LIST
> where type = "Minuta"
> where IDProyecto = this.IDProyecto
> ```

> [!NOTE]+ Enlaces importantes
> 
> - [Carpeta del Proyecto](https://drive.google.com/drive/folders/1f_pl9NjN9ZPFGCo-sBR3EZKUdenrbytD?usp=sharing)
> - [Informe de Status](https://docs.google.com/presentation/d/1Rr4Kg0bZDKAAzw5VDje7zP-uvwWfhmmX3nbdEoelST0/edit?usp=sharing)
> - [Tablero Jira](https://escala24x7.atlassian.net/jira/software/c/projects/DACR/boards/733)

> [!abstract]+ Calendario/Cadencias
> - Inicio de Sprint:  
> - Fin de Sprint: Domingo (Viernes)
> - Envío de Status Report: Viernes (15/03, 29/03, ...)
> - Cerrar Sprint en JIRA: N/A

---- 
# Apuntes




======
Features de alto impacto:

- Segmentación de Data por Roles (Alto)
	- Eso es un modulo de seguridad completo
- Correo remitente, Correo de retorno (Medio)
	- El remotente implica desarrollo
- Reitentos
	- Lo tnemos si lo queren por ecampaña tambien tiene ipoact.
- Adutoria e accioens del suario
	- Deben ir a cloudwatch

====



====


--------



