``

#minuta
## Fecha de Reunion
2024-01-18

## Asistentes

### Davivienda
1. Alan Giovanni Garibello Andrade
2. Carolina Vanessa Morales Calderón
3. David Chaparro Zuñiga
4. Edward A Alfonso Castellanos
5. Edwin Perilla Fino
6. Fernando Alfo Guerrero Alvarado
7. Ivan Dario Zambrano Zambrano
8. Nicolas Medrano Poveda
9. Orlando Lucas Lucas Peña
10. Sandra Milena Ojeda Pineda
### Escala24x7
1. Carlos Leonel Ramírez
2. Jenny Rodriguez
3. Johan Blanco

## Agenda
- Despliegue de Infraestructura AWS - Región de Ohio
- Recursos ya desplegados por Escala24x7 en la Región de Ohio
- Despliegue de servidores NGINX para la region de Ohio
- Accesos a la consola AWS para el equipo de Ciberseguridad.
## Temas Discutidos

### Infraestructura AWS  para Seguridad Perimetral -  Región de Ohio:
- Se revisó el diagrama de arquitectura enviado por Davivienda para los recursos a desplegar en la región de Ohio
- Davivienda indica que necesita que se creé una cuenta llamada CIBERSEGURIDAD
- Davivienda indica que utilizará una VPC con 8 subredes, distribuidas en 2 AZ.
- David de Davivienda solicita conocer el estado de la configuración del Direct Connect, para lo que solicita tener una sesión técnica.
- Davivienda indicó que desplegará un GTWLB y 2 FW zona Sur, y 2 FW zona Norte (los 4 Palo Alto)
- Los FW zona Norte serán para la inspección de trafico, y los FW zona Sur serán para le manejo de VPNs.
- Se desplegara un NAT GW para dar salida a internet a los FW, y un ALB para publicaciones.
- Davivienda indicó que ah tenido avances en la definición del esquema de red a utilizar en esta VPC.
- **Davivienda confirmó que su alcance es que  ellos desplegaran los recursos de la Seguridad Perimetral en Ohio y Escala implementaría la solución de  DR para Cyberbank Centroamerica.**
### Recursos ya desplegados por Escala24x7 en la Región de Ohio
- Johan Blanco de Escala24x7 confirma que ya se tienen una cuenta desplegada (SHARED) y que ya se desplegó un VPC, subredes, Transit Gateway y Direct Connect,  de acuerdo al direccionamiento enviado por Davivienda el año pasado.
- Davivienda confirma los CIDR enviados en año pasado a Escala **YA NO VA**, y que están trabajando en definir nuevos segmentos.
- Por lo anterior, Johan confirma que es necesario destruir los recursos que ya se tenían desplegados.
- Johan Blanco comentó que todo esta implementado por plantillas de infraestructura como códigos, Davivienda indica que ellos no cuentan con plantillas.
### Despliegue de servidores NGINX para la region de Ohio
- El equipo de Ciberseguridad Davivienda indicó no tener mayor contexto sobre los NGINX implementados.
- El señor Ivan Zambrano describió de forma general la funcionalidad de los NGINX como proxy reverso en la región de Virgina.
- Se acordó realizar una sesión técnica para describrir a detalle la arquitectura implementada en Virgina.
- Es necesario definir si los NGINX se implementaran como parte de la arquitectura de seguridad perimetral en Ohio.
### Accesos a la consola AWS para el equipo de Ciberseguridad.
- Johan confirmó que el dia de hoy estaría habilitando los accesos para el personal de Davivienda solicitado.
- David indicara los permisos que requiere el personal de Davivienda.
- Ivan Zambrano expresó la autorización para que Orlando Lucas pueda crear tickets, así como autorizar la creación de infraestructura, y solicitar accesos adicionales.
## Puntos de Acción acordados
1. Coordinar una proxima sesión técnica de 1.5h, para tratar los siguientes temas (Fernando y Carlos)
	1. Revision a profundidad de la arquitectura implementada
	2. Revision de la configuración actual del Direct Connect
	3. Revision de la implementación de los servidores NGINX.
2. Confirmar los permisos requeridos para el personal de Davivienda. - David (Davivienda)
3. Configurar los permisos solicitados y habilitar a Orlando como autorizador - Johan (Escala)

## Proxima Reunión
1.  Por Definir


Interno:
- Como queda el soporte?`