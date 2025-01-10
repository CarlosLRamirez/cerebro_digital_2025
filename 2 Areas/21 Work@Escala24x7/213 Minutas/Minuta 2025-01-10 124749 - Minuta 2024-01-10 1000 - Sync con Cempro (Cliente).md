---
created: 2025-01-10T12:47:49
modified: '"2025-01-10 12:48", "5tc/G1T+6"'
date: 2025-01-10
type:
  - minuta
IDProyecto:
  - "10854"
---

#minuta 
#id10854

## Fecha de Reunion
2024-01-10
## Notas de Reunion interna

Proxima 2 semanas: --> Participar de la Sync interna con el equipo: Fecha xx para revisar estatus de temas --> Participar de la Sync semanal con el cliente Miercoles 10/1 1.00pm (la semana del 3/1 se pidio suspender) - minuta si surgen compromisos y gestionar sesiones tambien si fueran requeridas durante la sesión. 

Contexto --> Principales 3 temas princiaples a hacer seguimiento: 1. avanzar con la implemtacion de Amazon SES(a partir del 15/1)  2. avanzar con la modernizacion de 3 Apps (Beatriz) y 3. Analizar alternativa de Fortinet en nube para mejorar el balanceo de carga (Juan K tiene que pasar propuesta) 

-->Luego podria mencionar como 4 Tema, Avanzar con CCoE. 
- Posiblememte sea necesario seguir escalando con Martin de AWS, Jenny y con Juan Carlos / Eduardo (comerciales de Escala) que compartan detalles de la autoria de McKinsey y arrancar con la planificacion para CCoE. (por parte de Cempro el tema lo lleva Hugo Bran o directo a Jose (CEO)

## Temas Discutidos
1. Data:
	1. No hay nada, hasta que el cliente no se reporte, a partir del 15/01
	2. Lo nuevo que se esta agregando es desde 0
	3. Seria bueno hacer un especie de Kickoff
	4. Se quiere implementar dashboard de Quicksight del servicio SES
		1. Van haber dos iniciativas: 
			1. SES
			2. Modernización de 3 aplicaciones, ya se tuvieron las sesiones de recolección de información, ya se les presentó la arquitectura.
	5. Queda pendiente que definan el tipo de repositorio.
		1. Se definió que será ECR
2. Jose Abzum:
	1. Se va asignar a Xavier Encarnación para el proyecto de modernización de las Apps
	2. Jose le dio toda la inducción, las aplicaciones, donde están los artefactos
	3. Con José van a ver el tema del Backlog
3. Fortinet
	1. es mas un tema comercial.

Puntos de seguimiento
- SES
- Modernización
- Fortinet (Balanceo de Carga) 

- [x] preguntarle a Juan Carlos sobre Fortinet - CEMPRO #id1854-CEMPRO ✅ 2024-01-25

## Notas de la Sesión


- Modernización
	- Se tuvo una sesión hace dos semanas, se solventaron algunas dudas
	- Xavier Encarnación es el encargado de realizar esa modernización, ya tenemos la experiencia de una modernización en Wordpress.
	- Ayer se terminó el backlog de la primera aplicación.
	- Hoy en la tarde se tiene una sesión interna para empezar con el tema de landing zone, y empezar a generar los repositorios iniciales.
	- Les vamos a enviar un correo para que provean las fuentes de las tres aplicaciones, queremos priorizar en una, Cempro indica que quiere iniciar con la de ruteo. (no Cempro ni Mixtolisto, la tercera)
	- La aplicación es transaccional.
	- El siguiente paso es solicitar las fuentes.
	- Se confirma que ya esta actualmente en un RDS, necesitamos confirmar en que RDS esta.
	- Se confirman las cuentas a utilizar.
	- Empezaríamos en desarrollo, actualmente solo existe RDS en Produccion y QA, toca crear Desarrollo (xx97).
- SES
	- Se va iniciar el 15 de enero, el despliegue de SES (regresa Jonathan)
	- Luego Natalhy trabajará en la parte de data.
- Fortinet
	- Estamos a la espera de Juan Carlos


