---
type:
  - proyecto
IDProyecto:
  - "11236"
statusProyecto:
  - activo
cssclasses:
  - wide-page
modified: '"2024-12-19 12:27", "4tc/G12T+6"'
tags:
  - Escala24x7
---

> [!multi-column]
>
>> [!tip]+ Do Today
>> ```dataview
>> TASK WHERE contains(tags, "#id" + this.IDProyecto) AND due < date(today) AND !completed AND !contains(tags, "#followup") AND !contains(tags, "#actionpoint")
>>```
>
>> [!abstract]+ Do Tomorrow
>> ```dataview
>>TASK WHERE contains(tags, "#id" + this.IDProyecto) AND due > date(today) AND !completed
>>```
>
>> [!warning]+ Follow UP
>> ```dataview
>>TASK WHERE contains(tags, "#id" + this.IDProyecto) AND contains(tags, "#followup") AND !completed
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
> 
- [Tablero Lucid](https://lucid.app/lucidspark/0c13aaf9-7c3c-44fb-ad3e-3c3bdd52c41a/edit?viewport_loc=-14768%2C-13287%2C30727%2C16089%2C0_0&invitationId=inv_d39e6337-0f68-42f9-9c4d-5a4dcc68e060)
- [Carpeta del Proyecto](https://drive.google.com/drive/folders/1QfM_Mt7q79Y5xz7BotpSMqktTmxFpnLe?usp=drive_link)
> - [Informe de Status](https://docs.google.com/presentation/d/1Rr4Kg0bZDKAAzw5VDje7zP-uvwWfhmmX3nbdEoelST0/edit?usp=sharing)
> - [Tablero Jira](https://escala24x7.atlassian.net/jira/software/c/projects/DACO/boards/1551/backlog)
> - [Diagrama de Arquitectura](https://lucid.app/lucidchart/0a23965f-6b60-493f-8d81-6a960ccde2bc/edit?viewport_loc=-4068%2C-2537%2C8911%2C6025%2C8PoB4jq7HZ-1&invitationId=inv_b1bff465-c58a-4563-ae29-e32ddb23ae4c)

> [!abstract]+ Calendario/Cadencias
> - Inicio de Sprint:  
> - Fin de Sprint: Domingo (Viernes)
> - Envío de Status Report: Viernes (15/03, 29/03, ...)
> - Cerrar Sprint en JIRA: N/A

---- 
# Apuntes


