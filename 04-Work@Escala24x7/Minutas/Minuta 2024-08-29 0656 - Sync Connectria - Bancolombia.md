---
type: Minuta
IDProyecto: "11152"
date: 2024-08-29
---
`

### Seguimiento

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
2024-08-29

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* [x] Transmitir mensaje a Escala/Connectria de JDV #followup
* [x] Tema Outage FW anoche #followup
* [x] Alinear fechas para SUFIPRP #followup
* [x] Correo de Pastor pidiendo mas detalle para la actividad de Mimix #followup
	
* SLA comprometidos por los 3rd Party - Necesita ser documentado y revisado.
	* 
## Temas Discutidos
*  Tatiana: El FW que se va utilizar es el productivo
	* Tiene un PortChannel 2 x 10GB
	* Se va dejar de hacer inspección de ese trafico
	* Mañana en la noche, se iniciaría la transmisión
	* Tener posible a alguien monitoreando desde las primeras horas
	* Si se llega a percibir algún impacto se pararia el trafico de replicación
* Las configuraciones hoy
* Ariosto
	* Validar las IPs en el leaf
* Connectria
	* Estan preparando todo para tenerlo listo
* Plan
	* Mañana en la mañana la sesión de configuración
	* Relación de confianza
	* Poner a sincronizar el pool vacío (la sesión administrativa de la sincronización la hacemos en otra sesión)
	* 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
Template: [[2024-12-15T112346 - Nota Rápida]]
Author: Carlos Ramírez - 2024


Estimada María Elsy,

Esperamos que este correo te encuentre bien.

Queremos compartir algunas preocupaciones y riesgos que hemos identificado en relación con la gestión de los firewalls en el proyecto de migración iSeries.

Habitualmente Connectria despliega, configura y administra un par de firewalls en modo HA que actúan como frontera de seguridad para las máquinas (LPAR) del cliente en cada AZ. Estos firewalls manejan tanto el tráfico productivo como el no productivo, ya que dicho tráfico se separa a nivel de zonas dentro del clúster de FW.

El alcance original del proyecto incluía este par de firewalls (recursos de cómputo, licencias de Palo Alto y servicios de despliegue). Sin embargo, al iniciar el proyecto, recibimos el requerimiento de que Bancolombia debía configurar los firewalls, proveer las licencias y administrarlos exclusivamente en producción a través de un proveedor externo, Axity. Además, la visión de la arquitectura de red de Bancolombia consideraba 2 clústeres en HA, es decir, 4 firewalls.

A lo largo del proyecto, hemos tenido varias reuniones para alinear la forma en que Connectria tiene la configuración con la visión de Bancolombia sobre el diseño de red, que a menudo se contrapone a las buenas prácticas y la configuración estándar.

Consideramos un riesgo el que los firewalls sean administrados por un tercero, en este caso Axity. Si Bancolombia no tiene problema en que su infraestructura de seguridad sea administrada externamente, no entendemos por qué no se permitió que Connectria administrara dichos firewalls.

Estos firewalls son la "puerta de entrada" a toda la infraestructura (LPARs) en Connectria. Cualquier inconveniente con ellos implicaría depender de un tercero para acceder a los LPARs, impactando los SLAs que podemos garantizar como Escala24x7/Connectria.

Las definiciones realizadas durante el proyecto por los equipos de Cyber y Telco han llevado a reprocesos y retrabajos en Connectria. Esto se habría evitado si Bancolombia hubiera seguido la recomendación original de mantener el diseño estándar de Connectria y considerar una gestión compartida de los firewalls.

Además, observamos que Bancolombia aún está adquiriendo licencias de firewall, a pesar de que Connectria las incluyó en el alcance original y ya las tenía disponibles.

Estamos seguros de que, si se hubiera seguido el plan original con Connectria configurando los firewalls, probablemente ya estaríamos realizando pruebas en los LPARs desplegados. De hecho, ayer Axity perdió la gestión de los firewalls debido a una maniobra en la configuración de HA, lo que refuerza nuestras preocupaciones.

Agradecemos su atención a estas preocupaciones y esperamos poder colaborar para encontrar la mejor solución que garantice el éxito del proyecto y la seguridad de la infraestructura de Bancolombia.

Cordialmente,


![[../attachments/Pasted image 20240829105224.png]]



 ![[../attachments/Pasted image 20240829110032.png]]



- Se requiere el FW entre el SD-WAN y el Internet
- Compartir el diagrama 


Entre Lumen y Connectria:

![[../attachments/Pasted image 20240829110212.png]]

Entre Connectria y el Versa:
![[../attachments/Pasted image 20240829110944.png]]

![[../attachments/Pasted image 20240829111105.png]]



