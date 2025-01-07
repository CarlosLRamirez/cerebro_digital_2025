---
created: 2024-12-27T10:27:39
modified: '"2024-12-31 10:35", "2tc/G12T+6"'
date: 2024-12-27
type:
  - minuta
aliases: 
tags:
  - Escala24x7
  - minuta
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

- [ ] Importante tener visibilidad de los pipelines en Jenkins #followup #id11248 
- [ ] No tenemos acceso a un Transit Gateway  #followup #id11248

## Temas Discutidos
*  

## Puntos de Acción acordados
- [x] Enviar correo pidiendo los accesos #id11248 📅 2024-12-27 ✅ 2024-12-27
	- Despues que me des todos los prerequisitos, el proyecto inicia
	- Hay que ser bien rigidios y duros
- [x] Compartir editable del diagrama de arquitectura #followup #id11248 ✅ 2024-12-27

Que hacemos nosotros
- Pedir CIDRs
- Configurar la parte de networking (con sus modulos)
- Mejorar los modulos siguientes a networking (de que hay que hechar código hay que hechar)

Que hacen ellos
- Crear cuentas

## Feedback Pablo
- Denis es quien el más difícil de tratar, el es quien involucra al equipo de Guatemala
- Denis dice que no le gustan los sprints
	- El va preguntar cuando nos van a entregar desarrollo
	- Se quejó de la metodologia
	- 1 semana para desplegar desarrollo (Networking, Seguridad y Monitoreo)
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
[[20241231T1023 11248-GT-Banco Cuscatlan - Fabrica Digital GT]]
