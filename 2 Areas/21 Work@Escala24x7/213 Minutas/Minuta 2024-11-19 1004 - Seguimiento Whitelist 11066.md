---
type:
  - minuta
IDProyecto:
  - "11065"
date: 2024-11-19
modified: '"2025-01-10 14:42", "5tc/G1T+6"'
created: '"2024-12-16 08:13", "1tc/G12T+6"'
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
2024-11-19

## Asistentes

### Cliente
* Lina Mantilla
### Escala24x7
- Carlos Leonel Ramírez
- Cori Arenas
- Iliana Estupinian
- Eva Castaneyra

## Agenda
* 
## Temas Discutidos
* [x] Conectividad Ambiente DEV  #id11065
	* Aún hay unos problemas con SuperApp
	* Luego de los cambios de Jhonatan dicen que siguen
	* Cori realizó unos cambios y le va decir al cliente que vuelva a probar.
	* Se implemento un ALB, el cual no era parte de la infraestructura original (MBaaS o SuperApp).
* Pipelines
	- [x] Ayer que se tuvo reunion con Carlos y Daniel, y hay cambios solicitados de refactorización de código. Iliana estaría trabajando en eso  #id11065
		* Eso nos impactaría la infra otra vez
		* Son los últimos cambios que pidió seguridad.
* Desarrollo
	* [x] Nelson aún tienen algunos pendientes cosméticos, a nivel de Lambdas  #id11065
	* [x] El tema de las suscripción con Honduras ya se solventaron?  Nelson cree que hicieron click a correos viejos.. #followup ✅ 2024-11-19
		* Nelson dice que ya todas están aceptadas
	* [x] Hay un error de comunicación con GoAnywhere Lina lo esta revisando internamente, puede que sea causa de los cambios en KMS. Se necesitará una sesión #iid11065 ✅ 2024-12-16
		* was unexpectedly interrupted. User: arn:aws:iam::975049947086:user/ForGoAnywhere is not authorized to perform: kms:GenerateDataKey on resource: arn:aws:kms:us-east-1:975049947086:key/bcc944ae-4063-4601-b7ca-9cfc931df8e6 because no identity-based policy allows the kms:GenerateDataKey action (Service: Amazon S3; Status Code: 403; Error Code: AccessDenied; Request ID: 9ESK0RXY2FBGP4BW; S3 Extended Request ID: apAvbncJPf0wuKykzzhyxZIqHtgon2OeFKyVDiktiKeWoBdy7WMUaGNqhMF+vSnvUAC06TZxQTc=; Proxy: proxy

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
