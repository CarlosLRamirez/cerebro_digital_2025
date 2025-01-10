---
type:
  - minuta
IDProyecto: "11152"
date: 2024-07-19
modified: '"2025-01-07 12:42", "2tc/G1T+6"'
---

``

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
2024-07-19

## Asistentes

### Cliente
* Jeferson - Cisco
* Pedro  - Cisco
* Oscar Mauricio Morales
### Escala24x7
- Carlos Leonel Ramírez
- Antonio Lopez
- Roy Flores - Connectria
- Fred Lubber - Connectria
- Jason Weller - Connectria
-  

## Agenda
* 
## Temas Discutidos

- **Conectividad:**
    - Habrá dos proveedores MPLS independientes que llegarán al centro de datos de Connectria.
    - Las instancias de Connectria deben tener conexión tanto por MPLS como por Internet.
    - Connectria proveerá EdgeConnect, un servicio de capa 3 para SD-WAN, ya sea físico o virtual.
- **Detalles Técnicos:**
    - Se aclaró que Connectria ofrece una frontera en capa 3 para permitir la implementación de SD-WAN.
    - Se discutió la importancia de definir detalles de enrutamiento, protocolos y número de puertos.
    - Se confirmó la alta disponibilidad y capacidad de ancho de banda en el hipervisor de Connectria.
    - Bancolombia tendrá dos circuitos independientes con proveedores diferentes.
- **Configuración SD-WAN:**
    - Se acordó tener dos routers SD-WAN por centro de datos, virtualizados en Connectria (no incluido en el alcance actual).
    - Se utilizará VRF para separar lógicamente los entornos.
    - La replicación de Mimix se hará por Internet vía túnel IPsec mientras se activan los circuitos MPLS.
    - Los routers SD-WAN deben alcanzar las controladoras por MPLS e Internet.
- **Firewall y Conectividad a AWS:**
    - Se confirmó que la conexión Direct Connect a AWS está incluida en el diseño.
    - Se discutió la gestión del firewall de salida a Internet (Bancolombia o Connectria). Connectria aclaró que solo habrá dos firewalls de alta disponibilidad y que la gestión debe definirse.
    - Se propuso la co-gestión como opción.

**Puntos de Accion:**

- Definir la responsabilidad de gestión y el modelo operativo de los firewalls de alta disponibilidad. Cyberseguridad Bancolombia
- Definir la gestión de los permisos de Internet. - Cyberseguridad Bancolombia
- Definir los bloques de direcciones para SD-WAN (Oscar/Jefferson).
- Definir los bloques de direcciones para las LAN internas de IBMi (equipo de Pastor).

**Proxima Reunión**
- Miercoles 24 a las 11am



**Revised Summary in English:**

The following key points were discussed in the meeting:

- **Connectivity:**
    - There will be two independent MPLS providers connecting to Connectria's data center.
    - Connectria instances should have connectivity through both MPLS and the Internet.
    - Connectria will provide EdgeConnect, a layer 3 service for SD-WAN, either physical or virtual.
- **Technical Details:**
    - It was clarified that Connectria offers a layer 3 boundary to enable SD-WAN implementation.
    - The importance of defining routing details, protocols, and the number of ports was discussed.
    - High availability and bandwidth capacity in Connectria's hypervisor were confirmed.
    - Bancolombia will have two independent circuits with different providers.
- **SD-WAN Configuration:**
    - It was agreed to have two SD-WAN routers per data center, virtualized in Connectria (not included in the current scope).
    - VRF will be used to logically separate environments.
    - Mimix replication will be done over the Internet via an IPsec tunnel while the MPLS circuits are activated.
    - SD-WAN routers must reach the controllers via both MPLS and the Internet.
- **Firewall and AWS Connectivity:**
    - It was confirmed that the Direct Connect connection to AWS is included in the design.
    - The management of the outbound Internet firewall (Bancolombia or Connectria) was discussed. Connectria clarified that there will only be two high availability firewalls and that the management needs to be defined.
    - Co-management was proposed as an option.

**Next Steps:**

- Define the management responsibility and operating model for the high availability firewalls. - Cybersecurity Bancolombia
- Define the management of Internet permissions. - Cybersecurity Bancolombia
- Define address blocks for SD-WAN (Oscar/Jefferson).
- Define address blocks for internal IBMi LANs (Pastor's team).

**Next Meeting**
- Miercoles 24 a las 11am




---
