---
created: 2024-12-19T07:34:23
modified: '"2024-12-19 12:17", "4tc/G12T+6"'
date: 2024-12-19
type:
  - daily-note-escala
aliases: 
tags:
  - Escala24x7
---
## Apuntes
**Apuntes de trabajo en Escala2x47** del  jueves 19 de diciembre, de la semana 51 

> Aquí escribe todo lo que necesites relacionado a Escala24x7

### EMX - Robert Santos

- Cree un dashboard de tickets open  y lo comparti con Rober Santos para algunos clientes (https://escala24x7.atlassian.net/jira/dashboards/10237)

## Tareas para hoy o vencidas

```dataview
TASK
FROM "04-Work@Escala24x7"
WHERE !completed
WHERE due <= date(today)
WHERE !contains(tags, "#followup")
```



## Registro de tiempo
7:10 Sesión Arquitectura PER
7:40: things
8:00 sync ejecutivo Cempro
8:10 Sesion Empalme PER
9:00 desayunar
9:10 ver agenda, gestion sobre PER, EMX-Credicorp, 
9:30 Sesion Multidiciplinaria EMX-Rober Stantos
10:00 Trabajar en Dahsbaord para Rober Santos en paralelo con el TownHall
10:30Town Hall Escala
11:36 terminamos, pero estoy haciendo gestion de PER (10min)
12:15 inicio gestion de PER: organizacion artefactos



## Apuntes Proyectos


## Minutas del Dia
 ```dataview
table date as "Fecha de Reunión", IDProyecto as "ID del Proyecto"
from "04-Work@Escala24x7/Minutas"
where contains(type, "minuta")
where date = date(this.file.frontmatter.date)
sort date asc
```

----
**Notas relacionadas:**
[[TOC-Agenda Escala24x7]]

