---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.file.last_modified_date("YYYY-MM-DDTHH:mm:ss") %>
date: <% tp.date.now("YYYY-MM-DD") %>
type:
  - daily-note-escala
aliases: 
tags:
  - Escala24x7
---
<%* await tp.file.move("/04-Work@Escala24x7/Agenda/" + "Escala-" + tp.date.now("YYYY-MM-DD") + " - " + tp.file.title) -%>`


**Apuntes de trabajo en Escala2x47** del  <% moment(tp.date.now("YYYY-MM-DD")).locale('es').format('dddd DD [de] MMMM') %>, de la semana <% tp.date.now("WW") %> 

> Aquí escribe todo lo que necesites relacionado a Escala24x7

## Tareas para hoy


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

