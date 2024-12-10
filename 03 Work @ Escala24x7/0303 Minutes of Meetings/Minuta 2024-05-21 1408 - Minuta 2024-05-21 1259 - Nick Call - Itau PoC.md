---
IDProyecto: "11105"
pilar: Escala24x7
type: Minuta
date: 2024-05-21
---
``

#minuta
## Fecha de Reunion
2024-05-21

## Asistentes

### Cliente
1. 
### Escala24x7
1. Carlos Leonel Ramírez
2. 

## Agenda

## Temas Discutidos
1. 

## Puntos de Acción acordados
1. 

## Proxima Reunión
1.  

`

#minuta
## Fecha de Reunion
2024-05-21


## Asistentes

### Cliente
1. 
### Escala24x7
1. Carlos Leonel Ramírez
2. 

## Agenda

## Temas Discutidos
1. Si la fecha para que Itau este listo pasa delMay 31th -  Necesitamos pedirle a Connectria y explicarle cuanto tiempo mas necesitamos.
2. Nick confirmara con ventas si el tiempo de pruebas puede ponerse en pausa o dividirse en 2.
3. Connectria tiene que instalar Mimix en el source system - puede ser en una sesion supervisada, pero si Connectria si necesitan tener credenciales - Nick va confirmar si es Root (sudo access) (Root is preferable)
4. Sesión con Fred (3pm Jueves - GMT-5)
	1. Fred puede 7am hasta 9:30am (GMT-5), 10AM - 12AM, 1PM - 3PM 
	2. Le va preguntar si es flexible para 3PM
5. Viernes disponibilidad de Fred
		1. cualquier hora
6. Nick necesita validar unas cosas con Preciseli, aprox 3 days to build LPAR2 once we have they have the files
7. Thread on Mimix (Puertos que se necesitan)
	- [x] Responder respuestas del cliente, sobre preguntas de Nick en Active Collab (tager Nick, Sean y Soon) #id11105 📅 2024-05-21 ✅ 2024-05-28





Para Mimix queremos abordar lo siguiente:

1. ¿Qué tamaño tiene la base de datos que se moverá con MIMIX?

La definición de los contenedores en la base de datos tiene un peso de 1 TB

El backup de la base de datos pesar aproximadamente 250 GB

2. ¿De qué tipo de base de datos se trata? (Oralce, Informix, DB2, etc.)

Sybase

3. ¿Dónde se encuentran los archivos de datos en el sistema?

File System y Rawdevice

4. ¿Están ubicados en sistemas de ficheros normales? (en algún lugar al que se pueda acceder mediante "cd")

Los que son File System (si)

5. ¿Están ubicados en volúmenes lógicos en bruto? (sólo /dev/<dispositivo>)

SI

6. Si se encuentran en dispositivos sin formato, ¿cómo se denominan los volúmenes lógicos?

Logical volumen (tipo raw) 85

7. ¿Cuántos sistemas de archivos o volúmenes lógicos componen la base de datos?

File system 4

8. ¿El servidor es de producción?

NO, es un ambiente de pruebas

9. ¿Con qué frecuencia se puede obtener tiempo de inactividad para el servidor?

El servidor estará dedicado a la POC , por los tanto los tiempos de actividad e inactividad son controlados por el equipo de la POC

 Adjunto las preguntas originales en inglés, en caso me esté perdiendo de algo en la traducción.

1. How big is the database that will be moving with MIMIX?

The definition of the containers in the database has a weight of 1 TB.
Database backup weighing approximately 250 GB

1. What type of database is it? (Oralce, Informix, DB2, ??)
Sybase

3. Where do the data-files live on the system?
File System y Rawdevice

5. Are they located in regular filesystems? (somewhere you can "cd" to)
Those that are File System (yes)

7. Are they located raw logical volumes? (just /dev/<device>)
Yes

9. If they are in raw devices, how are the logical volumes named?
Volumen lógico (tipo raw) 85

11. How many filesystems or logical volumes comprise the database?
File system 4

13. Is the server production?
NO, it is a test environment

1. How frequently can downtime be obtained for the server?
The server will be dedicated to the POC, therefore uptime and downtime are controlled by the POC team.