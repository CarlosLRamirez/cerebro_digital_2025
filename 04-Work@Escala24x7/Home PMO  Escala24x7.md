---
cssclasses: []
ultima-modificacion: 2024-12-13T08:31:02-06:00
modified: '"2024-12-13 08:33", "5tc/G12T+6"'
---


# 👨‍💼 HOME - Escala24x7

[[20241119 1249 - Enlaces Escala24x7]]
[[20241119 1317 - Registro de horas]]



## Proyectos Escala24x7

[Indice de Minutas](Indice%20de%20Minutas.md)

### Activos

```dataview
TABLE IDProyecto, statusProyecto
from "04-Work@Escala24x7/ProyectosEscala24x7"
where type = "proyecto" and statusProyecto = "Activo"
sort IDProyecto asc
```

### Cerrado, Transferidos o Cancelados

```dataview
TABLE IDProyecto, statusProyecto
from "escala24x7/proyectos"
where type = "proyecto" and (statusProyecto = "Cerrado" or statusProyecto = "Cancelado" or statusProyecto = "Transferido" or statusProyecto = "Suspendido")
sort IDProyecto asc
```

### Todos  los proyectos

```dataview
TABLE IDProyecto, statusProyecto
from "escala24x7/proyectos"
where type="proyecto"
sort asc
```


## Accounts
### Davivienda CECA
- [Carpeta Arquitectura](https://drive.google.com/drive/folders/1D-QKvglLwwTeO6GmhitXAkN0pkraHXOu?usp=drive_link)
## Enlaces  
[20241119 1249 - Enlaces Escala24x7](20241119%201249%20-%20Enlaces%20Escala24x7.md)

