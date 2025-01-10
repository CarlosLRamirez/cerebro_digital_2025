---
created: 2025-01-10T08:03:11
modified: '"2025-01-10 08:04", "5tc/G1T+6"'
date: 2025-01-10
type:
  - minuta
IDProyecto:
  - "11236"
---

`

#minuta 

## Fecha de Reunion
2025-01-10

## Asistentes

### Davivienda
* Darwin Arellano
* David Bohorquez
* Diego Garcia
* Nicolas Leon Perez
### Escala24x7
- Carlos Leonel Ramírez
- Jenny Rodriguez
### Mobile
- Juan Galeano
- Martin Vasconcelos
- Nahuel Moyano

## Agenda
* 
## Temas Discutidos
*  [ ] Tareas pendientes que anoto Jenny de la reunion de ayer (SPI2) #followup #id11236
	* Ajustes en el diagrama. hoy tiene una reunion con Vanne
		* Luego tener una sesión para tener el GO y dejarlo formal por correo
	* El flujo que vimos ayer fue solo para la parte pública
		* Queremos preguntar como queda amarrado el Imperva
	* Quedaron dos pendientes para usuarios internos
		* Lo mismo aplica para Camara de Compensación porque no hay usuario externo
* [ ] Otros temas pendientes de definir #followup #id11236
	* Los componentes que se deben reutilizar, que el banco tiene, como nos van a dar acceso? o están de forma transversa? o lo despliega Davivienda?
* Ayer MC envió el correo con las consultar para Technyisis relacionados al servicio de Notificaciones
* Nahuel pregunta si nos van a compartir la lista de servicios que van a intervenir para hacer la autenticación
	* Nico indica que tienen la tarea del lado de ellos, ya tiene borradores. David Santiago tiene el punto. Se espera entregar la documentación la próxima semana (WSDL). David dice que iniciaría el proximo lunes para Honduras, y a medida que avancen las demás filiales.
		* Documentación de servicios transaccionales y de consulta
	* Sería un documento por país.
	* Se llamarían distintos servicios por cada país.  Confirmado por David Santiago
	* Si hay un usuario que necesita ver tres países, deben hacer tres llamadas y consolidar la información.
* Nahuel quiere saber los proveedores de hardtoken y softoken. Así como los servicios que intervienen.
	* [ ] Nicolas espera que podamos tener una sesión con Technysis para la proxima semana para el singlesingon #followup #id11236
		* Darwin dice que con Technysis no se necesita. SSO es una cosa, y Softoken es otra. 😋
		* Se debe volver a estimar el DME 508 ❓ , porque hay un cambio
	* [ ] Nicolas espera que tambien tengamos una sesion con el proveedor para la proxima semana por el tema de hardtoken #followup #id11236 
		* Hardtoken solo para Colombia
		* Softoken para CAM
	* Nahuel dice que necesitan saber cuales son los servicios que deben utilizar para manejar hardtoken y softtoken.
* Nicolas dice todo el flujo del SSO debería ir dentro del primer entregable 🚩
	* Nahuel dice que lo están validando en estas últimas reuniones.
	* El login esta en el primer entregable
	* Nahuel dice que les falta informacion sobre cuando es el primer acceso, y los usuarios requieres activación de soft token. Esa parte del flujo es la que todavía necesitan entender como es la interacción de cada país.
	* El login esta dividido en do partes
		* El login y la transición al PER
		* La activación de soft-token (usuario nuevos)
* Nahuel comenta que han estado trabajando en el desarrollo proyecto Web, y pregunta si ya existe el repositorio para empezar a subir código
	* El repositorio ya se creó.
	* [ ] Nicolas dice que podemos darle acceso al repositorio a Iliana que ya tiene acceso al Github. #followup #id11236
	* El martes esperan tener fecha.
* Nahuel pregunta sobre la base de datos
	* Eso tiene dependencia de los CIDR
	* Nicolas dice que hasta que no cerremos el diagrama de infraestructura Cloud, no podemos tener definido el CIDR, ya que necesitamos el VoBo de Cyberseguridad.
	* [ ] Nicolas estimas que se toma 5 dias aproximadamente para la creación del CIDR. #risk #id11236 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   


## Post Reunion
- [ ] Punto Critico: no tener confirmada la arquitectura de Login, a estas altúras ya deberia estar validado, seguramente va impactar en una demora. Debe quedar registrado por escrito. #risk #id11236

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---
