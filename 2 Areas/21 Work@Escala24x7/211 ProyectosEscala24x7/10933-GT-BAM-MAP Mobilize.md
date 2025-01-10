---
type:
  - proyecto
IDProyecto:
  - "10933"
statusProyecto:
  - Transferido
cssclasses:
  - wide-page
tags:
  - Escala24x7
modified: '"2025-01-09 15:31", "4tc/G1T+6"'
created: '"2024-05-20 16:46", "1tc/G5T+6"'
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
>```dataview
>LIST
>where  contains(type, "minuta" )
>where IDProyecto = this.IDProyecto
>```

[[Minuta 2023-11-24 0000 - 10933-Pilotos de Migración BAM]]
[[Minuta 2023-12-01 0000 -10933-Pilotos de Migración BAM]]




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

- [x] Socializar la arquitectura de MDF a Otto Arana  📅 2024-05-29
- [x] Enviar resumen final de entrevistas EVC   #backlog
 - [x] Revisar si hay horas registradas en Subtareas #backlog


![[Pasted image 20240611081028.png]]

---


##### CCoE
- 23/Ene: Se re-programó la sesión de seguimiento del CCoE para este viernes 26/Ene a solicitud de Escala24x7 debido a inconvenientes para poder realizarlo el día de hoy.
- 23/Ene: Recibimos feedback del BAM sobre el tema de CCoE:
	- Manifiestan un malestar por los cambios en la planificación como por ejemplo: **El Workshop de CCoE iba ser presencial y ya no fue presencial**, el cambio en la sesión de la semana pasada, el cambio de hoy, etc..
	- La retroalimentación que ha recibido el líder el proyecto de los equipo de BAM es que no estamos tomando en serio el tema del CCoE, indica que estamos perdiendo credibilidad enfrente de las personas que estamos invitando a estas sesiones.
	- Escala tomará en cuenta los comentarios recibidos para buscar puntos de mejora y cumplir con las expectativas de BAM.
### Plataforma
#### Assessments Landing Zone, Seguridad y DevOps
##### Landing Zone y Seguridad:
- 23/Ene: Se definió la fecha limite del 29/Enero para recibir respuesta de los equipos de BAM sobre las recomendaciones realizadas, en caso de no recibir respuesta se dará por finalizado el tema y se dará por completado el alcance de Escala.
- ~~Punto de Acción: Definir si hay alguna acción adicional para LZ y Seguridad o se puede cerrar este workstream - 29/01~~ 
- 26/01: Relacionado a Seguridad, se pidió prorroga para el 29, para revisar como van a quedar los compromisos de las areas respectivas. Del lado de Landing Zone, lo que tiene que ver con infraestructura seguramente no vamos a tener mayor feedback en 3 temas. 
- 26/01: El punto de acción que se pudiera implementar es relacionado con session manager (punto de mejora) a impulsar del Centro de Excelencia
##### DevOps:
- 23/Ene: el equipo de BAM tienen algunos comentarios sobre la matriz de  recomendaciones y quisiera revisar algunas, Manuel va buscar un espacio para hacer una reunión. 
- 24/Ene: se tiene agendó una sesión para hoy a las 11:30 para revisar la matriz de recomendaciones del Assessment de DevOps.
- ~~Estamos esperando la retroalimentación de BAM sobre las recomendaciones del Assessment de DevOps - 29/01  
- 26/Ene: No se ha tenido mas feedback del resto de equipos, se seguira impulsando desde el Centro de Excelencia

#### Optimización de Plataforma
##### Centralización VPC Endpoints
- 22/Ene: Jonathan Flores generará un documento para formalizar las conversaciones para las recomendaciones de centralización de VPC endpoints.
- 24/Ene: Se generó el documento con las recomendaciones sobre VPC endpoints y se subió a Teams #actionpoint #Escala24x7 #puntocerrado
#### Automatización de Etiquetado
- 23/Ene: El equipo de DevOps de Escala, esta haciendo unas pruebas sobre unas fuentes que le pidieron a Manuel, en relación al tagging requerido. 
- Jose Abzum estará informando los resultados de las pruebas para la definición de los siguientes puntos de acción para la automatización del etiquetado por medio de Pipelines #actionpoint #Escala24x7 
- 30/Ene: Jean Montilla dice que siguen trabajando, están haciendo algunas pruebas. Estimamos tenerlo para presentar para la proxima semana (Lunes 04/02).
### Modelo Operativo
#### Tagging Management
- 22/Ene : Tenemos una reunión hoy por la tarde con Otto Arana de BAM para dar seguimiento al proceso de definición del esquema de etiquetado de BAM, se buscará que nos acompañe Lillibeth de Escala24x7
- Manuel tuvo una reunion con el CCoE de Bancolombia, donde se mencionó lo siguiente
	- El año pasado se trabajó en un proyecto regional (Cloud Center), el alcance es poder colectar información de cada uno de las filiales y centralizarlo en el Cloud Center de las cuentas de Bancolombia
	- Se  desplegó un lago de datos, y agentes de config, para la replicación de cada una de las filiales
	- Ellos crean dashboards basadas en etiquetas, y pidieron una etiquetas clave.
- En BAM hay un alto porcentaje de recursos de AWS que no estan etiquetados.
- BAM esta llevando un proceso de re-etiquetado el cual lo esta liderando Otto Arana.
- Cuando se complete ese proceso, se va llevar las nuevas etiquetas clave
- Manuel necesita Escala de su retroalimentación sobre la estrategia de etiquetado para darla como cerrada
- 23/Ene: BAM nos enviará  la información sobre su política de Tagging
- 23/Ene  Luego de la sesión de ayer, enviamos un correo con el resumen de lo realizado como parte del apoyo a BAM para que definiera su estrategia de etiquetado.  #puntocerrado #Escala24x7 
- 24/01: Otto esta pidiendo acceso a la Wiki de BAM, para que quede documentado, sin embargo ya tiene un documento el cual nos va compartir  #puntocerrado #Escala24x7
- 25/Ene: La [estrategia de Tagging](https://dev.azure.com/BancoAgromercantilGT/Transformaci%C3%B3n%20Digital/_wiki/wikis/Wiki%20Programa%20Transformaci%C3%B3n%20BAM/224/AWS-Tagging-Strategy) ya esta documentado en una Wiki de BAM (la de Transformación), BAM lo va socializar internamente los lideres de BAM y luego se enviará un comunicado general. #puntocerrado #Escala24x7
	- 
#### Gestion de Parchado
- 16/Ene: BAM menciona la necesidad de un workshop para revisar la solución de AWS de Patch Management, su mayor interés es poder contar con dashboards y reportería para poder integrarla con Quicksight, les interesa que se tenga un alcance de varios SO.
	- También mencionan que tienen  un dolor sobre poder tener tracking de depreciaciones ( ej. Lambdas, etc..)
- 22/Ene:  Se mencionó la necesidad de realizar un Worskhop para conocer sobre la solución de AWS para Patch Management, sin embargo para ellos tienen prioridad la gestión de AMIs.
	- Se realizará un workshop de Patch Management, se debe coordinar cuando y quien lo estará facilitando de Escala24x7 #actionpoint #Escala24x7 
#### Gestión de AMI
- 22/Ene
	- Se tuvo una sesión donde se revisó la cuenta en AWS donde se realiza la gestión de AMIs y de parchado.
	- Ya existe una mesa de trabajo, para preparar 2 AMIs: Windows Server 2019 y Amazon Linux 2 
	- El equipo de mitigación de riesgo se encarga actualmente de las instancias en on-premise.
	- El siguiente paso es hacer un workskhop sobre EC2 Image builder, se debe coordinar cuando y quien lo estará facilitando de Escala24x7  #actionpoint #Escala24x7 
#### Modelo Operativo
- 23/Ene: Ya iniciamos con la generación de los entregables relacionados al modelo operativo, de acuerdo a los resultados obtenidos de las conversaciones de gestión de parchado, AMIs y etiquetado.
- 23/Ene: Se solicitó a BAM el llenado de una matriz con la información de los responsables de capacidad operativa. 24/Ene: Jonathan  tiene una nueva version del documento, se compartirá a BAM para su revisión.  #actionpoint #BAM 
- 24/Ene: Se creará un canal en Proyecto J2C de Modelo Operativo, aquí deberíamos colocar los diferentes procesos (Organización y cuentas, Asignación de Usuarios y Roles, Proceso de Etiquetado, Aseguramiento de servicios, Recolección de información sobre aplicaciones, Proceso de Migración) #actionpoint #BAM
- 24/Ene Jonathan ya esta trabajando en el documento final del Modelo Operativo. Se colocará en el canal de Modelo Operativo #actionpoint #Escala24x7 
- 30/Ene: Entregar un primer draft del documento del modelo operativo, antes de empezar a abordar los otros temas, Jonathan va completar los puntos de Patch Management, Monitoring & logging, y AMI Management. La matriz que Jonathan entregó, donde todos está como Reponsables, Manuel pregunta si lo vamos a dejar así como vamos a tener sesiones con los responsables. Considera que debe socializarlo y agregar los roles de los equipos existentes. Accenture levantó un modelo operativo, pero solo se le entregó a los lideres, y segun Manuel esta muy fuera del contexto del banco (es mas como una plantilla), no se puso en marchan, no se reflejaron las estructuras de BAM (Roles y atribuciones, perfiles). Ahora es una buena oportuidad para que eso no vuelva a pasar.  #actionpoint #Escala24x7 
## Portafolio

### Herramientas de Discovery
- 22/Ene
	- Debido al freeze por el ejercicio de DR, se puede iniciar con el proceso de instalación de agente a partir de la próxima semana 29/01.
	- La instalación debe ser desatendida, y la idea es que se haga por medio de Endpoint Central
	- Edgar Lange enviará las instrucciones de instalación desatendida por correo, la cual incluira varios sistemas operativos.  #Escala24x7  25/Ene: hoy Edgar envió las instrucciones #puntocerrado
	- Esta semana podemos avanzar con el tema de la Bases de Datos
	- Edgar Lange revisará el punto de la configuración de los parametros de base de datos y nos enviará una respuesta.  #Escala24x7 #puntocerrado 25/Ene: Edgar indicó que iba hacer unas pruebas con un AD, dar seguimiento con Edgar.
	- Ya se solicitaron los acceso de Edgar Lange y Luis Yepes, BAM nos compartirá la información hoy. 
- 23/Ene
	- Se solicita dar seguimiento a la solicitud de BAM sobre la generación de un algoritmo o proceso para la recolección de datos por medio de las herramientas de Discovery
	- Generar un procedimiento que describa los pasos a realizar para la recolección de datos por medio de las herramientas de discovery (p.ej. Agrupación de servidores, configuración de base de datos, repositorios de códigos, etc.. #actionpoint #Escala24x7 
	- Ya se compartieron las credenciales de Edgar y Luis a Catherine Yepes. 24/Ene: esperamos la confirmación de los accesos a la consola #actionpoint #BAM
- 24/Ene:
	- Respuesta de AWS con la herramienta. AWS dice que hagamos una prueba con un ESXI aislado, actualmente no tienen capacidad, y Manuel necesita claridad sobre el porque los ESXI se estresaban, queda la duda si se transmitió bien en el mensaje, Luis Yepes lo esta gestionado con AWS. #actionpoint #Escala24x7
	- Necesitamos que Edgar Lange y Luis Yepes, tengan una licencia para Azure DevOps #actionpoint
- 26/Ene: Ayer tuvieron una sesion sobre el tema de los ESXI, quedaron algunos puntos de acción (3 compromisos macro)
	- Creación de un usuario de base de datos, (sqllogin), Edgar ya entrego la información sobre como debe ser el usuario #actionpoint #BAM
	- Area de administración de sistemas, instalación de el agente. Edgar ya compartió la información sobre los comandos para ejecutarse de manera remota. Se solicitaron 10 servidores (6 Windows, 4 Linux), aún no se han identificado. Esta implicito la instalación de manera remota. Se impacta al equipo de identificación de vulnerabilidades, ya que la herramienta de parchado es la que se utilizar (Endpoint Central) #actionpoint #BAM 
	- Proveer a acceso a internet a la URL, se impacta al equipo de Cyberseguridad, será por Firewall #actionpoint #BAM
- 30/Ene
	- Hoy nos asignaron un sysadmin, para que nos den información sobre los servidores e IPs, se espera que hoy tengamos esa información.
		- Ya tenemos 11 servidores de QA (solo servidores de aplicación), vamos a instalar el agente en estos cinco servidores.
	- Para la instalación debemos involucrar a otro equipo (el que instala los parches), hay que pasarle las instrucciones de instalación. Podemos hacer una prueba de instalación manual y des-instalación, Edgar esta disponible a las 4pm. #actionpoint #BAM 
	- Vamos a aprovechar para gestionar el acceso ala URL con ciberseguridad. #actionpoint #BAM 
	- Con el tema de DB, se les planteó y dijeron que van a entregar un listado de instancias de BD y un formulario. Se debe llenar ese formulario y luego gestionar todas las  autorizaciones debidas #actionpoint #Escala24x7 #ojo 
	- Sesión con AWS para hacer revisar el tema de los ESXI #BAM #actionpoint
### Entrevistas con las EVC
- 22/Ene
	- Ya están agendadas todas las sesiones de entrevistas asignadas para el Sprint 2, incluyendo las 5 de la EVC de Transformación Interna BAM.
- 23/Ene
	- Se solicitó el apoyo a los lideres de las EVC para que completen los diagramas de arquitectura de las aplicaciones faltantes #actionpoint #BAM 
- 24/Ene: Se esta solicitando la información del servidor actual,
- Se esta pidiendo la planificación para el siguiente sprint #actionpoint #BAM
- 30/Ene:
	- Sesión con Luis Porras #BAM #Escala24x7
- 
## Migración
### Arquitecturas objetivo
- 23/01
	- Se tiene el compromiso de entregar al final de este sprint (26/01) las arquitecturas objetivo de las 5 aplicaciones piloto. #actionpoint #Escala24x7 
	- Solicitamos identificar las personas para abordar la aplicación de MQ, contacto proveedor #actionpoint #BAM
## Mobilize
- 23/01
	- Se definirá un mecanismo para dar seguimiento a los diferentes puntos de acción acordados en las diferentes sesiones de seguimiento con BAM
	- Enviar un listado de los diferentes puntos de acción del proyecto para poder darle seguimiento.  #Escala24x7 #puntocerrado 



## Puntos de acción abiertos

```dataview
list without id
L.text
flatten file.lists as L
where contains(L.tags, "#actionpoint") AND file.name = this.file.name
```



29/01
- Centralización de comunicaciones con terceros en una cuenta. Vamos a tener mas de 10 o 50 VPNs en una sola cuenta, el tema es que AWS tiene cuotas. Manuel quiere verificar si VPC Lattice tiene capacidad de gestión de VPNs, o si se puede incrementar las cuotas de VPNs en una sola cuenta.
- Ver tema de Jonathan por su Teams
- [x] Subir los archivos de Jonathan ✅ 2024-02-02
- Rony Reyes dice que con ellos no hubo assessment, o una documentación de recomendación del lado de ellos. 
- Assessment de DevOps: los puntos que no se tocaron , deben ser atacados por el centro de excelencia.
- Portafolio
	- Ya se solicito a los DBA el usuario
	- Ya se solicitó a Admin Systemas, el detalle de los servidores.
	- Ya se dio a Edgar el acceso a Azure DevOps
	- Podemos hacer una prueba para conectar strategy con ADO 
	- Manuel solicita apoyo sobre los puntos que cada equipo necesita trabajar, importante tener un listo (checklist) de las necesidades. 
		- Que acción se necesita de cada equipo, y hacer track de cada (pasos macro) #actionpoint 


## Planning Sprint 8
- Inicio del Sprint: 29/Enero
- Fin del Sprint: 11/Febrero
### Objetivos del Sprint:
- **People:** 
	- Finalizar los entregables del CCoE,
- **Platform:** 
	- Ejecutar planes de acción e identificar responsabilidades a partir de los resultados de los diferentes Assessments.
	- Generar recomendaciones y planes de acción para las solicitudes planteadas por BAM para optimizar su plataforma mas allá del baseline.
	- Construir el modelo operativo en la nube para BAM, con análisis de estado actual y generar recomendaciones y planes de acción.
- **Portafolio**:
	- Iniciar con la ejecución de las herramienta de descubrimiento automatizado del portafolio de aplicaciones, con el fin de obtener datos que permitan el análisis y categorización de las aplicaciones según su estrategia de migración.
- **Migración**:
	- Definir junto con BAM las arquitecturas en la nube para las 5 aplicaciones piloto.
	- Realizar las acciones necesarias para preparar la plataforma para poder realizar migraciones masivas, en base a las arquitecturas modelo propuestas.
	- Iniciar con las acciones de preparación para poder migrar la primera aplicación piloto a AWS.

### Sprint Backlog

People - CCoE
* [Documentación y entregables CCoE](https://escala24x7.atlassian.net/browse/BAM-239) -  Luis Higuera

Plataforma - Optimización de Landing Zone
* [Optimización de la Gestión de VPNs](https://escala24x7.atlassian.net/browse/BAM-240) - Jonathan Flores
* [Optimización para la Automatización de Etiquetado por Pipelines](https://escala24x7.atlassian.net/browse/BAM-120) - Jean Montilla

Plataforma - Assessment de Seguridad
- [Definir acciones a implementar según recomendaciones de seguridad](https://escala24x7.atlassian.net/browse/BAM-175) - Francisco Brito
- [Implementación recomendaciones sobre postura de seguridad (consultoria y acompañamiento)](https://escala24x7.atlassian.net/browse/BAM-126) - Francisco Brito

Plataforma - Assessment de DevOps
- [Definir y asignar responsabilidades sobre los resultados](https://escala24x7.atlassian.net/browse/BAM-241) - Jean Montilla

Plataforma - Modelo Operativo
- [Account & User Management](https://escala24x7.atlassian.net/browse/BAM-136) - Jonathan Flores
- [Change Management](https://escala24x7.atlassian.net/browse/BAM-104) - Jonathan Flores
- [License Management](https://escala24x7.atlassian.net/browse/BAM-149) - Jonathan Flores
- [Availability & Continuity Management (includes Backup / Restore)](https://escala24x7.atlassian.net/browse/BAM-151) - Jonathan Flores
- [Event & Incident Management (includes Logging & Monitoring)](https://escala24x7.atlassian.net/browse/BAM-99) - Jonathan Flores
- [Configuration Management](https://escala24x7.atlassian.net/browse/BAM-127) - Jonathan Flores
- [Documentación Modelo Operativo](https://escala24x7.atlassian.net/browse/BAM-238) - Jonathan Flores

Portafolio - Data Collection
- [Ejecución del Discovery Tool (Migration Hub) (escaneo, agrupación y BD)](https://escala24x7.atlassian.net/browse/BAM-131) - Edgar Lange
- [Configuración de información de repositorios de código](https://escala24x7.atlassian.net/browse/BAM-237) - Edgar Lange
- [Sesiones de discovery con EVCs](https://escala24x7.atlassian.net/browse/BAM-235) Luis Higuera/Christian Segovia/John Barrera/Jean Montilla

Portafolio - Análisis de Portafolio
- [Categorizar aplicaciones según estrategia de migración (7 R's)](https://escala24x7.atlassian.net/browse/BAM-123) - Luis Higuera

Migración  - Arquitecturas Objetivo
- [Definir arquitectura objetivo (Aplicación Piloto 1)](https://escala24x7.atlassian.net/browse/BAM-96) - Luis Higuera / Christian Segovia
- [Definir arquitectura objetivo (Aplicación Piloto 2)](https://escala24x7.atlassian.net/browse/BAM-111) - Luis Higuera / Christian Segovia
- [Definir arquitectura objetivo (Aplicación Piloto 3)](https://escala24x7.atlassian.net/browse/BAM-194) - Luis Higuera / Christian Segovia
- [Definir arquitectura objetivo (Aplicación Piloto 4)](https://escala24x7.atlassian.net/browse/BAM-234) - Luis Higuera / Christian Segovia
- [Definir arquitectura objetivo (Aplicación Piloto 5)](https://escala24x7.atlassian.net/browse/BAM-122) - Luis Higuera / Christian Segovia

Migración - Migration Factory
- [Despliegue de Migration Factory](https://escala24x7.atlassian.net/browse/BAM-116)- Jonathan Flores
- [Pruebas de Migration Factory](https://escala24x7.atlassian.net/browse/BAM-97) - Jonathan Flores

Migración - DevOps Baseline
- [Migration Governance - DevOps Mobilize Scope Planing](https://escala24x7.atlassian.net/browse/BAM-103) - Jean Montilla
- [DevOps Baseline Platform Deployment](https://escala24x7.atlassian.net/browse/BAM-117)- Jean Montilla
- [Landing Zone - Iac Pipeline Template Implementation](https://escala24x7.atlassian.net/browse/BAM-134) - Jean Montilla

Migración - Aplicación 1
- [Preparación Migración Aplicación 1  - Por Refinar](https://escala24x7.atlassian.net/browse/BAM-158) - lidera Luis Higuera, apoya todo el team.


## 31/Enero
- Instalación de herramienta:
	- Ayer se instaló un agente en una máquina
	- Se desplegó un grupo de recursos en la nube, pero resulta que la máquina que se desplegó en la nube, según Edgar, esa le tiene que llegar a todas las maquinas donde esta instalado el agente. Eso tiene un impacto muy alto y tiene mucho riesgo para BAM, se esta buscando la posibildad de configurar una de las VM (uno de los colectores) y que ese se comunique con las maquinas a travez de WinRM.
	- Nos ha echo falta contextualizar mejor las soluciones, tener un plan previo y los pre-requistos bien definidos para el cliente. Lo vamos resolviendo y cambiando en el camino. Nos compromete porque no damos claridad de todo lo que vamos a hacer a los equipo internos del Banco.
	- Manuel indica que necesita mas claridad sobre cual es la diferencia o cual es la ganancia de instalar los agentes, su perspectiva es que no era necesario porque ya teniamos el inventario de servidores con el otro agente. El agente tambien es para hacer inventario de maquinas y que aparte hay otro tipo de colector. Manuel tiene la inseguridad que se vaya volver a estresar las maquinas. Cual es la diferencia?
	- Manuel quieisra tener una compartiva de la arquitectura y el flujo de lo que hemos trabajado. Manuel se esta creando una mala percepción.
	- Jean-Paul nos dice que le esta quedando la impresion que estamos probando y pareciera que no lo habíamos hecho antes. Que es primera vez que lo hacemos. Este era el plan B y ven que no estamos avanzando.
- Arquitecturas
	- Buscar una sesion de seguimiento con Luis Valle y Rony
- Entrevistas EVC
	- Los equips de Escala no estan tomando elementos transversales, como DNS, actualización de IPs, definiciones previas sobre NTP, DNS





## SYNC interno - Discovery Tools
- Ellos quedaron con la tarea de poner el parametro en Disabled






--------
## Enlaces:
[[Minuta 2023-11-24 0000 - 10933-Pilotos de Migración BAM]]
[[Minuta 2023-12-01 0000 -10933-Pilotos de Migración BAM]]
[[Minuta 2024-01-05 1048 - Sync BAM]]
[[Minuta 2024-01-05 1521 - Alto consumo de CPU]]
[[Minuta 2024-01-12 1024 - Sync BAM]]
[[Minuta 2024-01-12 1505 - Sync Discovery Tool - BAM]]
[[Minuta 2024-01-15 1436 - Seguimiento BAM - Herramientas de Discovery]]
[[Minuta 2024-01-16 1054 - Daily BAM]]
[[Minuta 2024-01-17 1036 - Daily Sync BAM]]
[[Minuta 2024-01-17 1128 - sync interna BAM]]
[[Minuta 2024-01-18 0906 - Reunion con Manuel sobre Dicovery]]
[[Minuta 2024-01-22 1550 - Tag Management - BAM]]
[[Minuta 2024-02-01 0832 - Sync interna - Backlog Seguridad BAM]]
[[Minuta 2024-02-05 1037 - Daily Sync - BAM]]
[[Minuta 2024-02-06 1034 - Daily BAM]]
[[Minuta 2024-02-07 1033 - Daily BAM]]
[[Minuta 2024-02-12 0902 - Novedades cierre de proyectos]]
[[Minuta 2024-02-12 1035 - Sync BAM Daily]]
[[Minuta 2024-02-13 1037 - Sync BAM]]
[[Minuta 2024-02-16 1033 - Sync BAM]]
[[Minuta 2024-02-19 1033 - Daily BAM]]
[[Minuta 2024-02-19 1400 - sync interno - BAM - Portafolio]]
[[Minuta 2024-02-20 0806 - Revision Desembolso de Credito Faci - Bamavisa]]
[[Minuta 2024-02-20 1532 - Sesión por WAT y SCR - BAM GT]]
[[Minuta 2024-02-22 0930 - Reunion con Bancolombia sobre BAM]]
[[Minuta 2024-03-22 1054 - Sync BAM - Pilotos de Migración]]
[[Minuta 2024-03-25 1034 - Sync BAM - Plataforma]]
[[Minuta 2024-03-27 0907 - Sync Interna - BAM]]
[[Minuta 2024-04-01 1030 - 10933-BAM-Cadencia BAM - Plataforma]]
[[Minuta 2024-04-02 1431 - Sync BAM - Portafolio]]
[[Minuta 2024-04-15 1043 - Cadencia - Plataforma - BAM]]
[[Minuta 2024-04-16 1007 - CAdencia - BAM - Portafolio]]
[[Minuta 2024-04-17 0922 - Sync interna modernizacion BAM]]
[[Minuta 2024-04-19 1205 - Sync BAM Migraciones]]
[[Minuta 2024-04-24 0907 - Sync interna BAM]]
[[Minuta 2024-05-08 1540 - 10933 - BAM Sync - Discovery portafolio]]
[[Minuta 2024-05-09 1110 - 10933 - Onboarding Infraestructura - Modernizacion]]
[[Minuta 2024-05-17 0856 - BAM - Sync Interno - 2024-05-16]]
[[Minuta 2024-05-20 0804 - Sync BAM - Sprint Planning]]
[[Minuta 2024-05-24 1047 - Cadencia Modernización - BAM]]
[[Minuta 2024-05-28 0830 - Daily BAM - MDF]]
[[Minuta 2024-05-30 0807 - BAM - Daily Sync MDF]]
[[Minuta 2024-05-31 0804 - Sync BAM Daily - 31May]]
[[Minuta 2024-06-03 0756 - Migracion MDF - Cadencia Diaria - Sprint 1 - 3 Jun]]
[[Minuta 2024-06-04 0806 - Sync BAM MDF]]
[[Minuta 2024-06-04 1137 - SYNC BAM]]
[[Minuta 2024-06-10 0801 - Sync BAM - MDF Daily]]
[[Minuta 2024-06-11 0803 - Daily MDF BAM]]
[[Minuta 2024-06-12 0806 - BAM - Daily Sync - MDF]]
[[Minuta 2024-06-12 0905 - Infra -BAM - MDF]]
[[Minuta 2024-06-14 0802 - Daily BAM - MDF]]
[[Minuta 2024-06-17 0951 - Sync MDF BAM]]
[[Minuta 2024-06-18 0822 - BAM MDF Sync]]
[[Minuta 2024-06-19 0820 - Sync BAM MDF]]
[[Minuta 2024-06-21 0803 - Sync BAM MDF]]
[[Minuta 2024-06-21 0937 - Sync Discovery Portafolio BAM]]
[[Minuta 2024-06-21 1041 - Cadencia migraciones BAM]]
[[Minuta 2024-06-24 0759 - Daily Sync - BAM]]
[[Minuta 2024-07-09 0807 - Daily MDF BAM]]
[[Minuta 2024-07-09 1209 - Sync Ruth]]
[[Minuta 2024-07-11 0707 - Jorland entrega BAM]]
[[Minuta 2024-07-11 0802 - Daily MDF]]
[[Minuta 2024-07-30 1504 - Planificaciòn BAMAVISA]]

