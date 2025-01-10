---
created: 2024-12-31T10:04:35
modified: '"2025-01-09 15:22", "4tc/G1T+6"'
date: 2024-12-31
type:
  - minuta
aliases: 
tags:
  - Escala24x7
  - minuta
IDProyecto:
  - "11248"
---
#minuta 
#id11248

## Fecha de Reunion
2024-12-31

## Asistentes

### Cliente
* Carmen Yanes
* Mayela Campos
* Joel Erroa
### Escala24x7
- Carlos Leonel Ramírez
- Jenner Fernandez
- Yaxer Palacios

## Agenda
* 
## Temas Discutidos
*  Usuario de Cori
	* Mayela nos dice que por ser nuevo hay un proceso que se debe hacer, se va demorar quizá entre jueves 2  y viernes 3, hay se inició.
	* Necesitamos que se haga el CuscaID #followup #id11248
* Los usuarios de Jenner y Yaxer
	* Ya estaban creados
	* Se extendió el plazo, porque este vencía hoy.
* Jenner y Yaxer hacer la prueba de la VPN
	* Les pidió cambió de contraseña.
	* Yaxer ya se conectó ✅
	* Jenner necesita otra contraseña, y necesita la IP o URL de conexión 
		* se intenta con: rabct.bancocuscatlan.com.sv
	* Jenner ya se conectó ✅
	* [ ] Cori pendiente acceso de VPN #followup #id11248
* Acceso a las cuentas
	* Yaxer: comenta que tiene acceso a las cuentas, es igual solo que termina en GT  ✅
	* Jenner: estamos ok ✅
	* Cori: aún necesita su usuario de AWS 
* Repositorios (Bitbucket)
	* Repositorio para el Salvador y Honduras - no se tiene acceso, necesitamos hablar con Dennis para que nos vuelvan a dar acceso, para tener las plantilla utilizadas en previos proyectos #followup #id11248 
		* Yaxer me pasará un correo
		* Kevin Pineda indica que el puede dar el acceso pero necesita un ticket.
		* Yaxer ya pudo acceder a la pagina pero su usuario aún no tiene permisos 
	* [ ] Repositorio para Guatemala, se deben de crear. Carmen Yanes los creará y nos pasará el acceso #followup #id11248
* Bucket S3 y Roles donde se guardaran los estados de Terraform
	* [ ] Se necesita crear un bucket por cada ambiente para guardar el state de Terraform del banco - Eso lo crea el equipo de fábrica  #followup #id11248
* Pipelines y acceso al Jenkins
	* Carmen Y: De la misma forma que se hizo en Honduras
	* para HN nunca tuvimos acceso a los pipelines #followup #id11248 

---
- Abrieron un ticket por el segmento de red: ticket 29322
- Validar parámetros de instancia de Base de datos, segmentación de subredes, attachment al TGW, Internet GW en las cuentas o la salida de internet para el EKS. Necesitamos una sesión técnica para levantamiento de información.
- 


-----
CuscaID de Yaxer: yp52932


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
[[11248 - GT - Cuscatlan - Fabrica Digital GT]]
