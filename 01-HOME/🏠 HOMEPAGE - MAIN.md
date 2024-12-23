---
created: 2024-12-09T18:27:08
modified: '"2024-12-23 09:13", "1tc/G12T+6"'
type:
  - Home
  - TOC
aliases: 
tags: 
---
# 🏠 Home
Bienvenido a mi Vault principal, donde manejo mi productividad y mi sistema de conocimiento.

## 🌟 Acceso Rápido
- [[👷 Work@Escala24x7]]
- [[📚 Gestión de Conocimiento - Pagina Principal]] 
- [[2024-12-20 - Task Manager]]



## Paginas Recientes
```dataview
TABLE file.mtime AS "Last Modified"
FROM "" 
SORT file.mtime DESC
LIMIT 10
```



------


- 📝 [[01-Quick Notes]] (Notas rápidas y captura de ideas)
- 📅 [[02-Productividad]] (Tareas, proyectos y planificación)
- 💼 [[👷 Work@Escala24x7]] (Notas de mi trabajo principal)

- 🗂️ [[05-Archive]] (Proyectos y notas finalizadas)


## 📈 Sistema de Productividad
- 📋 [[02-Productividad/0201-Tareas]] (Gestión de Tareas)
  - Tareas pendientes: `dataview-inline` 
    ```dataview-inline
    task from "02-Productividad/0201-Tareas" where !completed
    ```
- 📂 [[02-Productividad/0202-Proyectos]] (Gestión de Proyectos)
  - Proyectos activos: 
    ```dataview-inline
    table file.name as "Proyecto", status
    from "02-Productividad/0202-Proyectos"
    where status = "Activo"
    ```
- 📓 [[02-Productividad/0203-Journal]] (Entradas diarias y planificación)


## 🧠 Sistema de Conocimiento
- 📂 [[04-Knowledge/0401-Zettelkasten]] (Ideas y conceptos interconectados)
  - Últimas notas creadas:
    ```dataview-inline
    list from "04-Knowledge/0401-Zettelkasten"
    sort file.mtime desc
    limit 5
    ```
- 📚 [[04-Knowledge/Referencias]] (Libros, artículos, y recursos)
- 🔗 **Explorar conexiones**: 
  - [[20241123 - Concepto 1]]
  - [[20241122 - Concepto 2]]

## 🔄 Revisión
- 📅 [[Revisión Semanal]] (Pendientes y logros de la semana)
- 📅 [[Revisión Mensual]] (Análisis de objetivos y resultados)


## ⚡ Acciones Rápidas
- ✍️ [Nueva Tarea](command:quickadd:add-tarea)
- 📓 [Nueva Nota Diario](command:templater:create-note)
- 📚 [Nueva Nota Zettelkasten](command:quickadd:add-zettel)


