---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
date: <% tp.date.now("YYYY-MM-DD") %>
type: []
aliases: 
tags:
---
<%*
const iso8601 = tp.date.now("YYYY-MM-DDTHHmmss");
const currentTitle = "Nota Rápida" ; // Obtiene el título actual de la nota
const newName = `${iso8601} - ${currentTitle}`;
await tp.file.rename(newName);
%>

--- 
 **Notas relacionadas:**
 