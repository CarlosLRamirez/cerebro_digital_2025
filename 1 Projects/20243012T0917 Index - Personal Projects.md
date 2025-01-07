---
created: 2024-12-30T21:17:30
modified: '"2025-01-07 07:13", "2tc/G1T+6"'
type:
  - Index
aliases: 
tags:
  - projects
---

## Proyectos Activos

[[20250107T0715 Proyecto Certificación Github Fundamentals|Proyecto: Certificación Github Fundamentals]]


```dataview
list
from "1 Projects"
where contains(type, "project") and contains(status, "in-progress")
```

```dataview
LIST
WHERE contains(file.text, "#project")
```

## Backlog de proyectos

```dataview
list
from "1 Projects"
where contains(type, "project-main") and contains(status, "not-started")
```

## Proyectos Finalizados

```dataview
list
from "1 Projects"
where contains(type, "project-main") and contains(status, "completed")
```

----
## Todos los proyectos
```dataview
table status as "Status"
from "1 Projects"
where contains(type, "project-main")
```

___
[[🏠 HOMEPAGE - MAIN]]
