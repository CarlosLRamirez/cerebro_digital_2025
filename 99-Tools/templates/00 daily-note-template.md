---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.file.last_modified_date("YYYY-MM-DDTHH:mm:ss") %>
type:
  - daily-note
aliases: 
tags:
  - journal
---
 <%* moment.locale("es"); %>
 **Entrada de diario:** 
<% tp.date.now("dddd DD [de] MMMM") %>, estamos en la semana <% tp.date.now("WW") %> del año <% tp.date.now("YYYY") %>

> Aquí escribe todo lo que piensas sobre el día de hoy


----
**Notas relacionadas:**