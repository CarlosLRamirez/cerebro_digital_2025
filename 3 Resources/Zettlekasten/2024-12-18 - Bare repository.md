---
created: 2024-12-18T17:01:11
modified: '"2024-12-18 17:26", "3tc/G12T+6"'
type:
  - Zettelkasten
aliases: 
tags:
  - git
status:
  - in-progress
---
# Concepto
Un repositorio "desnudo" o *bare repository* es un tipo especial de repositorios en **Git**, el cual no tienen ningún *working tree* asociado, es decir no contiene los archivos del proyecto como tal, si no solo la información del repositorio (historial, ramas, etc..) almacenadas en el directorio `.git`.

## Analogia
Podríamos comparar un *bare repository* con los planos de una casa, contiene la información de como construir la casa, pero no la casa en sí.

## Puntos Clave
- Uno de los principales usos de un *bare repository* es para compartir un proyecto con otro usuario, quien podría "generar" nuevamente el working tree a partir de este repositorio.
- Tambien podríamos usarlo como backup, ya que podríamos regenerar todo el proyecto a partir de este directorio `.git`
- Un bare repository o puede ser editado directamente

## Ejemplo
- Podemos crear un *bare repository* con el comando `git init --bare`


--- 
 **Notas relacionadas:**
 [[2024-12-18 - Procedimiento de restauración a partir de un bare repository]]
 
 