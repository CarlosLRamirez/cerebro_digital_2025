---
created: 2025-01-07T14:17:34
modified: '"2025-01-07 14:19", "2tc/G1T+6"'
date: 2025-01-07
type:
  - minuta
IDProyecto:
  - "11248"
---
[Fábrica Digital IaC GT project overview - Bitbucket (banco.latam)](http://bitbucket.agile.banco.latam:7990/projects/FDIG "http://bitbucket.agile.banco.latam:7990/projects/fdig")

#minuta 
#id11248
## Fecha de Reunion
2025-01-07

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Problema con VPN de Yaxer - Resuelto
* Acceso a Repositorios
	* HN ✅
	* GT: [Fábrica Digital IaC GT project overview - Bitbucket (banco.latam)](http://bitbucket.agile.banco.latam:7990/projects/FDIG "http://bitbucket.agile.banco.latam:7990/projects/fdig")
- Yaxer va dedicar la plantilla para hacer las pruebas de lanzamiento.
	- VPC
	- Subredes
	- RDS
	- SNS
	- MSK
	- Llaves KMS (IaC) con CloudFormation
- Prueba Manual de Lanzamiento
	- En teoría si se puede lanzar infra con el usuario de Yaxer.
	- ![[Pasted image 20250107142150.png]]
- Jonathan Cruz comenta sobre los usuarios de para Jenkins  (Cross Platform permission )
	- Dice que ya existe un stack en CloudFormation para hacerlo automatizadamente #followup 
		-  Se podrá gestionar el permiso para los usuarios DevOps y DevOps IAC para extender los roles entre las diferentes cuentas DevOps GT, DevOps Dev GT, DevOps QA GT, DevOps PROD GT
- Mañana hacemos la prueba con los accesos de Cori
- Fecha de deadline para los otros ambientes:
	- Mayela lo tienen que confirmar las fechas.
- 




## Puntos de Acción acordados
- 

## Proxima Reunión
*   

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---

# War Room - Fabrica GT

Se

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---
