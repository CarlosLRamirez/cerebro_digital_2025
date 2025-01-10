---
created: 2025-01-09T08:02:24
modified: '"2025-01-09 08:04", "4tc/G1T+6"'
date: 2025-01-09
type:
  - minuta
IDProyecto:
  - "11236"
---

#minuta 
#id11236
## Fecha de Reunion
2025-01-09

## Asistentes

### Cliente
* Diego Felipe Garcia
* Vanesa Hernandez
* Nicolas Leon
* David Santiago Bohorquez
* Darwin Arellano
* Wendy Manrique
### Escala24x7
- Carlos Leonel Ramírez
-  Jenny Rodriguez
- Johan Blanco

### Mobile
- Juan Galeano
- Nahuel Moyano

## Agenda
* Empalme diario PER
## Temas Discutidos
*  Ayer estuvieron revisando el flujo para autenticación para SoftToken, generaron un diagrama
	* https://drive.google.com/file/d/1i1xvhFSBy217cmX2p523E6PGKdfC5VdA/view?usp=drive_web
	* Se ajusto el flujo
	* El diagrama este el mismo archivo de Lucid del proyecto (pestaña Flujo Sesión Usuario)
	* Dudas con Activación de Semilla Token Softtoken
		* Esta antes de la selección de Empresa
		* Según Nahuel esta en una zona gris, porque uno ya esta en el modulo regional. Darwin dice que esto va de parte de Mobile.
			* Dicen que eso no lo habían incluido, pero lo van estar incluyen mas adelante. #followup #id11236
		* Cuando el usuario aprieta el botón, la aplicación debe validar si el usuario tiene softtoken, hardtoken.
		* Cuando el cliente venga de la banca en linea la app ya debe saber que tipo de token tiene el usuario.
		* La app debe tener el serial del token.
		* David Bohorquez nos enviará las especificaciones técnicas de los servicios de autenticación #followup #id11236
		* Jenny considera tener sesiones con los proveedores del SSO #followup #id11236
	* Inquietudes sobre el ingreso de Miami #id11236 #followup 
	* Jenny dice que con esos ajustes el flujo esta en firme, y va confirmar la base de servicios para que vayamos mapeando los endpoinds.
* Nico dice que el día de esperan dejar la solicitud de las licencias de Github, ya se crearon los grupos.
* Se recuerda los CIDRS.

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---

## Related Notes
[[Investigar como funciona el tema de autenticacion hardtoken y softtoken]]
