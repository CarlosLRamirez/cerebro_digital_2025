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
<%* await tp.file.move("/04-Work@Escala24x7/Agenda/" + tp.date.now("YYYY-MM-DD HHmmss") + " - " + tp.file.title) -%>`


**Entrada de diario:** 
Hoy es <% moment(tp.date.now("YYYY-MM-DD")).locale('es').format('dddd DD [de] MMMM') %>, estamos en la semana <% tp.date.now("WW") %> del año <% tp.date.now("YYYY") %>

> Aquí escribe todo lo que necesites relacionado a Escala24x7


## Tareas para hoy


## Apuntes Proyectos




----
**Notas relacionadas:**