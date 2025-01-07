---
type:
  - proyecto
IDProyecto:
  - "11236"
statusProyecto:
  - activo
cssclasses:
  - wide-page
modified: '"2025-01-02 09:34", "4tc/G1T+6"'
tags:
  - Escala24x7
---
## Tareas y Puntos de seguimiento

> [!multi-column]
>
>> [!tip]+ Do Today or Overdue
>> ```tasks
>>not done
>>(due today) OR (due before today)
>>tag includes #id11236
>>```
>
>> [!abstract]+ Do Tomorrow
>> ```tasks
>> not done
>> due AFTER today
>> tag includes #id11236 
>> ```
>
>> [!warning]+ Follow UP
>> ```tasks
>> not done
>> (tag includes #id11236) AND (tag includes #followup) 
>> ```

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
>> ```tasks
>> not done
>> (tag includes #id11236) AND (tag includes #risk) 
>> ```

> [!Example]+ Minutas
>```dataview
>LIST
>where  contains(type, "minuta" )
>where IDProyecto = this.IDProyecto
>```

## Enlaces 

> [!NOTE]+ Enlaces importantes> 
> - [Tablero Lucid](https://lucid.app/lucidspark/0c13aaf9-7c3c-44fb-ad3e-3c3bdd52c41a/edit?viewport_loc=-14768%2C-13287%2C30727%2C16089%2C0_0&invitationId=inv_d39e6337-0f68-42f9-9c4d-5a4dcc68e060)
>  - [Carpeta del Proyecto](https://drive.google.com/drive/folders/1QfM_Mt7q79Y5xz7BotpSMqktTmxFpnLe?usp=drive_link)
> - [Informe de Status](https://docs.google.com/presentation/d/1Rr4Kg0bZDKAAzw5VDje7zP-uvwWfhmmX3nbdEoelST0/edit?usp=sharing)
> - [Tablero Jira](https://escala24x7.atlassian.net/jira/software/c/projects/DACO/boards/1551/backlog)
> - [Diagrama de Arquitectura](https://lucid.app/lucidchart/0a23965f-6b60-493f-8d81-6a960ccde2bc/edit?viewport_loc=-4068%2C-2537%2C8911%2C6025%2C8PoB4jq7HZ-1&invitationId=inv_b1bff465-c58a-4563-ae29-e32ddb23ae4c)
> - [RAID LOG](https://docs.google.com/spreadsheets/d/1d_elL-W5sRhfpDWoLm_8fQopYCPJsZcJYY1ySIFu_Kg/edit?usp=sharing)

## Información General

> [!abstract]+ Calendario/Cadencias
> - Inicio de Sprint:  
> - Fin de Sprint: Domingo (Viernes)
> - Envío de Status Report: Viernes (15/03, 29/03, ...)
> - Cerrar Sprint en JIRA: N/A

---- 
## Otros Apuntes

### Mi bitácora del proyecto
- 10/Dic: Diciembre Frank Dirigió dirigió el kickoff con el cliente ya que yo estaba de vacaciones
	- [[Minuta 2024-12-12 094303 - Sync con Frank]]
- 12/Dic Diciembre se tuvo la primera sesión formal con el cliente 
	- [[Minuta 2024-12-12 095845 - Primera Sesion de Trabajo con Davivienda]]
	- https://app.read.ai/analytics/meetings/01JGKZT47M4NZA1RAGJN6N00XX
- 12/Dic: Se creó el canal de Slack con MC
- 13/Dic: Nicolas creo los chats de Google Space entre Escala/Davivienda/MC
- 16/Dic: Se tuvo una sesión interna entre Escala y MC: Yo/Frank/Sergio Bonanno/Juan Galeano
	- [[Minuta 2024-12-16 105033 - Sync PMs con Mobile Computing]]
	- https://app.read.ai/analytics/meetings/01JF7WYD8KB4ZPPV7SAH2KZR2G?utm_source=Share_Nav
	- Fue la entrega de Frank, ya no volvió a participar en el proyecto
- 16/Dic: Sesión con Nicolas, PM de Davivienda
	- [[Minuta 2024-12-16 Sync con PM Davivienda -11236 PER]]
	- Se agendarón las sesiones de "Empalme diario (excepto lunes)"
- 16/Dic: Enviamos a Nicolas los usuarios para el acceso a los prototipos ✋ via Google Chat
- 17/Dic: **Primera sesión** de Empalme diario
	- https://app.read.ai/analytics/meetings/01JFAEHVH5TM1X7QVQWR5DYGJ6?utm_source=Share_Nav
	- [[Minuta 2024-12-17 080219 - 11236 PER Empalme diario - revision de HU - sesion 1]]
- 17/Dic: Nicolas envió la nueva versión de las Historias de Usuario:
	- Subject: Correo informativo: Historias de Usuario PER Estructural - 11236
- 18/Dic: Sergio reportó que aún no tiene acceso a los prototipos, se pidió una sesión para ver este tema, pero luego pidió que se desestimara
- 18/Dic: **Segunda sesión** de Empalme Diario
	- [[Minuta 2024-12-18 080437 - Empalme PER]]
	- https://app.read.ai/analytics/meetings/01JFD10R5XRDPEVDMR6E9JQQR8?utm_source=Share_Nav
	- En esta sesión ofrecieron tener los diagramas de flujo para el 3 de enero
- 19/Dic: **Tercera sesión** Empalme Diario
	- [[Minuta 2024-12-19 082640 - Empalme Diario PER]]
	- https://app.read.ai/analytics/meetings/01JGM7GS262M5VSBGSKJ0ZBSRZ?utm_source=Share_Nav
- 20/Dic: **Cuarta sesión** Empalme Diario
	- [[Minuta 2024-12-20 080205 - 11236 - Empalme diario PER]]
	- https://app.read.ai/analytics/meetings/01JFJ5YH8AAZ0RGZBZJRNVXXKN?utm_source=Share_Nav
- 20/Dic: Envié un correo a Nicolas solicitando las  HU faltantes, según Sergio
	- Subject:  11236 PER - Nuevas HU vs Alcance MVP
- 23/Dic: Sesión Sync Semanal PMs 
	- [[Minuta 2024-12-23 110720 - Sync PMS]]
- 23/Dic: Sergio envío la propuesta inicial de cómo estructuraríamos las entregas.
	- ![[Pasted image 20250102122520.png]]
- 26/Dic: **Quinta** Sesión de Empalme Diario PER
	- [[Minuta 2024-12-26 123015 Empalme PER]]
	- https://app.read.ai/analytics/meetings/01JG1M5E6ZNS0A3HWC3P32Z3P1
- 26/Dic: tuvimos la sesión interna entre Escala y MC, para revisar la matriz RACI
- 27/Dic: **Sexta** Sesion de Empalme Diario PER
	- [[Minuta 2024-12-27 080112 - Empalme PER 11236]]
	- https://app.read.ai/analytics/meetings/01JG46GXCCAHGJAZBM8FQ1S2T5
- 30/Dic: Sesion Sync Semanal PMs (DAV/ESC/MC)
	- [[Minuta 2024-12-30 110717 - Sync PMs PER]]
	- https://app.read.ai/analytics/meetings/01JGC8ANSBM1X4W019TFWY1B18?utm_source=Share_Nav
- 30/Dic: SPI Contexto
	- https://app.read.ai/analytics/meetings/01JGCEXYT2BHK53TQZX830GMWS?utm_source=Share_Nav
- 31/Dic: Sesion: Sync Aspecto de Seguridad PER
	- Esta fue una sesión interna tecnica entre Jenny y Martín
	- https://app.read.ai/analytics/meetings/01JGEG1W234W18H03J3SBBAJH8?utm_source=Share_Nav
- 31/Dic: Sesión interna: Escala y Mobile Computing
	- [[Minuta 2024-12-31 090118 - Meeting con MC - Por Davivienda PER]]
- 2/Ene: **Septima** Sesión de Empalme PER
	- [[Minuta 2025-01-02 080108 - 11236 Empalme PER]]
- 2/Ene: Sesión: Revisión técnica (11236) -buzón de notificaciones PER Estructural
	- Se discute la funcionalidad InsertAlert
	- Pendiente resumen de Read. 🍒
	- Sergio dice que eso no esta mapeado en la entrega 1 y entrega 2

[[Resumen de Proyecto 2 Enero (GenAI)]]



---
[[20241231T1037 Proyectos Escala]]



