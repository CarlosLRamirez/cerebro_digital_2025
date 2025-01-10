---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.file.last_modified_date("YYYY-MM-DDTHH:mm:ss") %>
date: <% tp.date.now("YYYY-MM-DD") %>
aliases:
---
<%* await tp.file.move("/2 Areas/21 Work@Escala24x7/Agenda/" + "Escala-" + tp.date.now("YYYY-MM-DD") + " - " + tp.file.title) -%>`

#daily-escala 

**Agenda Escala2x47** del  <% moment(tp.date.now("YYYY-MM-DD")).locale('es').format('dddd DD [de] MMMM') %>, de la semana <% tp.date.now("WW") %> 

## ☑ Tasks

```tasks
not done
(due before today) OR (due today)
```


## 📓 Notes 
- 
- 
- 


## 🗒 Minutes of Meetings

 ```dataview
table date as "Fecha de Reunión", IDProyecto as "ID del Proyecto"
from "2 Areas/21 Work@Escala24x7/213 Minutas"
where contains(type, "minuta")
where date = date(this.file.frontmatter.date)
sort date asc
```

----
## Related Notes:

