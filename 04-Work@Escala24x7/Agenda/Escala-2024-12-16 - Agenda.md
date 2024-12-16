---
created: 2024-12-16T10:16:37
modified: '"2024-12-16 12:16", "1tc/G12T+6"'
date: 2024-12-16
type:
  - daily-note-escala
aliases: 
tags:
  - Escala24x7
---


**Apuntes de trabajo en Escala2x47** del  lunes 16 de diciembre, de la semana 51 

> Aquí escribe todo lo que necesites relacionado a Escala24x7

Ticket para acceso a Jira MC: [SOI-2663](https://escala24x7.atlassian.net/browse/SOI-2663)
Ticket para acceso a OpenVPN para MC: [SOI-2664](https://escala24x7.atlassian.net/browse/SOI-2664)

#### Temas para hablar con el PM de Davivienda #id11236
- Jira de Davivienda
- Proxima sesiones
	- Mapa de Dependencias de comunicaciones
- Cadencia sesiones
- Requerimientos para accesos a Github
- Prototipos UI/UX


## Gestión de Tareas
```dataview
TASK 
FROM "04-Work@Escala24x7"
WHERE due <= date(today) 
WHERE !completed 
WHERE !contains(tags, "#followup")  
```

## Apuntes Proyectos


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

