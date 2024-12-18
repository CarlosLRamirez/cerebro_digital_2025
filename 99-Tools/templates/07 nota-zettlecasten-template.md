---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
type:
  - Zettelkasten
aliases: 
tags: 
status:
  - in-progress
---
<%*
const iso8601 = tp.date.now("YYYY-MM-DD");
const currentTitle = tp.file.title; // Obtiene el título actual de la nota
const newName = `${iso8601} - ${currentTitle}`;
await tp.file.rename(newName);
%>

--- 
 **Notas relacionadas:**
 