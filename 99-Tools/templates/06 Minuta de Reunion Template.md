---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.file.last_modified_date("YYYY-MM-DDTHH:mm:ss") %>+
date: <% tp.date.now("YYYY-MM-DD") %>
type:
  - minuta
IDProyecto:
---

<%* await tp.file.move("/2 Areas/21 Work@Escala24x7/213 Minutas/Minuta " + tp.date.now("YYYY-MM-DD HHmmss") + " - " + tp.file.title) -%>`

#minuta 

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
