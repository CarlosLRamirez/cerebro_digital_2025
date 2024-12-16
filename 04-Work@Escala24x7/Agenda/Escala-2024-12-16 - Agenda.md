---
created: 2024-12-16T10:16:37
modified: '"2024-12-16 13:48", "1tc/G12T+6"'
date: 2024-12-16
type:
  - daily-note-escala
aliases: 
tags:
  - Escala24x7
---


**Apuntes de trabajo en Escala2x47** del  lunes 16 de diciembre, de la semana 51 

> Aquí escribe todo lo que necesites relacionado a Escala24x7



## Gestión de Tareas
```dataview
TASK 
FROM "04-Work@Escala24x7"
WHERE due <= date(today) 
WHERE !completed 
WHERE !contains(tags, "#followup")  
```

## Apuntes Proyectos

### 11236 PER Daivienda

- [ ] Se abrio Ticket para acceso a Jira MC: [SOI-2663](https://escala24x7.atlassian.net/browse/SOI-2663) #followup #id11236 
- [ ] Ticket para acceso a OpenVPN para MC: [SOI-2664](https://escala24x7.atlassian.net/browse/SOI-2664) #followup #id11236

- [ ] Temas para hablar con el PM de Davivienda #id11236 #followup
- Jira de Davivienda
- Proxima sesiones
	- Mapa de Dependencias de comunicaciones 
		- Hoy en la tarde me confirma
	- Sesiones de Empalme 
		- A partir de manaña en adelante a las 9am
- Cadencia sesiones
- Requerimientos para accesos a Github
	- Hoy tienen una sesion con el equipo de Whitelist, hoy en la tarde me confirman que necesitan
- Prototipos UI/UX
	- Mockups 
	- Martin
	- Darle el correo del desarrollador front  end a Davivienda (Schedule)
	- 
### 10854
- [ ] Sesión de PaO Lift &Shift martes 17 Dic #followup #id10854
### 11065 -Whitelist

- Actualice el registro de Items Abiertos
- [ ] Darle seguimiento al cuadro de items abiertos #id11065 #followup 

### 11206  - Davivienda - Ambientes Bajos
- Se envió un correo con los proximos pasos para las pruebas de conectividad
- [ ] Dar seguimiento al correo enviado sobre pruebas de conectividad 📅 2024-12-18 #id11206 




## Minutas del Dia
 ```dataview
table date as "Fecha de Reunión", IDProyecto as "ID del Proyecto"
from "04-Work@Escala24x7/Minutas"
where contains(type, "minuta")
where date = date(this.file.frontmatter.date)
sort date asc
```

----
**Notas relacionadas:**
[[TOC-Agenda Escala24x7]]

