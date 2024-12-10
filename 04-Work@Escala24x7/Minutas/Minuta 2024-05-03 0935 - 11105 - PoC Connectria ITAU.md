``

#minuta
## Fecha de Reunion
2024-05-03

## Asistentes

### Cliente
1. Emiro Zabala
2. Erik Giancarlo Ruiz Lopez
3. William Hebert Castro
4. Carlos Rafael Gamez Amaya

### Escala24x7
1. Carlos Leonel Ramírez
2. Antonio Florez
3. Cesar Gomez
4. Jeremy Enciso

## Agenda

## Temas Discutidos
1. Usuario de Sterling / Carga de imágenes
	1. Ya enviamos la información de cédula de Cesar Gomez para la creación del usuario
	2. En espera de recibir la información del usuario, Emiro indica que el proceso de  toma de 2 a 3 días.
	3. Posteriormente se cargaran los archivos de las imágenes
2. Comunicaciones/Definición de CIRDS
	1. El contactó de Itaú para los temas de comunicaciones es Juan Camilo Garcia 
	3. Es necesario definir las IPs/segmentos red a utilizar para de Connectria y AWS
	4. En la solución actual todo esta en un mismo segmento de red.
	5. Para la PoC es probable que eso no se pueda replicar, eso se debe definir con Juan Camilo García
	6. Emiro reenviará a Juan Camilo Garcia le correo con las consultas de comunicaciones
3. Cuentas de AWS para el despliegue de Infraestructura
	1. Es necesario definir las cuentas donde se desplegaran los recursos de AWS
	2. La recomendación de Escala24x7 es crear una cuenta nueva para este proyecto.
	3. Se confirmo durante la sesión que el formato que se necesita es un archivo .OVA
4. Mimix / VPN RMM
	1. El tema de la VPN de RMM se debe validar con el equipo de comunicaciones
	2. Con respecto a la gestión de la infraestructura del banco, Emiro menciona que no esta autorizado la gestión de un tercero, cualquier cambió o configuración a realizar la hace Itaú con la guía o acompañamiento del proveedor, en este caso Connectria/Escala.
	3. Emiro escalará este tema para validar si existe alguna alternativa para esta PoC.
5. Mimix  / Sybase
	1. Se debe confirmar la compatibilidad de Mimix con la versión de base datos Sybase con la versión que tiene Itaú
	2. Antonio Florez indicó que podemos enviar una respuesta formal, confirmando dicha compatibilidad
6. Sybase
	1. Es necesario involucrar al DBA para empezar a gestionar las licencias temporales de Sybase
	2. La función del DBA es ayudar a Connectria a que el motor suba y gestionar las licencias temporales

## Puntos de Acción
- Incluir al Alvaro Lopez (DBA) en las proxima reuniones. - Brenda/Emiro
- Incluir a la persona de Itaú encargada las cuentas de AWS en la proxima reunión.  Brenda/Emiro
- Involucrar a personal de comunicaciones en la próxima reunión (Juan Camilo Garcia)  Brenda/Emiro
- Generar el usuario y empezar a subir los archivos - Emiro
- Enviar por correo el formato para la imagen de VMware - Jeremy Enciso 

## Proxima Reunión
1.  Lunes 6/05/2024

`