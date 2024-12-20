---
type:
  - proyecto
IDProyecto:
  - "11152"
statusProyecto:
  - Transferido
cssclasses:
  - wide-page
modified: '"2024-12-13 14:58", "5tc/G12T+6"'
tags:
  - Escala24x7
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

12/Nov

Temas a dar seguimento con Connectria:
- [x] Comandos de la VTL para adicionar al menú #followup ✅ 2024-12-20
- [x] Reunion para tema de Landing Zone #followup ✅ 2024-12-20
- [x] Estado de la replica de Mimix SUFIPRO #followup
- [x] Reunion para asimetría con Josh Patterson #followup ✅ 2024-12-20
- [x] Estado del monitoreo de las maquinas #followup ✅ 2024-12-20
- [x] Reunion con Bancolombia sobre el cifrado en Direct Connect #followup ✅ 2024-12-20
- [x] Datos de ID de las tres personas de Connectria (Daniel Valverde) #followup

Puntos de Acción interno:
- [x] Confirmar la asignación de recursos de IBM al 100% #followup
- [x] Programar sesión de sync interna  #followup




8/jul:

Antonio:

I want to let you know that we are working on different topics: you must know:

1. It’s impossible to divide the NACIONAL LPAR into two because there are cross applications, which are more complex for data and object updates.
2. The client has IASP replicated by hardware right now; according to this, we are considering taking the backup, option 21, in the DR machine. Cut the replicate and execute the backup to VTL. Next, create the tapes from VTL. What do you think about this?.  Do you have some recommendations?.
3. It’s crucial the meeting tomorrow morning because we need to find a better way for IP addressing in Connectria; we need to affect the final users as little as possible.


6/Agosto:

Buenas tardes, comparto el status de los puntos de acción al final del día de hoy:

1. ~~**Definición de Bloques IP a nivel Interno:** Ya fueron entregados y se revisaron en una sesión el dia de hoy. ✅~~
2. **Definición de Direccionamiento IP a nivel WAN:** Pendiente de confirmar, el jueves 8 tenemos una reunión con Cirum/Bancolombia/Connectria donde esperamos definir el tema con Jhon Carmona
3. **Entrega de Circuitos MPLS por Cirium**: Pendiente de confirmar, el jueves 8 tenemos una reunión con Cirum/Bancolombia/Connectria donde esperamos definir el tema con Jhon Carmona
4. **Despliegue de FWs en Connectria:** En espera de recibir la licencia del proveedor. Según  información de Tatiana Sanchez, falta una aprobación "interna" de la parte económica con Axity así como la planificación de actividades, una vez se desplieguen necesitan 5 días aproximadamente. Del lado de Connectria estamos adelantando en desplegar las maquinas con el OVA sin la licencia.
5. **VPN RMM (Remote Management & Monitoring):** El de hoy nos entregaron el formulario diligenciado, la configuración en el FW del lado Banco se hará el viernes 9/ago, el proximo lunes 12/ago, estaríamos haciendo las pruebas.
6. **Direct Connect**: Jhon Carmona nos indicó que debe validar primero el diseño con el equipo de arquitectura Bancolombia, luego de reunirse con ellos nos dará feedback sobre los proximos pasos.
7. **Pre-Analisis de MIMIX en SUFI PRODUCCION:** Fue aprobada la orden de cambio para realizar la actividad el jueves 8/ago con la asistencia de manos remotas de Pastor de los Rios, debido a que aún no se resuelve el tema de los acceso del personal de Connectria.
8. **Backup Opcion 21 en maquinas de  SUFI:** Se tiene una sesión agendada para el 8/ago para revisar las alternativas planteadas.
9. **Pruebas para validar retos de Migrar Nacional**: Se solicitó una agendar una sesión para el jueves 8/Ago, con la célula de BCOM, Maria Elsy y Erwin, para revisar un documento para definir el formalizar el alcance de dicha prueba

24/Oct: Open Items

- Usuarios Escala

- 

- Conectividad Administracion y Monitoreo Connectria
- VPN usuarios Operciones Escala24x7
- Acceso a Tria Escala24x7
- Cisco SD-WAN

**NTP Issue:**

We are still aw

**New Request: Tape Restoration**


**New Request: IBMi License Expiration**

Open Items

### FIDU
- Mimix Replication
	- We have not been able to start Mimix migration, Mimix Libraries has not been restored from the tapes sent the last week. We need to start Mimix replication as soon as possible, even if remotes-hand session is required  we should request to client and prioritize - Jason 28/10
### SUFI
- NTP issue
	- We have not received answer from Connectria about the issue of time sincronization on SUFI machines. - Jason 28/10
- IBMi License
	- Bancolombia reported an IBMi license expiration on the SUFIQA machine. - Jason 28/10

- Despliegue de DevOps fallo
- Socializar numero de atención 24x7: Onboarding soporte Escala24x7
- 



### Operational
- Backup procedure and VTL access: 
	- We need to schedule a meeting with the Bancolombia, Escala,  and Connectria (Josh, Carl Norman, Micke Becker) to align and soclialize the operational process for Backups within Connectria.  - Rafael/Carlos - 28/Oct
- Connectria access credentials
	- We are waiting from Connectria to provide information of background check documents so we can confirm with the client if this comply their requirements - Jason - 28/Oct
- Runbooks:
	- We're going to present the first draft of the runbooks to Bancolombia next Monday 28/Oct with the goal to obtain their approval - Cesar Gomez - 28/Oct
- Connectria Monitoring
	- We're waiting from Connectria to confirm the integration of LPARS to the Monitoring platform. If something related to comunication is needed we need to address with client with priority. - Jason - 28/Oct
- Bancolombia Dashboards in Tria
	- We're waiting from Connnectria to confirm the Dashbaord in Tria for Bancolmbia and provide access to Escala24x7 users - Jason - 28/Oct
- Connectria VPN access
	- It might be needed that Connectria team will require to install  Cloudfare VPN client on their machines in order to connect to Cyberark. We need to consider this and provide procedure con Connectria - Carlos - 28/Oct
### Networking  (AZ1)
 
- Cisco SD-WAN Appliances:
	- VMs were deployed and ready to configure, were waiting  for next meeting with Bancolombia, no action required
- Connectria Service Network:
	- We need to test the communication between Connectria service network and the LPARS - Jason - 28/10
### Misc
- We request the creation of the user in Active Collab for rafael.tamayo@escala24x7.com - Jason - 28/10



--------
[[2024-12-09T191216 - Pilar de Trabajo (Escala24x7)]]
