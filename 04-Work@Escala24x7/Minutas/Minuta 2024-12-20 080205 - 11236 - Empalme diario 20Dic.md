---
created: 2024-12-20T08:02:05
modified: '"2024-12-20 08:37", "5tc/G12T+6"'
date: 2024-12-20
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "11236"
---

`

### Seguimiento


 ```dataview
TASK WHERE contains(tags, "#id" + this.IDProyecto) AND contains(tags, "#followup") AND !completed
```


## Fecha de Reunion
2024-12-20

## Asistentes

### Cliente
* David Romero
* Santiago Bohorquez
* Darwin Arellano
* Nicolas Leon Perez
* Wendy D Manrique

## MC
- Juan Galeano
- Sergio Bonanno
- Martin Vasconcelos
- Nahuel Moyano
### Escala24x7
- Carlos Leonel Ramírez
- Jenny Rodriguez 

## Agenda
* Objetivo: Chequeo rapido de la arquitectura completa de PER, flujo completo
## Temas Discutidos
*  EL Datapower utiliza TLS (certificados)
* Martin Vasconselos envio ayer un diagrama con el flujo de la autenticación
* Dependencias de Technisys #risk #id11236 🚩 
* [ ] Es necesario validar si BEL generó el token #followup #id11236
	- Esto no esta en el alcance del proveedor del BEL
	- ![[Pasted image 20241220083029.png]]
	- David Romero hará la validación con Seguridad de la información
- La responsabilidad de la sincronización de usuarios (empresas) multilatina esta compartida entre PER y Control Center
	- ![[Pasted image 20241220083649.png]]
- Integración (enrolamiento) de soft-token regional
	- Esta como activació n 


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

## Grabación
- pendiente poner link
---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
