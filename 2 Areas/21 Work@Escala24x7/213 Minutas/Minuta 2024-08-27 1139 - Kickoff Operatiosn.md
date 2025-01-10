---
type:
  - minuta
IDProyecto: "11152"
date: 2024-08-27
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
2024-08-27

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  

## Puntos de Acción acordados


Hello Jason Waller Josh Patterson Roy Flowers  and team,

  
As discussed in our previous meetings, Bancolombia is eager to start aligning on several operational topics and involve their team responsible for the post-migration operations.  
  

We believe it's crucial to start defining a plan and timeline for working sessions, both internally between Escala24x7 and Connectria, as well as with the client, to address these concerns. We feel that involving the relevant teams from Bancolombia will help alleviate their anxiety and mitigate any internal resistance to the project.  
  

Here are the main topics they've expressed concern about:  


**1. Privileged Access Management for Connectria**  
Bancolombia has a dedicated "Control de Accesos" (Access Control) area responsible for managing privileged access to their LPARs. They use Cyberark and require requests for special authorities like QSOCFR or *ALLOBJ to be approved by this team. Kindryl currently follows this process. Bancolombia is inquiring whether Connectria can adhere to this same access control procedure.  

- Siempre que se tenga documentado, lo podemos hacer, ellos ya lo hacen con otros clientes.
- Necesitamos tener el proceso del cliente, hay un plugin para ACS
- *CONSRV account for the monitoring tools ?? (service account). 


**2. Monitoring of Machines in Connectria**  
Bancolombia currently has a 24/7 monitoring center called CoES, with dedicated staff for each vendor. This model won't be feasible when the machines are migrated to Connectria. The bank needs to understand what type of monitoring platform they will have access to and how it can be integrated into their CoES. They are interested in options like accessing a dashboard or integrating Connectria's monitoring data into their own dashboard via an API.  


- We need to fill the Escalation Notification Runbooks
	- Jose Raborg y/o Cesar nos ayudaran con el llenado de la primera iteración del documento
- Standard view on Tria (Dashboard)
	- Another views? Ryan mention another view that integrates Grafana but only for Escala24x7
	- Josh and Ryan will come back 
  
**3. Third-Party Monitoring Tools and iDoctor Replacement**  
Bancolombia currently uses a third-party monitoring tool called Nimbus on their machines, which will need to be disabled after migration. Additionally, they utilize IBM iDoctor for specific monitoring tasks like Full Open Close, Activation Groups, and database locks, as well as for maintaining an updated inventory and low-level system insights. Bancolombia needs to understand what kind of alerts will be available in the Connectria environment and how they can monitor the same events currently tracked by iDoctor.  


  
**4. Automations during a DR**  
Bancolombia currently uses CRO (IBM Cloud Resiliency Orchestration) provided by Kindryl to automate the DR switchover process. They are concerned about how this automation will be handled in the Connectria environment, where CRO will no longer be available. They want to know if the process will revert to manual steps or if Connectria has alternative tools for automation.  

- Not Ansible 
- they have some Auto-reply for some customer, they have some automation on the Monitoring System, but depends on the customer.
- for any ad-hoc action they wil need a ticket.


**5. DR Testing**  
Bancolombia currently conducts DR tests by operating in the alternate site for an extended period (e.g., one week). They expect to maintain this practice after migrating to Connectria. However, the commercial team believes the SoW doesn't include this type of testing. We need to align on how to address this discrepancy with the client.  

- AZ1 and AZ2? work 6 months
- We need to talk with with the customer?

  
**6. Dynatrace Agent Installation**  
Bancolombia plans to install Dynatrace agents on the LPARs. We need to confirm there are no restrictions from Connectria's side and align on whether this is compatible with the proposed monitoring model, as it could give Bancolombia visibility into equipment performance.  

- Ellos si lo pueden hacer para monitorear aplicaciones.

**7. PRI Backup to VTL Implementation and Management**  
Bancolombia has decided to use PRI for their backups, storing them on VTLs. We need to consult with Connectria on how they will handle the implementation and ongoing management of this backup strategy within their environment.  

- Josh nos dio los requerimientos

**8. Monthly and Biweekly Reporting**  
Bancolombia requires clarity on the types of reports that will be provided, including both monthly and biweekly reports. The specific reports and their frequency need to be agreed upon with Bancolombia, involving the Escala24x7 Operations team. Additionally, information about SOCKS compliance needs to be included in the reporting.  

- Josh pide un ejemplo de los reportes, para ver cuales necesitan.
- They have to special dates in the month (half-month / end-of-month).
- They have report availables on Tria on the fingertip.


**9. DB2 Support for IBMi**
- Reports about recommendation?
- Full/Open/Close?
- Related to iDoctor - Josh va respondernos sobre esto.
- Antonio puede enviar un reporte de ejemplo?
- SSAE 16: Antonio investigara el requerimiento


Thank you.



## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
