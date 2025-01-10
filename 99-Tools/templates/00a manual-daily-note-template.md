---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.file.last_modified_date("YYYY-MM-DDTHH:mm:ss") %>
date: <% tp.date.now("YYYY-MM-DD") %>
type:
  - daily-note
aliases: 
tags:
  - journal
---
**Entrada de diario:** 
Hoy es <% moment(tp.date.now("YYYY-MM-DD")).locale('es').format('dddd DD [de] MMMM') %>, estamos en la semana <% tp.date.now("WW") %> del año <% tp.date.now("YYYY") %>

> Aquí escribe todo lo que piensas sobre el día de hoy

<% tp.file.rename(tp.date.now("YYYY-MM-DD ddd HHmmss") + "-Daily Note") %>



**Hacerlo hoy:**
```tasks
not done
(due before today) OR (due today)
(tag include #personal) OR (tag include #syprotec) OR (tag include #teaching)
```

----
**Notas relacionadas:**