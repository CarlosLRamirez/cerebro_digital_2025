---
created: 2025-01-02T14:33:20
modified: '"2025-01-02 14:38", "4tc/G1T+6"'
date: 2025-01-02
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "11221"
---
## Fecha de Reunion
2025-01-02

## Asistentes

### Davivienda
* David Chaparro Zuñiga
### Escala24x7
- Carlos Leonel Ramírez
-  Raul Aquino
- Oscar Eduardo Gonzalez

## Agenda
* 
## Temas Discutidos
*  

## Puntos de Acción acordados
- Status despliegue de Ciberseguridad
	- Los Firewalls serán administrados por los Panorama existentes, en Azure, van a levantar  una VPN contra el TGW de AWS, el objetivo es que queden centralizados
	- Esta semana el objetivo es levantar las VPN, desplegar los FW 
	- Dice que no hay alertamientos con las fechas estimadas (11 de enero). Pendiente consultar con Fernando el status de Cyberark
- Pruebas de integración
	- Terminada la implementación de los TGW, ya se podrían hacer pruebas entre cuentas de AWS Ohio - Ohio
	- Comunicación con otra region con SSI o SSA
- Pruebas on-premise
	- Debemos coordinarla con esta persona:  Juan J Mendoza Soler <jjmendozas@davivienda.com> 
		- Actualizar cronograma con actividades on-premise
	- Eso tocaría hacerlo a las 10pm
	- David dice que la VPN la levantan en un día.
	- Ya entregados los FW estos pasan a operaciones
	- El freeze termina el lunes 13 de enero.
- El mejor escenario es que el 22 este el canal con SSI y SSA
- Daniel Bernal es el líder de operaciones del SOC
	- Hay una persona que hay que darle de baja
## Proxima Reunión
*   

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---
[[2025-01-02 - Indice Minutas Escala24x7]]
