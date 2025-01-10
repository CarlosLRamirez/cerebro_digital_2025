---
created: 2025-01-10T10:32:09
modified: '"2025-01-10 10:32", "5tc/G1T+6"'
date: 2025-01-10
type:
  - minuta
IDProyecto:
  - "11248"
---
#minuta 
#id11248

## Fecha de Reunion
2025-01-10

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Yaxer Palacios

## Agenda
* 
## Temas Discutidos
*  De momento hemos concentrado todos los esfuerzos para desplegar el ambiente DevOps
	* Se esta probando desplegar el cluster del EKS de Jenkins, aún existen inconventientes que se están tratando de resolver
* Se evidencio que el rol que tenemos tiene alguna falta de permisis
	* Estamos investigando cuales son los permisos que nos falta
	* Para poder desplegar en local, y guardar el state en el bucket S3.
* Estamos apoyando con el TS del EKS
* Pedimos del banco equiparar los roles del usuario que hace los despliegues a nivel Jenkins como el usuario que estamos utilizando para despliegue en local.
	* No conocemos el usuario (el profile dentro de Jenkins se llamaba Bancus)
	* Jonathan Cruz dice que el perfil Bancus es una configuración que se hizo a nivel local
* En el War Room vemos que no tenemos conectividad en el cluster la cuenta DevOps
	* Eso lo debemos ver con el equipo de Redes.
* En Honduras no se hizo el rol cross-account #followup #id11248
	* Se solicita que se utilice acá.
* El impedimento es que el Cluster de EKS no esta listo, el plan B es hacer los despliegues de manera local.
	* No existen los perfiles cross-account. Estamos verificando internamente quien desplegó en el Salvador.
* El plan C es utilizar el Jenkins de El Salvador para desplegar el cluster de Guatemala, pero el impedimento es que no tienen salida a Internet.
	* Podemos hacer la misma gestión para Dev.
	
## Puntos de Acción acordados
- 

## Proxima Reunión
*   

[[Minuta 2025-01-10 105623 - War Room 10 Ene]]
