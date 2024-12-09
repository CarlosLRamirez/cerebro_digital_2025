``

#minuta
## Fecha de Reunion
2024-01-12

## Asistentes

### BAM
- Manuel Hernandez
- Gerson Daniel Cruz
- Elder Enrique Lopez
- Erwin Orlando Ramírez

### Escala24x7
1. Edgar Lange
2. Luis Higuera
3. Christian Segovia
4. Carlos Leonel Ramírez

## Agenda
Definir el plan de acción para ejecutar las herramientas de discovery

## Temas Discutidos
1. Escaneo del universo completo de servidores de BAM (700)
	1. Se acordó ejecutar el escaneo a partir del martes 16 de Enero
	2. Se estima una duración máxima de 48h, esto basado en la vez anterior en la cual en 20h aproximadamente, escaneo el 97% se los servidores
	3. Esa actividad la puede ejecutar el equipo de BAM
2. Se definieron las preferencias globales de la herramienta MHER, de acuerdo a lo acordado, eso tiene influencia en las recomendaciones que entrega la herramienta, quedando de la siguiente manera:
	1. Objetivos empresariales priorizados
		1. Reduce operational overhead with managed services
		2. Modernize infrastructure with cloud native technologies
		3. License cost reduction
		4. Speed of migration
3. Luego de concluir el escaneo se identifican los siguiente pasos, los cuales pueden irse realizando de forma iterativa.
	1. Agrupar los servidores por aplicación individual o por etiquetas (pendiente definir la mejor estrategia)
	2. Configurar los parametros de Base de Datos
	3. Configurar los repositorio de Código para los servidores de aplicaciones
	4. Obtener recomendaciones de la aplicación o grupo de aplicaciones.
4. Se converso sobre la necesidad de apoyarse en las EVC para realizar esta clasificación, en caso de hacerse por aplicaciones individuales.
5. El equipo de infraestructura de BAM proveerá la información sobre la clasificación de servidores según el ambiente al que pertenecen.
6. Se acordó realizar una sesión el proximo lunes por la tarde para revisar el tema del secreto de las base de datos.

## Puntos de Acción acordados
- Realizar el escaneo de los 700 servidores nuevamente - BAM - 17/Enero
- Definir la estrategia para agrupar los servidores - Escala - 17/Enero
- Proveer la información sobre los servidores según el ambiente que pertenecen - BAM - 16/Enero
- Realizar una sesión el proximo lunes 15/Ene para revisar el tema del secreto de la base de datos - Escala/BAM - 15/Enero


1. Poner a correrlo el martes 16 y miércoles 17:
	1. La vez pasada, se inicio jueves 4pm, y el viernes a las 11:30am estaba en un 97%.
2. Luego debemos agrupar las aplicaciones, con las EVC

## Proxima Reunión
1.  15/Enero

`