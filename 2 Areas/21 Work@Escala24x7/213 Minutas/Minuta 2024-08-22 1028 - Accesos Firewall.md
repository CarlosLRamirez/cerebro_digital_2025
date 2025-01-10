---
type:
  - minuta
IDProyecto: "11152"
date: 2024-08-22
---

## Fecha de Reunion
2024-08-22

## Asistentes

### Bancolombia
* Jose Palacio Holguin (Cirion Technologies)
* Jhang Gaviria (Axity)
* Jossie Piza Rada (Cirion Technologies)
* Tatiana Snachez Londono
* Andres Felipe Ramirez
* Oscar Mauricio Morales
* Antonio Jose Florez
* Luis Alfredo Nieto
### Escala24x7
- Carlos Leonel Ramírez
### Connectria
- Roy Flowers
- Jason Waller
- Fred Luber

## Agenda
* Definir esquema de conexión para la administración de los Firewalls en Connectria.
## Resumen

En la reunión se discutieron varios temas relacionados con la configuración de la red. Se habló sobre la necesidad de agregar dos nuevas interfaces en los Versa gateways y se aclararon dudas sobre la configuración de VNICs. También se discutió la posibilidad de habilitar Internet en los firewalls de Conectria para el tráfico interno y se planteó la posibilidad de proporcionar acceso a Internet a través de SD-WAN, con opiniones divididas sobre la viabilidad y los riesgos asociados. Además, se abordó la necesidad de realizar cambios en la configuración del firewall y el gateway, y se estableció que se dejará listo al menos el ambiente pre-productivo esa noche, con la posibilidad de realizar pruebas al día siguiente.

Durante la reunión, se discutieron preocupaciones sobre el impacto potencial en la infraestructura y se acordó realizar las configuraciones necesarias después de las 8 de la noche para minimizar riesgos. También se mencionó la importancia de contar con los permisos necesarios en el Firewall Cloud y se estableció la necesidad de un punto de control al día siguiente para revisar la efectividad de la configuración. En general, se discutieron varios temas importantes relacionados con la configuración de la red y se tomaron decisiones importantes para avanzar en la implementación de los cambios necesarios.

## Temas Discutidos

**Discusión sobre la configuración de interfaces y VNICs en Versa gateways.**
Carlos Leonel Ramirez Martinez consultó a Fred y Roy sobre la revisión de un correo electrónico, mientras Tatiana Sanchez Londono preguntó si habían visto el correo enviado el día anterior. Se discutió la necesidad de agregar dos nuevas interfaces en los Versa gateways, y se aclararon dudas sobre la configuración de VNICs, con participación de Andres Felipe Ramirez Restrepo, Fred Luber, y Palacio Holguin, Jose.
* Acceso al firewall a través del SD-WAN
* Configuración de interfaces en el Versa
* Creación de VNIC para administración

**Discusión sobre la habilitación de Internet en los firewalls de Conectria.**
Oscar Mauricio Morales Castano y Andrés Felipe Ramirez Restrepo debatieron sobre la viabilidad de obtener Internet desde Niquia para los firewalls de Conectria. Se destacó la necesidad de establecer un control sobre el tráfico de salida y se mencionó la posibilidad de habilitar un gateway en la salida a Internet.

**Discusión sobre la salida a Internet a través de SD-WAN**
Carlos Leonel Ramirez Martinez, Roy Flowers, Fred Luber, Oscar Mauricio Morales Castano y Tatiana Sanchez Londono debatieron sobre la opción de proporcionar acceso a Internet a través de SD-WAN, con preocupaciones sobre la seguridad y la viabilidad técnica.

**Discusión sobre la infraestructura de red y seguridad.**
Luis Nieto plantea la posibilidad de enviar logs a la nube de Palo Alto, lo que genera un debate sobre la conveniencia de tener el canal de internet en Conectria. También se discute la administración de los panoramas y la segmentación de infraestructuras en la nube.

**Discusión sobre las opciones de enrutamiento de tráfico de Internet**
Durante la discusión, Oscar expresa su preocupación sobre el cambio de direccionamiento IP y la posible inmanejabilidad del tema. Luis propone la alternativa de utilizar Direct Connect hacia AWS para la salida del tráfico, 
* Uso de Panorama para administración de firewalls

**Discusión sobre cambios en la configuración de firewall y gateway.**
Roy Flowers destacó la importancia de dirigir cualquier pregunta a Fred y a él mismo después de la llamada. Se planteó la posibilidad de eliminar interfaces y reconfigurar las IP públicas, así como la necesidad de cambiar el default gateway para apuntar a la Versa en lugar de la misma firewall. Se discutió la viabilidad de realizar estos cambios antes de habilitar el tráfico.

**Discusión sobre la habilitación de las interfaces de producción y no producción.**
Oscar y José acuerdan habilitar ambas interfaces, considerando posibles riesgos. Se decide dejar listo al menos el ambiente productivo y se establece que la configuración se realizará esa noche.

## Puntos de Acción
* El Equipo de Telco configurará las interfaces en el Versa para separar los datos y la administración de los firewalls.
* El Equipo de Telco configurará las rutas y gateways para habilitar el acceso a Internet de forma segura.
* El Equipo de Cyberseguridad utilizará Panorama para administrar los firewalls de manera eficiente, mientras se define la forma en que los FW saldrán a Internet.


## Proxima Reunión
*   Por Definir

---
🎶
Author: Carlos Ramírez - 2024

