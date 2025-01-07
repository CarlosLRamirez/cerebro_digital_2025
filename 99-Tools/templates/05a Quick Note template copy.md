---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
date: <% tp.date.now("YYYY-MM-DD") %>
type: []
aliases: 
tags:
---

<%* 
const fileName = tp.file.title; 
const iso8601 = tp.date.now("YYYYMMDDTHHmm");
const dateAgenda = tp.date.now("YYYY-MM-DD");

if (fileName.startsWith("Agenda Escala")) { 
  // Aplica la plantilla "Agenda Escala"
  await tp.file.move("/Areas/Work@Escala/Agenda/" + dateAgenda + " " + "at Escala24x7"); 
} else {
  const newName = `${iso8601} ${fileName}`;
  await tp.file.rename(newName);
}
%>
--- 
 **Enlaces:**
 