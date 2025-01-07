---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
modified: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
aliases:
  - <% tp.file.title %>
tags:
---
<%*
const iso8601 = tp.date.now("YYYYMMDDTHHmm");
const currentTitle = tp.file.title; // Obtiene el título actual de la nota
const newName = `${iso8601} - ${currentTitle}`;
await tp.file.rename(newName);
%>

## Concepto Principal
*¿Què es? ¿De que se trata?*

## Contexto
*¿Porqué es importante? ¿Como se relaciona con otro tema?*

## Aspectos Clave
*Puntos principales*

## Aplicaciones
*¿Donde se podría aplicar?*


## Ejemplos
*Ejemplos de la vida real, Evidenca*

## Preguntas/Reflexiones
*¿Què preguntas o dudas me surgen del tema?*
*¿Cuales son mis reflexiones?*

## Conclusiones
*¿Cuales concluyo YO del tema?*


--- 
## Enlaces: 


## Referencias:


