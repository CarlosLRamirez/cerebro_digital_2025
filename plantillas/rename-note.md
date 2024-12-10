---
Created: <% tp.date.now("YYYY-MM-DD") %>
Last modified: <% tp.file.last_modified_date("YYYY-MM-DD") %>
Aliases: 
Tags: 
---
<%*
const iso8601 = tp.date.now("YYYY-MM-DDTHHmmss");
const currentTitle = tp.file.title; // Obtiene el título actual de la nota
const newName = `${iso8601} - ${currentTitle}`;
await tp.file.rename(newName);
%>