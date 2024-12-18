---
created: 2024-12-18T13:13:57
modified: '"2024-12-18 16:22", "3tc/G12T+6"'
type:
  - Zettelkasten
aliases: 
tags:
  - git
status:
  - in-progress
---

## Concepto
Es el área en donde están todos los archivos y estructura de carpetas que forman parte del proyecto. Es como esa "area de maniobras" o "*staging area*" en donde hacemos todos los cambios que necesitamos en nuestros archivos (como editar, agregar, borrar, etc..) antes de confirmarlos (hacer *commit*) en el repositorio.

## Puntos Clave
- El Working Tree refleja el estado actual del proyecto (archivos y carpetas).
- Todos los cambios que se realizan en el working tree no son rastreados por Git hasta que no son puestos en escena (*staged*)
- El comando que nos sirve para ver los cambios realizados en el working tree es `git status`
- El comando para hacer *stage* de los cambios en el working tree es `git add`


--- 
 **Notas relacionadas:**
 [[Staging Area]]
 [[Local Repository]]
 [[2024-12-18 - Commit]]
