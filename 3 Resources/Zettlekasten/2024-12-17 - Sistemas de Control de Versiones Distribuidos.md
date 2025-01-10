---
created: 2024-12-17T15:07:40
modified: '"2025-01-08 07:36", "3tc/G1T+6"'
type: 
aliases:
  - Sistemas de Control de Versiones Distribuidos
tags:
  - git
---
## Definición
En un sistema de control de versiones distribuido **todo el historial del proyecto** es almacenado tanto en el cliente como en el servidor (esta "*distribuido*" en todos los clientes, ademas del servidor central)

## Principales ventajas
- Permite que podamos editar los archivos sin tener conectividad con el servidor central, confirmar los cambios localmente y sincronizar con el servidor una vez esté en linea nuevamente, por lo anterior podemos decir que pueden trabajar completamente "offline".
- Si ocurre algo en el servidor con el repositorio central, los clientes poseen una copia local del proyecto; por lo que son más tolerantes a fallas.
- En general tienen mejor rendimiento que los [[2024-12-17 - Sistemas de Control de Versiones Centralizados|Sistemas de Control de Versiones Centralizados]] 
- El *branching* y *merging* es mas eficiente y directo. 

![[Pasted image 20241217154607.png]]

--- 
 **Notas relacionadas:**
[[20241218T0949 Git|Git]]


**Referencias:**
https://medium.com/@pm74367/types-of-vcs-version-control-system-f7af5594bd04
https://learn.microsoft.com/en-us/training/modules/intro-to-git/1-what-is-vc


 