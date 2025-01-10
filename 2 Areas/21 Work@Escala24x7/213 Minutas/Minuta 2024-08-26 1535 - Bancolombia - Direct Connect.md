---
type:
  - minuta
IDProyecto: "11152"
date: 2024-08-26
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
2024-08-26

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
*  Summary:

En la reunión se discutió la conexión a un puente de tránsito, con énfasis en la redundancia en la conexión y la preparación para una prueba de conexión. También se abordó la posibilidad de utilizar la misma red de tránsito para la conexión con los firewalls, lo que generó una lista detallada de requisitos para avanzar en el proceso. Se discutió la importancia de realizar pruebas en un entorno de prueba antes de implementar cambios en producción, y se mencionó la necesidad de clarificar la configuración con el equipo de Connectria.

Además, se discutió la segmentación y conexión de los firewalls Pro y DEV, así como la configuración de la infraestructura para la conexión con Megaport. También se analizó el tráfico entre AWS y Conectria, llegando a la conclusión de que el cuello de botella se encuentra en Conectria debido a su ancho de banda limitado. Se acordó realizar pruebas de conectividad en horas de la noche para evaluar la suficiencia del ancho de banda y discutir la necesidad de ampliarlo si es necesario.


Chapters & Topics:

Discusión sobre Conexión a Transit Gateway
Durante la discusión, Oscar expresa interés en comprender la arquitectura y preparar los primeros pasos para una prueba de conexión. Fred detalla los pasos necesarios, incluyendo el número de cuenta de AWS, las redes a anunciar y las direcciones IP para las interfaces BGP tunnel. También se aborda la posibilidad de utilizar la misma red de tránsito para la conexión con los firewalls.
* Uso de SD-WAN en la conexión

Discusión sobre la configuración de redes y pruebas de conectividad.
Durante la discusión, Oscar busca claridad sobre cómo separar el tráfico de desarrollo y producción para las pruebas de conectividad. Carl explica que la conexión a Megaport es redundante y que el enrutamiento del tráfico se realizará a nivel de red, sin posibilidad de separación física.
* Configuración de redes y enrutamiento

Discusión sobre la Red de Tránsito
Durante la discusión, Carlos Leonel plantea la necesidad de una red de tránsito separada para el punto 5, mientras que Oscar Mauricio sugiere utilizar el mismo Transit Gateway. Tatiana interviene para discutir la configuración de una nueva interfaz y la provisión de la red por parte de Connectria o Banco.

Discusión sobre la Conexión y Diseño de la Infraestructura
Oscar Morales y Carl Norman discutieron la segmentación y conexión de los firewalls Pro y DEV, así como la configuración de la infraestructura para la conexión con Megaport. Se acordó programar una reunión de seguimiento para revisar el progreso y compartir los avances en el diseño de la solución.
* Conexión a Transit Gateway con un Direct Connect
* Diseño de la arquitectura de conexión

Conectividad entre Connectria y AWS
Antonio consulta a Oscar sobre la viabilidad de utilizar las particiones existentes en Connectria para conectarse a AWS. Oscar asegura que es posible, detallando la necesidad de propagar el segmento de red de Connectria en el filtro de enrutamiento de AWS. John también interviene para discutir la creación de Preferred Lists y filtros en el SD-WAN para facilitar la conectividad entre Connectria y AWS.

Discusión sobre el tráfico y la conectividad entre AWS y Conectria.
Durante la discusión, Oscar Morales y Antonio Florez abordan la preocupación sobre el tráfico entre AWS y Conectria, concluyendo que el cuello de botella se encuentra en Conectria. También acuerdan realizar pruebas de conectividad en horas de la noche para evaluar la suficiencia del ancho de banda.
* Pruebas de conectividad y capacidad de tráfico:


Action Items:

* Fred Luber proporcionará el número de cuenta de AWS y las redes a anunciar y aprender.
* Carl Norman mostrará diagramas de Megaport y los traducirá si es necesario.
* Oscar Mauricio Morales Castaño diseñará la solución y buscará en qué cuenta se realizará la conexión.
* Antonio Jose Florez Benjumea programará una reunión de punto de chequeo para el viernes a las 11 am.
* John Fernando Carmona Cardona validará el enrutamiento y los filtros entre Conectria y AWS.


Key Questions:

* ¿Cuál es el caso de uso para llegar a un general de conexión con un Transit Gateway intermedio?
* ¿Cómo se manipulan las rutas en un enrutamiento tanto en la red de desarrollo como en la red de producción?
* ¿Se espera mucho tráfico entre AWS y Connectria?


Notepad:

* No notes

## Puntos de Acción acordados
- 

## Proxima Reunión
*   

---
🎶
Author: Carlos Ramírez - 2024
