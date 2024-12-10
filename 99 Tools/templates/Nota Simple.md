---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.file.last_modified_date("YYYY-MM-DDTHH:mm:ss") %>
pilar: 
type: 
aliases: 
tags:
---
<%*
const iso8601 = tp.date.now("YYYY-MM-DD");
const currentTitle = tp.file.title; // Obtiene el título actual de la nota
const newName = `${currentTitle} - ${iso8601}`;
await tp.file.rename(newName);
%>