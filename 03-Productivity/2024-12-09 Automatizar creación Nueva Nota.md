---
created: 2024-12-09T18:04:29
modified: '"2024-12-10 14:49", "2tc/G12T+6"'
aliases: 
tags:
  - obsidian
---
Con **Templater** cree una plantilla para nuevas notas simples:
```
---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.file.last_modified_date("YYYY-MM-DDTHH:mm:ss") %>
aliases: 
tags:
---
<%*
const iso8601 = tp.date.now("YYYY-MM-DDTHHmmss");
const currentTitle = tp.file.title; // Obtiene el título actual de la nota
const newName = `${iso8601} - ${currentTitle}`;
await tp.file.rename(newName);
%>
```

> el flujo actual es:
> 	1. creo la nota, le pongo un titulo , y luego hago click en el icono de templater para renombrar la nota o le doy Control+I
> 	2. .Otra forma es darle Control+N para crear una nueva nota desde cero con titulo Untitled, y luego renombrarla

Hay otra forma para que automáticamente le de formato a la nota al momento de su creación pero aún no lo he podido aplicar

#todo/obsidian
- [ ] Implementar automatización al crear notas nuevas
  

---
**Notas relacionadas**
[[2024-12-09 My Obsidian Setup]]


