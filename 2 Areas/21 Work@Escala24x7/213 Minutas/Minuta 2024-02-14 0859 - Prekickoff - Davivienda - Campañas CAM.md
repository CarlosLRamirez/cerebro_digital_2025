``

#minuta
## Fecha de Reunion
2024-02-14

## Asistentes

### Cliente
1. 
### Escala24x7
1. Carlos Leonel Ramírez
2. 

## Agenda
### Apuntes previos
- Proyecto regional para 3 paises el cual debe ser facturado independiente en partes iguales a El Salvador, Costa Rica y Honduras
- Este proyecto contempla 1850 horas de implementacion y desarrollo
- Proyecto Whitelist: Proyecto de desarrollo de Escala24x7 e infraestructura, sobre las campañas y mensajes masivos de Davivienda para el ofrecimiento de nuevos servicios como extrafinanciamientos, entre otros. Este es un proyecto regional que esta contemplado para Honduras, El Salvador y Costa Rica, el despliegue sera dentro de la organizacion actual de Davivienda CECA. Contempla 1850 horas de implementacion y desarrollo.
- Stakeholders de Davivienda?

## Temas Discutidos
1. 

## Puntos de Acción acordados
1. 
Esquema de DevOps / Iaac:
- Terraform:
	- Ellos tienen modulos construidos en TF.
	- Se va trabajar con lineamientos del cliente.
	- Vamos a trabajar con las lineas bases de ellos.
	- Conocer esos lineamientos es una de las primeras sesiones el proyecto
	- Mario dice que esto va requerir horas 🚩
	- Jenny indica que esto ya esta considerado en las horas, y eso se tomo en cuenta con Andres 🚩
	- 1700 horas
		- 566h por pais
 - Es la misma organización con Davivienda
 - En el alcance no esta consumir esa API, solo habilitarla y notificar al Core
 - Las tareas estan mas del lado de dsarrollo
 - Davivienda tendra ingerencia en las herramientas de desarrollo?
	 - El banco tiene unas lenguajes ya avalados
 - Seguridad: checkpoint normal a nivel de seguridad e infraestura
	 - Jenny dice que si hay lineamientos de seguridad, con respecto a la habilitación del area de trabajo, inspeccion de codigo. Jenny va pasar el RFC, dice que eso lo validó del área de seguridad
	 - Implementar herramientas de análisis de código.
 - La solución es para los tres paises, solo se despliega una vez.
	 - solo un PaO.
 - Las cuentas no existen, hay que crearlas
- Repositorio del cliente
	- se va guardar en el repositorio del cliente
- La carga en S3 no esta en el alcance
- ⚠ hacer una matriz RACI
- Identificación de Stakeholders, toma de decisiones, involucrar a seguridad, devops, gestion de código, desarrollo
- 
## Proxima Reunión
1.  

`