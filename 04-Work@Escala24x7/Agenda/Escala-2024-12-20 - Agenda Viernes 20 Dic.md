---
created: 2024-12-20T07:40:41
modified: '"2024-12-20 08:01", "5tc/G12T+6"'
date: 2024-12-20
type:
  - daily-note-escala
aliases: 
tags:
  - Escala24x7
---
`


**Apuntes de trabajo en Escala2x47** del  viernes 20 de diciembre, de la semana 51 

> Aquí escribe todo lo que necesites relacionado a Escala24x7

## Tareas para hoy
-


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

