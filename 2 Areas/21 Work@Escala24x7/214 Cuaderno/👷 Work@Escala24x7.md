---
created: 2024-12-13T15:13:00
modified: '"2025-01-09 10:20", "4tc/G1T+6"'
type: 
aliases:
  - Work@Escala24x7
tags:
  - Escala24x7
---
# 👨‍🏭 HOME - Escala24x7

- [[Gestión de Tareas de Trabajo]]
- [[2024-23-12 Shortcuts Escala24x7]]
- 


## Tareas

```dataview
TASK
FROM "04-Work@Escala24x7"
WHERE !completed
WHERE due <= date(today)
WHERE !contains(tags, "#followup")
GROUP by tags
```


[[2024-23-12 Shortcuts Escala24x7]]
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
[2024-23-12 Shortcuts Escala24x7](2024-23-12%20Shortcuts%20Escala24x7.md)



-----
[[2024-12-13 - Workflow - Gestion de Proyectos y Tareas Escala24x7]]



---
[[🏠 HOMEPAGE - MAIN]]
