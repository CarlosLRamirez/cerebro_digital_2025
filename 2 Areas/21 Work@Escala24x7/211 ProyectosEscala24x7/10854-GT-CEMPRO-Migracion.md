---
IDProyecto:
  - "10854"
statusProyecto:
  - activo
cssclasses:
  - wide-page
tags:
  - Escala24x7
modified: '"2025-01-08 09:30", "3tc/G1T+6"'
type:
  - proyecto
---
#proyecto-escala 
#id10854

> [!multi-column]
>
>> [!todo]+ Do Today or Overdue
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


> [!multi-column]
>> [!tip]+ Issues
>> ```dataview
>>TASK WHERE contains(tags, "#id" + this.IDProyecto) AND contains(tags, "#issue") AND !completed
>>```
>
>> [!danger]+ Risks
>> ```dataview
>>TASK WHERE contains(tags, "#id" + this.IDProyecto) AND contains(tags, "#risk") AND !completed
>>```

> [!Example]+ Minutas
>```dataview
>LIST
>where  contains(type, "minuta" )
>where IDProyecto = this.IDProyecto
>```



> [!NOTE]+ Enlaces importantes
> 
> - [Carpeta del Proyecto](https://drive.google.com/drive/folders/1f_pl9NjN9ZPFGCo-sBR3EZKUdenrbytD?usp=sharing)
> - [Informe de Status](https://docs.google.com/presentation/d/1Rr4Kg0bZDKAAzw5VDje7zP-uvwWfhmmX3nbdEoelST0/edit?usp=sharing)
> - [Tablero Jira](https://escala24x7.atlassian.net/jira/software/c/projects/DACR/boards/733)
> - [[👷 Work@Escala24x7]]

> [!abstract]+ Calendario/Cadencias
> - Inicio de Sprint:  
> - Fin de Sprint: Domingo (Viernes)
> - Envío de Status Report: Viernes (15/03, 29/03, ...)
> - Cerrar Sprint en JIRA: N/A

---- 
# Apuntes

10/Ene: El proyecto esta a punto de cerrarse, solo falta la ventana para hacer el paso a producción de AppRuteo, se envió un correo de seguimento el 8 de Enero

---

## Enlaces:
[[Minuta 2024-01-02 1558 - CEMPRO - Internal Sync]]
[[Minuta 2024-03-26 1308 - Reunion - AWS - Escala - Cempro]]
[[Minuta 2024-04-02 1433 - Sync Interna - CEMPRO - Arquitecturas Migracion]]
[[Minuta 2024-04-03 1025 - Sync Cempro]]
[[Minuta 2024-04-03 1201 - Sync Esteban]]
[[Minuta 2024-04-04 0922 - Cempro - Reunion - Presencial]]
[[Minuta 2024-04-05 1431 - Cempro - Alineación Interna]]
[[Minuta 2024-04-11 1002 - Cempro - Post Reunion]]
[[Minuta 2024-04-11 1407 - SFTP Cempro]]
[[Minuta 2024-04-15 0916 - Sync Interno - CEMPRO]]
[[Minuta 2024-04-16 1612 - Entrega SFTP - Cempro]]
[[Minuta 2024-04-17 1009 - Sync General - CEMPRO - Cliente]]
[[Minuta 2024-04-19 - Planificacion general Modernizacion]]
[[Minuta 2024-04-22 0916 - CEMPRO - Sync Interna]]
[[Minuta 2024-05-02 1202 - Programa de Modernización para Cempro]]
[[Minuta 2024-05-06 0902 - 10854 - Cempro - Working Session - Instalación de Agente ADS]]
[[Minuta 2024-05-20 1515 - Sync Storage - CEMPRO]]
[[Minuta 2024-05-22 1641 - Sync Juan Calros CEMPRO]]
[[Minuta 2024-05-30 1319 - Sync Interna Cempro 30Mayo2024]]
[[Minuta 2024-06-03 0758 - Cempro - Analisis Casos de Uso EFS]]
[[Minuta 2024-06-03 1614 - IMMD Devops y Container]]
[[Minuta 2024-06-04 0906 - Sync Presentación Cempro]]
[[Minuta 2024-06-12 1044 - CEMPRO - CASOS DE USO - STORAGE]]
[[Minuta 2024-06-17 1011 - Sync Con Luis Yepes - Jhonatan - CEMPRO]]
[[Minuta 2024-06-19 1032 - 10854 - CEMPRO - Sync interna]]
[[Minuta 2024-06-19 1132 - Sync Cempro]]
[[Minuta 2024-06-24 0832 - Sync Jenny-Carlos - Yepes-Lange-Cempro]]
[[Minuta 2024-07-09 1037 - Sync interno Cempro - Storage]]
[[Minuta 2024-07-25 1101 - Sync Cempro interna - Lift shift - discovery]]
[[Minuta 2024-07-31 1640 - Sync Juan Carlos]]
[[Minuta 2024-08-12 1336 - Sync AWS sobre Cempro]]
[[Minuta 2024-08-13 1130 - Sync interno CEMPRO]]
[[Minuta 2024-08-22 1043 - Cempro - Sync con AWS]]
[[Minuta 2024-09-23 1013 - Sesion de Trabajo Cempro - Modernizaciones]]
[[Minuta 2024-10-01 1412 - MAP Tagging - Cempro Sync]]
[[Minuta 2024-10-14 1018 - Cempro - Sesion de Trabajo]]
[[Minuta 2024-11-05 1140 - 10854 - Cempro]]
[[Minuta 2024-11-19 1136 - Sync Interno Cempro]]
[[Minuta 2024-12-17 111428 - PaO Cempro - Ift and shift]]
[[Minuta 2025-01-10 124749 - Minuta 2024-01-10 1000 - Sync con Cempro (Cliente)]]
[[Minuta 2024-03-25 0915 - Sync Interno - CemPRO]]
[[Minuta 2024-03-26 1007 - Reunion Cempro - Alejandro - Beatriz]]

