---
type: Minuta
IDProyecto: "11073"
date: 2024-08-19
---



### Seguimiento temas previos

```dataviewjs
let projectID = dv.current().IDProyecto;

// Función para filtrar tareas según las condiciones comunes
function filterTasks(tasks) {
   return tasks
        .where(t => t.tags.includes("#followup"))
        .where(t => !t.tags.includes("#backlog"))
     .where(t => !t.completed)
        
}

// Obtener todas las páginas que tienen tareas relacionadas con el ID del proyecto
let tasksByProperty = filterTasks(dv.pages().where(p => p.IDProyecto === projectID).file.tasks);

// Obtener todas las tareas que tienen el tag del ID del proyecto
let tasksByTag = filterTasks(dv.pages().file.tasks.where(t => t.tags.includes("#id" + projectID)));

// Combinar ambas listas de tareas y eliminar duplicados usando un Set
let combinedTasks = [...new Set([...tasksByProperty, ...tasksByTag])];

// Mostrar la lista de tareas
dv.taskList(combinedTasks, { asOf: dv.date("today") });
 ```
## Fecha de Reunion
2024-08-19

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  Yaxer Palacios
- Franklin Garcia
- Joel Solis

## Agenda
* 
## Temas Discutidos
*  

## Puntos de Acción acordados
*  Se enviará un correo al cliente indicando los siguiente:

Hola Kimberly, Maria Jose y equipo Davivienda

De acuerdo a nuestra ultima reunión y luego de validarlo internamente con el equipo técnico de Escala24x7, esta seria nuestra respuesta oficial con respecto al tema de la integración del IDP Microsoft Entra ID para la autenticación de la aplicación de Correos Masivos:
- Nuestra primera recomendación es el setting up de un AWS Lambda Authorizer utilizando OpenID Connect (OIDC), esto es la solución mas directa y fluida
- En el caso de requerir el uso de una solución basada en SAML 2.0, se requiere la utilización de un servicio adicional que no esta contemplado llamado Amazon Cognito. Con este Servicio existe un detalle que no es centralizado y para el caso del DR, cualquier cambio que se realice en una region no se replica automaticamente en otra Region.
- Es fundamental recalcar que para cualquiera de las dos alternativas planteadas anteriormente, es necesario que Davivienda se apoye en su proveedor para realizar la configuración en Entra ID y provea los parametros necesarios para poder incluirlos del lado de la aplicación
	- Escala24x7 no se responsabilizará de la configuración paso a paso (click by click) de la plataforma Entra ID ya que no es su especialidad.

Cualquier consulta adicional quedamos a la orden.


**Asunto: Integración de IDP Microsoft Entra ID - Aplicación de Correos Masivos**

Estimadas Kimberly, María José y equipo Davivienda,

Siguiendo nuestra última reunión y tras una validación interna con el equipo técnico de Escala24x7, les compartimos nuestra respuesta oficial respecto a la integración del IDP Microsoft Entra ID para la autenticación de la aplicación de Correos Masivos:

**Recomendaciones:**

1. **Solución recomendada: AWS Lambda Authorizer con OpenID Connect (OIDC)**
    - Consideramos que esta es la solución más directa y eficiente para la integración.
2. **Solución alternativa: SAML 2.0 con Amazon Cognito**
    - En caso de requerir estrictamente el uso de SAML 2.0, es necesario implementar Amazon Cognito.
    - Es importante tener en cuenta que esta solución implica una configuración descentralizada. Cualquier cambio realizado en una región de AWS no se replicará automáticamente en otras regiones, lo que podría requerir una gestión adicional en caso de recuperación ante desastres (DR).

**Consideraciones generales:**
- **Configuración en Entra ID:** Para cualquiera de las dos alternativas, es indispensable que Davivienda, con el apoyo de su proveedor, realice la configuración necesaria en Microsoft Entra ID y nos proporcione los parámetros requeridos para integrarlos en la aplicación.
- **Soporte de Escala24x7:** Escala24x7 brindará apoyo en la integración de los parámetros proporcionados por Davivienda en la aplicación. Sin embargo, no podemos responsabilizarnos de la configuración detallada (paso a paso) dentro de la plataforma Microsoft Entra ID, ya que esto escapa a nuestra área de especialización.

**Comentarios adicionales:**
- **AWS Lambda Authorizer:** Esta solución ofrece una integración nativa y simplificada con servicios de AWS, lo que facilita la gestión y escalabilidad de la autenticación.
- **Amazon Cognito:** Si bien es una opción viable para SAML 2.0, es importante considerar la complejidad adicional de la gestión descentralizada en escenarios de múltiples regiones.

Quedamos a su disposición para cualquier consulta o aclaración adicional que puedan tener.

Saludos cordiales,

Carlos Ramírez Project Manager Escala24x7

**Revisiones y precisiones técnicas:**

- El correo es claro y conciso, presentando las opciones de manera directa.
- La información técnica es precisa y resalta los puntos clave de cada solución.
- Se establece claramente el alcance del soporte de Escala24x7.
- Se incluyen comentarios adicionales para ayudar en la toma de decisiones.

**En resumen, el correo está bien redactado y técnicamente sólido.**

Si tienes alguna otra duda o necesitas más información, no dudes en preguntar.





## Proxima Reunión
*   

---
Template: [[Minuta de Reunion Proyecto]]
Author: Carlos Ramírez - 2024
