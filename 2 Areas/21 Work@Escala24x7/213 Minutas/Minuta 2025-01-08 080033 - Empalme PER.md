---
created: 2025-01-08T08:00:33
modified: '"2025-01-08 08:01", "3tc/G1T+6"'
date: 2025-01-08
type:
  - minuta
IDProyecto:
  - "11236"
---
`
#minuta 
#id11236

https://app.read.ai/analytics/meetings/01JH33913DPQVS30G5F381Z9PS


## Fecha de Reunion
2025-01-08

## Asistentes

### Cliente
* David Bohorquez
* Nicolas Leon
* Wendy Manrique
* Diego Felipe Garcia
* Darwin Gabriel Arellano
### Escala24x7
- Carlos Leonel Ramírez
- Juan Galeano
- Nahuel Moyano
- Johan Blanco
## Agenda
* 
## Temas Discutidos
* Pregunta de MC: Nomenclatura de los Microfront
	* En ingles
* Consulta sobre el InsertAlert
	* Endpoint?
* 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---

### Reunión de Empalme - 8 de enero de 2025

**Asistentes:** Nicolás, David Santiago, Diego, Nahuel, Juan, Carlos y Jenny

**Temas principales:**

- **Accesos a GitHub:** Se confirmó que Iliana ya tiene acceso. Se está verificando si el resto del equipo de Mobile Computing necesita nuevas licencias o solo acceso a los repositorios.
- **Nomenclatura:** Se utilizará nomenclatura en inglés para el desarrollo, incluyendo la base de datos.
- **Servicio InsertAlert:** Mobile Computing necesita más información sobre el input de este servicio. David Santiago se comprometió a compartir la documentación (incluyendo ejemplos de requests y responses) a partir del viernes.
- **Base de datos (RDS en AWS):** Jenny informó que ya tienen acceso a la cuenta de AWS, pero aún necesitan los CIDR y los módulos de DevOps para desplegar la red y la base de datos. Esperan tenerla lista para el viernes.
- **Documentación:** Mobile Computing está trabajando en la documentación del Home y la autenticación con SSO. Se espera que esté lista para el lunes.
- **Pendientes:**
    - Visto bueno de ciberseguridad para el diagrama de arquitectura.
    - Definición de los CIDR para las cuentas.
    - Documentación completa de los servicios.

**Puntos de atención:**

- **Gestión de accesos a GitHub:** Es crucial que se otorguen los accesos lo antes posible.
- **Entrega de la documentación de los servicios:** Davivienda debe cumplir con la fecha de entrega.
- **Definición de los CIDR:** Es necesario para completar la configuración de la infraestructura.

**Próximos pasos:**

- Nicolás gestionará las licencias de GitHub.
- David Santiago entregará la documentación de los servicios a partir del viernes.
- Jenny continuará trabajando en la creación de la base de datos.
- Mobile Computing finalizará la documentación para el lunes.

En general, la reunión sirvió para hacer seguimiento a los pendientes. Se espera avanzar en la entrega de información y la configuración de la infraestructura la próxima semana.

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---
