---
type:
  - minuta
IDProyecto: "11152"
date: 2024-08-20
modified: '"2025-01-09 15:16", "4tc/G1T+6"'
created: '"2024-12-16 08:13", "1tc/G12T+6"'
---
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
## Fecha de Reunión

2024-08-20

## Asistentes

### Cliente

- Jhang Felipe Gaviria
- Oscar Mauricio Morales
- John Fernando Carmona
- Pastor de los Rios
- Joan Sebastian Uribe Gil

### Escala24x7

- Carlos Leonel Ramírez
- Antonio Florez

### Connectria

- Jason Waller
- Fred Luber
- Carl Norman

## Agenda

- Discusión sobre la conexión de Direct Connect entre AWS y Connectria

## Temas Discutidos

- Se discutió con los equipos de Networking y Ciberseguridad de Bancolombia, así como con Escala24x7 y Connectria, sobre el esquema de conexión para el Direct Connect entre AWS y Connectria.
- Los puntos clave discutidos incluyen:
    - Bancolombia confirmó que la conexión se realizará a través de un Transit Gateway, que será único tanto para el tráfico productivo como para el no productivo.
    - Connectria debe aterrizar en la tabla de enrutamiento del Transit Gateway de Producción y No-Producción.
    - Connectria utilizará el proveedor [Megaport](https://docs.megaport.com/es/cloud/megaport/aws/) para esta conexión.
    - Connectria confirmó que se usará un solo Direct Connect Gateway y una sola conexión lógica mediante conexiones físicas redundantes.
    - El tráfico hacia AWS se separará entre PROD y NON-PROD mediante diferentes Transit VIFs.
    - Connectria indicó que el tráfico entrante a Connectria se separará mediante VRF y se enrutará a los firewalls de PROD y NON-PROD según corresponda.
    - El equipo de Ciberseguridad de Bancolombia estuvo de acuerdo con este esquema, siempre y cuando se asegure la separación del tráfico mediante enrutamiento.
    - Bancolombia, al ser la primera vez que utilizan un esquema con DXGW y dado que el Transit Gateway productivo está en una cuenta crítica, solicita realizar una prueba inicial en un entorno sandbox aislado con un DXGW aparte y redes ficticias para validar la conexión, evitando así el riesgo de inyectar redes no deseadas en la red productiva.
    - Oscar Morales indicó que mientras se configura y establece la conexión Direct Connect productiva, los entornos de AWS serán accesibles a través de la SD-WAN multinube, por lo que esto no debería tener un impacto significativo en las pruebas iniciales.
    - Se acordó una próxima sesión el lunes 26 de agosto a las 2:00 PM para tomar las definiciones finales, como las cuentas de AWS, etc.

## Acuerdos Realizados

- Se utilizará un esquema de conexión con un solo Direct Connect Gateway para el tráfico productivo y no productivo.
- El tráfico entrante a Connectria se separará a nivel de VRF hacia los firewalls según el entorno.
- Se realizará una prueba controlada en un entorno sandbox para validar el esquema propuesto. Bancolombia proporcionará la información necesaria.
- Las redes de AWS serán alcanzadas mediante SD-WAN multinube para las pruebas iniciales mientras se establece la conexión de baja latencia del Direct Connect.

## Próxima Reunión

- 26/08/2024 2:00 PM CST

	- 
*  AWS Account Number,  si se va terminar en un Transit Gateway
* Alinear sobre el enrutamiento CORE
	* ![[Pasted image 20240820101037.png]]
	- Connectria debería aterrizar en la tabla de enrutamiento del Transit Gateway de PDN o de QA
	- ![[Pasted image 20240820101855.png]]
	- La conexion puede aterrizar en un DXGW
	- Para separar el trafico, como debería ser la conexion fisica ( 1 o 2)
		- Seria solo una
		- Seria enrutada en el VRF para el FW Prod y non-prod
		- Oscar sugiere que se separe el DXGW para los traficos de PROD y NON-PROD

* Connectria lo hara con MegaPort
	* https://docs.megaport.com/es/cloud/megaport/aws/


- [x] Ejemplo tarea con tag #ignore
- [x] Ejemplo tarea sin tag



---
🎶
Author: Carlos Ramírez - 2024
