---
created: 2024-12-12T08:05:07
modified: '"2024-12-13 12:17", "5tc/G12T+6"'
date: 2024-12-12
type:
  - Minuta
aliases: 
tags:
  - Escala24x7
---
**Entrada de diario:** 
Hoy es jueves 12 de diciembre, estamos en la semana 50 del año 2024

> Aquí escribe todo lo que necesites relacionado a Escala24x7


## Tareas para hoy
- [x] Ponerme al dia de los proyectos ✅ 2024-12-12
- [x] Hablar con Rafa al final del dia ✅ 2024-12-12
- [x] Configurar la plantillas para minutas Escala ✅ 2024-12-12
- [x] Crear Slack con MC #id11236 

## Registro de tiempo
8:00 inicie con revision de los chats de proyectos, principalmente PER y Cempro, ah y ver un poco Bancolombia
9:00 reunion con Frank para revisar PER
9:30 termine con Frank, me puse a ver lo de la gestion de minutas
10:00 hay una reunion de PER, me puse a ver vainas
11:10  entre a una reunion interna con CPSM
12:20 termine con Novys y entre a sync on Raul
12:39 termine sync on Raul
1:00 intenté almorzar, y me meti a la sync con Novys, aùn no llega, mientras me pongo al dia con Slack de Whitelist y NetRetail.. nunca apareció Novys
1:30 Entro a sync de Davivienda Whitelist
2:30 Sesion con Davivienda (David Chaparro)
entre 3 y 4 estuve revisando correos

## Apuntes Proyectos

### 11236-Davivienda-PER #id11236

- Hoy es la primera sesión técnica entre Dav, MC y Escala24x7 a mis 10am
- A las 9 programé una sync previa con Frank
- Cuadro Resumen al dia de hoy: https://docs.google.com/spreadsheets/d/1d_elL-W5sRhfpDWoLm_8fQopYCPJsZcJYY1ySIFu_Kg/edit?gid=0#gid=0
- El Kickoff con el cliente fue el martes 10/Dic - Buscar la grabacion
- [ ] Buscar grabaciones de Kickoff y Prekickoff #id11236
- Matriz Raci. https://docs.google.com/spreadsheets/d/1O1jAzv0Ce6NdZIB3_utt-5omStVyI5EjQIc8057rC4I/edit?gid=0#gid=0 -- Esta vacia 😀
	- hay que marcar bien quienes son los responsables, por ejemplo, de seguridad perimetra (Davi CO), publicacion de las apps (Davi CO), devops (Davi CO), etc
- [ ] Completar la Matriz RACI - Gestionar #id11236
- Presentacion de Kickoff: https://docs.google.com/presentation/d/1ijw8Jg_yd7rZFv_BgKHDpiiHjZ4jCnFENQIkNs4WXT0/edit#slide=id.p1
- Plantilla Backlog:  https://docs.google.com/spreadsheets/d/1xAVlg8fVIGKjSWj7J1id53kNlgxX7QrULvLEpqYaRQ4/edit?gid=1120027636#gid=1120027636 -- Esta vacia 😀


### 10854 - Cempro #id10854
- Según el ultimo informe ya se terminaron las migracions Lift & Shift
- Solo queda pendiente la ventana para la salida a producción de APP Ruteo
- [ ] Confirmar con Jhonatan y resto del equipo #id10854
- [ ] Como quedaron los PaO? #id10854
- [ ] Hubo un issue con la aplicacion de marcajes? #id10854


### 11065 - Whitelist - Davivienda #id11065
- Vamos por el pase a Laboratorio (QA), ya casí estamos listos para desplegar
- Davivienda tenia pendiente la corrección de unos módulos
	- CloudWatch y ALB: dicen que ya lo liberamos
	- Aún nos esta dando un error con el ALB
	- El MBaSS no resuelve por DNS, en conclusión ya no va ir por ALB
		- El cliente esta de acuerdo, que no va resolver por nombre, solo por IP
		- Los vamos a comentar nuevamente - Cori

**Siguientes Pasos**
- Estamos esperando el GO del cliente para pasar a la Laboratorio
- Hacer el branch (Laboratorio) ✅ 
- Configuración del Pipeline para que tome el ambiente Laboratorio ✅ 
- DAV debería tener configurados los secrets - Iliana va confirmar ✅ 
- Solo hay que hacer el Pull Request ✅ 
- Alberto Madrir debe crear unos usuarios #followup
- Nelson esta resoliviendo unos temas de la redacción de los correos

### 11206 - Ambientes Bajos #id11206
- Ya se desplegó CR con el ambiente, ya esta clonado el RDS. Solo falta que nos digan como serían las pruebas.
	- Están pendientes una rutas en el TGW.
- Necesitamos coordinar una reunión para coordinar las pruebas de ambientes bajos con la seguridad perimetral.
- Los otros países aún no están desplegados, primero queremos hacer las pruebas Integrales.

**Punto de Accion**
- Buscar una reunión para ver el tema de la conexión contra ciberseguridad

### 11221 - DR #id11221
- David Chaparro: avances sobre la cuenta Shared-Services
	- Ya se desplegó la primer máquina Palo Alto
	- Desplegaron una maquina tipo Bastión
	- Esta semana continuan con la implementación de los otros dos dispotivios tipo FW
	- Ya tienen la base de Networking ya desplegada
	- Al momento no se tiene ningún inconveniente.
- Axity dicen que no recibieron el acta de la ultima sesión: Daniel Bernal daberyha@proveedores.davivienda.com
	- Si estaba Daniel Bernal en el correo

**Punto de accion**
- enviar un correo preguntando por la nueva imagen con RedHat

## Otros temas
- Performance Review 2024 https://drive.google.com/file/d/1kNEYfFGPQoYBtp02nbMy-JB9xZVnpV_R/view?usp=sharing
- Convivio Escala24x7 el jueves 19 de Diciembre
- [ ] Enviar consumo de horas a Sandra Lucas #PMO 
	- Ejemplo: ![[Pasted image 20241212115900.png]]
	- Enviarlo mensualmente a partir del 2025


## Minutas del dia

 ```dataview
table date as "Fecha de Reunión", IDProyecto as "ID del Proyecto"
from "04-Work@Escala24x7/Minutas"
where contains(type, "minuta")
where date = date(this.file.frontmatter.date)
sort date asc
```
----
**Notas relacionadas:**
[[TOC-Agenda Escala24x7]]


