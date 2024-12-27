---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.file.last_modified_date("YYYY-MM-DDTHH:mm:ss") %>+
date: <% tp.date.now("YYYY-MM-DD") %>
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto: 
---

<%* await tp.file.move("/04-Work@Escala24x7/Minutas/Minuta " + tp.date.now("YYYY-MM-DD HHmmss") + " - " + tp.file.title) -%>`


## Fecha de Reunion
<% tp.date.now() %>

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
