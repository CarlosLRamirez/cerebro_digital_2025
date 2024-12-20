---
created: 2024-12-13T15:13:00
modified: '"2024-12-20 10:54", "5tc/G12T+6"'
type:
  - Home
aliases: 
tags:
  - Escala24x7
---
# 👨‍🏭 HOME - Escala24x7

- [[TOC-Agenda Escala24x7]]
- [[2024-12-20 - Task Manager Escala24x7]]


## Tareas

```dataview
TASK
FROM "04-Work@Escala24x7"
WHERE !completed
WHERE due <= date(today)
WHERE !contains(tags, "#followup")
GROUP by tags
```


[[20241119 1249 - Enlaces Escala24x7]]
[[20241119 1317 - Registro de horas]]




## Seguimiento
## Proyectos Escala24x7
solo activos
```dataview
TABLE statusProyecto
from "04-Work@Escala24x7/ProyectosEscala24x7"
WHERE contains(type, "proyecto")
WHERE contains(statusProyecto, "activo")
sort IDProyecto asc
```

## Accounts
### Davivienda CECA
- [Carpeta Arquitectura](https://drive.google.com/drive/folders/1D-QKvglLwwTeO6GmhitXAkN0pkraHXOu?usp=drive_link)
## Enlaces  
[20241119 1249 - Enlaces Escala24x7](20241119%201249%20-%20Enlaces%20Escala24x7.md)



-----
[[2024-12-13 - Workflow - Gestion de Proyectos y Tareas Escala24x7]]



---
[[🏠 HOMEPAGE - MAIN]]
