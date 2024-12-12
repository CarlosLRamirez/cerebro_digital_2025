---
created: 2024-12-12T08:05:07
modified: '"2024-12-12 10:05", "4tc/G12T+6"'
date: 2024-12-12
type:
  - daily-note-escala24x7
aliases: 
tags:
  - Escala24x7
---
**Entrada de diario:** 
Hoy es jueves 12 de diciembre, estamos en la semana 50 del año 2024

> Aquí escribe todo lo que necesites relacionado a Escala24x7


## Tareas para hoy
- Ponerme al dia de los proyectos
- Hablar con Rafa al final del dia
- Configurar la plantillas para minutas Escala

## Registro de tiempo
8:00 inicie con revision de los chats de proyectos, principalmente PER y Cempro, ah y ver un poco Bancolombia
9:00 reunion con Frank para revisar PER
9:30 termine con Frank, me puse a ver lo de la gestion de minutas
10:00 hay una reunion de PER

## Apuntes Proyectos

### 11236-Davivienda-PER #id11236

- Hoy es la primera sesión técnica entre Dav, MC y Escala24x7 a mis 10am
- A las 9 programé una sync previa con Frank
- Cuadro Resumen al dia de hoy: https://docs.google.com/spreadsheets/d/1d_elL-W5sRhfpDWoLm_8fQopYCPJsZcJYY1ySIFu_Kg/edit?gid=0#gid=0
- El Kickoff con el cliente fue el martes 10/Dic - Buscar la grabacion
- [ ] Buscar grabaciones de Kickoff y Prekickoff #id11236
- Matriz Raci. https://docs.google.com/spreadsheets/d/1O1jAzv0Ce6NdZIB3_utt-5omStVyI5EjQIc8057rC4I/edit?gid=0#gid=0 -- Esta vacia 😀
	- hay que marcar bien quienes son los responsables, por ejemplo, de seguridad perimetra (Davi CO), publicacion de las apps (Davi CO), devops (Davi CO), etc
- [ ] Completar la Matriz RACI - Gestionar #id11236
- Presentacion de Kickoff: https://docs.google.com/presentation/d/1ijw8Jg_yd7rZFv_BgKHDpiiHjZ4jCnFENQIkNs4WXT0/edit#slide=id.p1
- Plantilla Backlog:  https://docs.google.com/spreadsheets/d/1xAVlg8fVIGKjSWj7J1id53kNlgxX7QrULvLEpqYaRQ4/edit?gid=1120027636#gid=1120027636 -- Esta vacia 😀

[[Minuta 2024-12-12 094303 - Sync con Frank]]




### 10854 - Cempro #id10854
- Según el ultimo informe ya se terminaron las migracions Lift & Shift
- Solo queda pendiente la ventana para la salida a producción de APP Ruteo
- [ ] Confirmar con Jhonatan y resto del equipo #id10854
- [ ] Como quedaron los PaO? #id10854
- [ ] Hubo un issue con la aplicacion de marcajes? #id10854

## Otros temas
- Performance Review 2024 https://drive.google.com/file/d/1kNEYfFGPQoYBtp02nbMy-JB9xZVnpV_R/view?usp=sharing
- Convivio Escala24x7 el jueves 19 de Diciembre
- 

### Minutas del dia

 ```dataview
table date as "Fecha de Reunión", IDProyecto as "ID del Proyecto"
where type contains "minuta"
sort date asc
```

from "/04-Work@Escala24x7/Minutas"
and date = date(this.file.frontmatter.created)
----
**Notas relacionadas:**