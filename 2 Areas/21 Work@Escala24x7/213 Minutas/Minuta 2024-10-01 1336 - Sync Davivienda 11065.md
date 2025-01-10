---
type:
  - minuta
IDProyecto: "11065"
date: 2024-10-01
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
2024-10-01

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
- Iliana Estupinian


## Agenda
* 
## Temas Discutidos
* Tenemos bloqueo con el ambiente de QA (Laboratorio)
	* Por el tema de los pipelines
* Pruebas de Canal
	* Comunicacion y resultados de las Novedades: Se finalizaron a satisfacción, en ambiente de integracion
	* Prueba de base de campañas cargadas, novedades y demas:
		* Pendiente la codificacion de los Emojis, estan quedadnco como carateres especiales en el canal, los emojis siguen quedando como caracteres ene l Front - Compromiso con Nelson. El equipo d eNegofio nos apoyo con dos tipos de codificaciones, se estan haciendo pruebas con Costa Rica
		* Honduras y El Salvador, no les llegan notificaciones, Nelson nos esta ayudando a confirmar de volver a generar. Joel genero nuva invitaciones, neceistamos recibir feebdack de Joel, si estamos recibiendo la campaña. Davivienda sigue sin recibir novedades de HN y SV #followup
	* Archivo de Salida: quedo un pentiente, que no se estaba presnetado una columna, Nelson quedo pendiente de revsiar qaue esa columnano esta definida, estaba en la definicion. Seguimos esperando a Nelson. #followup
	* Lina enviara una solcitiud porque el correo de alertas de campañas, y el archivo de novedades, esos correos estan siendo muy de la plataforma, nos van a pedir como quieren que sea el asunto y como organizar el contenido del correo. Lo que reciben no les gusta, dice AWS notifica. Nelson habia pedido la propuesta. Lina enviara el correo con la propuesta #followup
* MBaSS
	* Ya con lo que se tiene Carlos Robayo puede avanzar
	* Ya se pidio la configuraciòn en el ambiente de laborario para lacanzar la API en ambos path. #followup
- Lina esta apuntando para tener toda la comunicacion lista, el 3 de octubre, si no porlo menos al cierre de la semana. Pero por mucho no deberiamos extender al **viernes 11, pero NO MAS.**
- Nos falta la prueba de LABORATORIO para hacerlo por el DNS #followup
	- Relacionado con lo del ALB
	- En desarrollo esta con tabla de host
	- 

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
