---
created: 2024-12-27T10:27:39
modified: '"2024-12-27 11:28", "5tc/G12T+6"'
date: 2024-12-27
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "11248"
---
## Fecha de Reunion
2024-12-27
## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* Confirmación del equipo
* Retos encontrados
	* El mayor reto fue que todo lo querían rápido
	* Los accesos tomaron como 3 semanas
	* 
* Accesos
	* A los repositorios en bitbucket, eso lo tienen que escalar a su equipo de seguridad
	* y acceso a la VPN
	* Enviarlo antes de iniciar, hay un documento de Honduras, pedirlo para todos 
* Actividades
	* Creación de cuentas (las crean ellos), cuentas independientes, se va facturar aparte
	* La infra la despliegan ellos, antes que desplieguen debemos revisar los módulos de TF (EKC con nodos administrados, MSK, RDS, API Gateway, Cognito, SES, OpenSerch, CFN, S3, CoudWatch, *NewRelic (obervabilidad)* )
	* Las 4 cuentas (DEV,QA,UAT,PROD)
	* Nosotros responsables de networking, seguridad, monitoreo, y config alertas.
	* brindar el apoyo de revisar los módulos
	* trabajemos el rubro de dejar documentación de lo que se haga
* Creditos AWS
	* Eso va con créditos, dice Mafer que dice si y no
	* Los créditos van de último
	* Podríamos iniciar con lo que tenemos.. 
	* Vamos a esperar el correo se Jose
	* Vamos a tener que tagear el MAP después.
* Numero de Horas
	* 900 horas
	* Pablo lo ve positivo
* Confirmación de Alcance
	* Hay unos cambios en el alcance
	* apoyo con revision y mejoras a módulos de IaC
	* apoyo mejores practicas
	* diagramas y proyecto (conectividad, cargas por ambiente, seguridad)
	* Kubernetes (no es por Fargate, nos vamos por nodos)

## Temas Discutidos
*  

## Puntos de Acción acordados
- [ ] Enviar correo pidiendo los accesos 📅 2024-12-27  #id11248

## Proxima Reunión
*   

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---
Template: [[06 Minuta de Reunion Template]]
Author: Carlos Ramírez - 2024
