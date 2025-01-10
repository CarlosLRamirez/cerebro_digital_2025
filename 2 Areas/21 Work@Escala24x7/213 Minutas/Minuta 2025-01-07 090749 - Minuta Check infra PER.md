---
created: 2025-01-07T09:07:49
modified: '"2025-01-07 09:15", "2tc/G1T+6"'
date: 2025-01-07
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "11236"
---
#minuta 
#id11236

`


## Fecha de Reunion
2025-01-07

## Asistentes

### Cliente
* David Santiago Bohorauez
* Deigo Felipe Garcia 
* Nicolas
* Vanesa
### Escala24x7
- Carlos Leonel Ramírez
-  Ilinaa
- Jenny
- Johan

## Agenda
* 
## Temas Discutidos
1. Aún se esta refinando la arquitectura
	1. Falta aclarar el softtoken, reunión el jueves
	2. Falta aclarar lo de SSO, esta pendiente una sesion con cyberseguridad
2. Ya solicitamos las licencias
3. Definición de espacios de trabajo (codespaces) [[Que son los codespaces]]
	- Eso lo define Davivienda

De acuerdo a estas definiciones, se generan las siguientes preguntas con respecto a la infraestructura
1. Servicio a detalle utilizados y/o funciones en AWS?
	- No hay formato, queda libre - Jenny
2. Relación de rutas de logs de servicios
	-  Cloudwatch y Cloud Trail - Jenny
4. Relación de Errores conocidos
	- Glosario de Errores que puedan ocurrir en este ambiente?
	- Se orientaría a los servicio de AWS (infraestructura)
	- Jenny
5. Alcance de contrato, si hay algunos por favor enviarlo
	1. Nico
6. Vulnerabilidades, resultados de escaneo y remediaciones
	- En whitelist se utilizó ORCA
	- Se corren los servicios de AWS del Baseline de Seguridad
	- Jenny y Johan
7. Relación de costos detallados por filial, entendimiento de lo que será facturado a cada filial ya que es un único canal
	- Se facturá porcentual
	- Eso es de Nico
8. Definición de SLA para escalamiento
	- Esta en el ANS de Davivienda, podriamos consultarlo
	- Nico y David Santiago
9. Manejo de reportería e historicos
	- Toca mirarlo con Martín (definir en app)

![[Pasted image 20250107091938.png]]

- Dynatrace #followup #id11236 
## Puntos de Acción acordados
-  Jenny empezará a trabajar en la semana en la matriz, y la revisamos el viernes en el espacio de las 9. #followup #id11236


## Proxima Reunión
*   

----
# Conversacion post-Reunión

 - Johan
 - Jenny
 - Carlos Ramírez

- El jueves tienen una sesión para ver el tema de ciberseguridad, con respecto a la inspección
- Johan pregunta sobre el bucket S3 para el front-end?
	- Esta pendiente que nos definan si el sitio queda público, tienen que pasar por Imperva si o si. Que nos quede por aprobado por escrito #id11236 #followup

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---
