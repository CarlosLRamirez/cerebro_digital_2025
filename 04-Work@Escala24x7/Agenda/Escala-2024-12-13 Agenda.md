---
created: 2024-12-13T08:27:32
modified: '"2024-12-20 08:10", "5tc/G12T+6"'
date: 2024-12-13
type:
  - daily-note-escala
aliases: 
tags:
  - Escala24x7
---
`


**Entrada de diario:** 
Hoy es viernes 13 de diciembre, estamos en la semana 50 del año 2024

> Aquí escribe todo lo que necesites relacionado a Escala24x7


# Tengo que hacer

```dataview
TASK 
FROM "04-Work@Escala24x7"
WHERE due <= date(today) 
WHERE !completed 
WHERE !contains(tags, "#followup")  
```


## Tareas para hoy
- [x] Crear Space con Dav #id11236
- [x] Hablar con Jenny por PER #id11236 ✅ 2024-12-13
- [x] Hago Minuta de la ultima sesion de PER #id11236 ??? 📅 2024-12-13 ✅ 2024-12-18
- [x] Completar - Performance Review #Escala24x7 📅 2024-12-13 ✅ 2024-12-13
- [x] Organizar grabaciones del proyecto PER #id11236 📅 2024-12-20
- [x] Ver tema de Inicio de Relacion del proyecto PER #id11236 📅 2024-12-20
	
- [x] El lunes ver lo del proyecto nuevo de Switft 📅 2024-12-14  #pmo
- [x] Cargar mis horas el lunes!!! a primera hora #PMO 📅 2024-12-20 ✅ 2024-12-23
## Registro de tiempo
8:00 Organizacion
8:30 Buscar documentos PER - Organizar carpeta Proyecto
9:00 entro a sync de CPSMs




## Apuntes Proyectos

### 11236 - Proyecto PER

Cosas que tengo que platicar con Jenny sobre PER:
- Documento tecnico
	- Cual es el definitivo? - los que dicen FINAl, hay uno para PER y otro para Camara
	- Hay otro documento a tener en cuenta?
		- [x] Jenny me paso un slide con las funcionaldades, moverla y pasarlo a la carpeta de Jenny #id11236 📅 2024-12-20
	- [x] Buscar enlaces enlace a la Arquitectura en LucidChart, estan en el documento #id11236 📅 2024-12-20
- Tema de mapa de dependencias y conexiones
	- Cual era el documento que estabas viendo ayer
	- que necesita? 
		- Necesitamos sentarnos con el banco para estas sesiones:
			- [x] Sesion de depenencias de PER: Esquemas de conectividad de red (comunicacion) #followup #id11236
			- Jenny, Frankling, equipo Escala, Daivienda (Lideres de pais), arquitecto MC
					- Objetivo: Diagrama de dependencia sde networking (conectividad)
					- Levantar diagraa de conectividad con paises y platafrormas que rquieresn interactuar con plataforma d ePER y Camara de Comperancion
					- Recomendacion: adicionar responables de cada paises para revisar estas dependencias en detalle.
			- [x] Sesion para dependencias/esquema de SSO #followup #id11236
			- [x] Sesion para Despendencia de PER Seguridad - Conectividad a capacidades de negocio #followup #id11236 ✅ 2024-12-23
	- [x] Acceso de DevOps para equipo Escala y Mobile #followup #id11236
		- Lo mas fácil es que lo administremos nosotros y le demos acceso a MC
	- [x] Diagrama de dependencias deben estar bajo nuestra administración #followup  #id11236
- Historias de Usuario
	- Donde las encuentro? en la carpeta
	- Ya las tiene MC? si
- [x] Acceso a Jira por MC #followup #id11236
- [x] Inicio de relacion con MC #followup #id11236
	- Firma de SoW
	- Contrato?

- [x] Ver con MAFE el tema de horas, para ver como lo dejo Maria Fernanda #followup #id11236 ✅ 2024-12-23
	- hay 1040 horas gestion y apoyo a MC
	- Toca validarlo con MAFE
- [x] Tenemos que construir una RACI #followup #id11236
	- hacer una sesion

**Open Items**
- [x] Firma de documentos (a). MSA (Master Services Agreement)  , (b). NDA (Non-Disclosure Agreement) #followup #id11236
- [x] Crear artefacto de open items para seguimiento, o utilizar el que hizo Frank #id11236 📅 2024-12-20
- [x] El lunes hacer un listado de cosas que tengo que hablar con el PM de mobiles y el PM de DAV #id11236 📅 2024-12-14


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


**Enlaces**
[[👷 Work@Escala24x7]]

