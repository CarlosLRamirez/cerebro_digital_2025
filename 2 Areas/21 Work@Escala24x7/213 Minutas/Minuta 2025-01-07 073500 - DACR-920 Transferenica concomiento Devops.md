---
created: 2025-01-07T07:35:00
modified: '"2025-01-07 07:38", "2tc/G1T+6"'
date: 2025-01-07
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - cmm-directores
---
#minuta 
#id-cmm-directores

## Fecha de Reunion
2025-01-07
## Asistentes

### Escala24x7
- Carlos Leonel Ramírez
- Julio Pestana
- Nelson Mora
- Johan Blanco
- Iliana Estupinian

## Agenda
* Volver a revisar con Nelson e Iliana para entender sobre el proyecto de Whitelist
## Temas Discutidos
* El proyecto de Whitelist fue bastante atropellado.
* Este proyecto y todo lo que está adelante.
* En Whitelist 
	* Al pasar a laboratorio, ellos dijeron que habían modificado los pipelines y ya no pasaron porque forzaban a utilizar sus módulos.
	* Se tuvo que hacer su re-trabajo para eliminar los módulos locales y empezar a  utilizar los módulos de ellos. Fue un re-trabajo de 2 a 3 meses.
	* Ellos son los que hacen las modificación y tienen la última actualización, entonces el lineamiento tiene que venir de ellos
	* Ellos tienen una validación en cada pipeline
		* Cuando ellos actualizar el repositorio central del pipeline, de rompen todos los pipelines
		* Si ellos una actualización, los módulos y o pipelines deben tener la última versión.
	* Nosotros requerimos tener a una persona de DevOps asignada para que pueda atender estos problemas. 
	* Es importante que tengamos el listado de todos los módulos y acceso a ellos.
	* Lo ideal es que el equipo tenga acceso antes de la sesion
* Esta version del pipeline, esta version del modulo -- que estas definiciones vengan de ellos, por escrito.

## Puntos de Acción acordados
- Se abrió [SOI-2740](https://escala24x7.atlassian.net/browse/SOI-2740)


## Proxima Reunión
*   

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---

