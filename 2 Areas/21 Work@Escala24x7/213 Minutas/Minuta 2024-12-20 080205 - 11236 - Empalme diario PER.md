---
created: 2024-12-20T08:02:05
modified: '"2025-01-02 14:01", "4tc/G1T+6"'
date: 2024-12-20
type:
  - minuta
  - Minuta
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
* [ ] Martin Vasconselos envio ayer un diagrama con el flujo de la autenticación
* Dependencias de Technisys #risk #id11236 🚩 
* [x] Es necesario validar si BEL generó el token  #id11236 ✅ 2024-12-23
	- Esto no esta en el alcance del proveedor del BEL
	- ![[Pasted image 20241220083029.png]]
	- David Romero hará la validación con Seguridad de la información (riesgo)
	- En cada filial hay un equipo de riesgo
- La responsabilidad de la sincronización de usuarios (empresas) multilatina esta compartida entre PER y Control Center
	- ![[Pasted image 20241220083649.png]]
- Integración (enrolamiento) de soft-token regional
	- Esta como activación de semilla
	- Tenemos que ver el detalle de esa integración
- [x] Reunión con el tercero para cerrar el alcance de single sign-on #id11236 #followup ✅ 2024-12-23

## Puntos de Acción acordados
- [x] David Romero pasará el diagrama de referencia de la arquitectura completa de PER #followup #id11236 ✅ 2024-12-23
- [x] A la espera de los WSDL #followup #id11236 ✅ 2024-12-23
- [x] Definir cronograma de actividades entre PMs #followup #id11236 ✅ 2024-12-23





## Proxima Reunión
*   

## Grabación
- pendiente poner link
---
