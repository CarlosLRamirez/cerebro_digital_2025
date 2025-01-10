---
created: 2025-01-03T10:02:40
modified: '"2025-01-03 10:05", "5tc/G1T+6"'
date: 2025-01-03
type:
  - minuta
aliases: 
tags:
  - Escala24x7
IDProyecto:
  - "11248"
---

https://app.read.ai/analytics/meetings/01JGPE9513JM498GCS0FEZA1DM?utm_source=slack



**  
Fecha de Reunión  
**2025-01-03  
  
**Asistentes  
**  
**Banco Cuscatlan  
**

- Carmen Yanes
- Mayela Campos
- Isaias Palacios
- Kevin Pineda
- Roberto Rubio

**Escala24x7**  

- Carlos Leonel Ramírez
- Yaxer Palacios
- Jenner Fernandez
- Cori Arenas

**Agenda:**

Definir aspectos pendientes para el despliegue

  

**Temas Discutidos:**

**1. Validación de la segmentación de red:**  

- Se revisó la segmentación de red propuesta por Banco Cuscatlán para el proyecto Fábrica Digital GT.
- Se confirmó que la segmentación es correcta y se puede proceder con ella, ya que fue validada previamente por Cuscatlán con el equipo de Fábrica Digital

**2. Definición del orden de despliegue de ambientes:**  

- Se acordó que el despliegue se realizará en el siguiente orden: Desarrollo, UAT y Producción.

**3. Conexión con Transit Gateway:**

- Se confirmó que Banco Cuscatlán se encargará de:

- Crear el attachment de cada VPC al Transit Gateway.
- Crear las nuevas tablas de ruta en los ambientes.

**4. Configuración de la RDS:**  

- Se definió que se utilizará una RDS Aurora Postgres basada en instancias, no serverless
- Quedó pendiente por parte de Cuscatlán confirmar si la RDS será global, considerando el impacto en costos y la estrategia de disaster recovery.

**5. Proceso de despliegue con Jenkins:**  

- Se acordó utilizar Jenkins para el despliegue, como en el proyecto de Honduras.
- Escala24x7 no tendrá acceso al usuario, sino que asumirá un rol dentro de la cuenta de DevOps para realizar el despliegue.

**6. Reuniones de seguimiento:**

- Se acordó realizar reuniones de seguimiento los martes y jueves a las 10:30 AM (hora de Guatemala).
- Carlos Ramírez se encargará de enviar las invitaciones a las reuniones.

**Puntos de Acción/Pendientes**

1. **Fecha de entrega del clúster de DevOps:** Cuscatlán debe proporcionar una fecha estimada para la entrega del clúster de DevOps.
2. **Proporcionar accesos:** Cuscatlán debe finalizar la gestión de accesos para Cori (Mayela Campos) y el equipo de Escala24x7, incluyendo la generación del CuscaID.
3. **Compartir información sobre pipelines y Jenkins:** Cuscatlán debe informar cuándo estarán listos los pipelines y Jenkins para que Escala24x7 pueda realizar pruebas.

**Proxima Reunion**

Martes 7/Ene

  

Quedo atento a cualquier consulta o comentario.



--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---

