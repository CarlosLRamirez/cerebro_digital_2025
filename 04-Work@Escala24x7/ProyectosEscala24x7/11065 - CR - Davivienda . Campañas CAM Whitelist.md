---
type:
  - proyecto
IDProyecto:
  - "11065"
statusProyecto:
  - activo
cssclasses:
  - wide-page
modified: '"2024-12-19 13:33", "4tc/G12T+6"'
tags:
  - Escala24x7
---

> [!multi-column]
>
>> [!tip]+ Do Today or Overdue
>> ```dataview
>> TASK WHERE contains(tags, "#id" + this.IDProyecto) AND due <= date(today) AND !completed AND !contains(tags, "#followup") AND !contains(tags, "#actionpoint")
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
> - [Carpeta del Proyecto](https://drive.google.com/drive/folders/1iaRCmBPOL5A-4f7GA1GUQtvYlC0cMqFK?usp=drive_link)
> - [Informe de Status](https://docs.google.com/presentation/d/1Rr4Kg0bZDKAAzw5VDje7zP-uvwWfhmmX3nbdEoelST0/edit?usp=sharing)
> - [Tablero Jira](https://escala24x7.atlassian.net/jira/software/c/projects/DACR/boards/733)
> - [Tablero Lucid](https://lucid.app/lucidspark/841a6a6f-4bde-4cc3-b43b-6ea34a6b5229/edit?viewport_loc=-21139%2C-28755%2C20201%2C10578%2C0_0&invitationId=inv_fee142cb-a741-453f-9163-fe6a90650c7e)
> - [[👷 Work@Escala24x7]]


> [!abstract]+ Calendario/Cadencias
> - Inicio de Sprint:  
> - Fin de Sprint: Domingo (Viernes)
> - Envío de Status Report: Viernes (15/03, 29/03, ...)
> - Cerrar Sprint en JIRA: N/A

---- 
# Apuntes

## Items abiertos

https://docs.google.com/spreadsheets/d/1PfjGHykV6l9DNL11K-NruCR8RIJ2Vwhx87sBqFieQlo/edit?usp=sharing



## Items Cerrados
- [x] Comunicación desde SuperAPP luego del re-despliegue del ambiente DEV #followup #id11065 ✅ 2024-12-16
	- 20/Nov: Necesitamos tener sesión con Technysis para ver tema de connectiividad, junto con Jhonathan Muñoz, el cree que son rutas del lado de Azure #
- [x] Reorganizacion de Codigo a peticion de CybarSeguridad Jose Miguel Vanegas #followup #id11065 ✅ 2024-12-16
	-  19/Nov: Iliana lo esta trabajando, dijo que era cuestion de un dia, dar seguimiento 
- [x] Ultimos ajustes de Desarrollo #id11065 #followup ✅ 2024-12-16
	- 19/Nov: Nelson dice que son solo ajustes cosmeticos, dar seguimiento 
- [x] Error de Comunicación con GoAnywhere #followup ✅ 2024-12-16
	- 19/Nov: Lina se llevó el tema, dar seguimiento



--------
