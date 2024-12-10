``

#minuta
## Fecha de Reunion
2024-02-20

## Asistentes

### Cliente
1. Jean-Paul Magermmans
2. Manuel Hernandez
3. Rony Reyez
4. Luis Valle
### Escala24x7
1. Carlos Leonel Ramírez
2. Luis Higuera
3. John Barrera
4. Christian Segovia

## Agenda

## Temas Discutidos

### Aplicación: Desembolso de Crédito Fácil
1. Luis Valle tiene la inquietud de porqué el componente administrativo de la aplicación, en lugar de ser una pagina web standalone, no se propuso migrarlo a Orkester.
2. Luis Higuera indica que en la información que recogimos de las entrevistas no se nos mencionó que tuviera un modulo administrativo, y por eso no se consideró.
3. Luis H indica que la razón por la que proponemos un re-platform antes de un refactor, es para buscar un "quick win", así como crear una experiencia de migración con varios  patrones de migración.
4. Luis H menciona en un refactor habría que considerar el esfuerzo y tiempo de desarrollo de código, el cual en este caso sería responsabilidad de BAM ya que no es parte de lo que haría Escala en el scope actual. Quienes mejor pueden determinar el tiempo de refactor es BAM ya que son quienes harían el esfuerzo de recodificación.
5. Luis Valle indica que se debe poner en la balanza aspectos como tiempos, costos, así como integraciones, para decidir si tomar el camino de una arquitectura transitoria (*replatform*) o una arquitectura definitiva (*Modernización con Orkester*).
6. Se mencionó la la necesidad de replantear los motivadores de BAM para ir a la nube, los cuales no son costos ni temas de disponibilidad.
7. El temor es que después del Mobilize, BAM termine con más costos y con las mismas tecnologías en la nube.
8. Luis Valle indicó que se necesita mayor información de costos,  los cuales les permitan ayudar a tomar la decisión entre algo transitorio vs. el objetivo final. 
9. Rony Reyes  indica que les gustaría ver mas detalle y basarse en el AS-IS, para determinar exactitud todos los componentes de integración que tiene esa aplicación y que cosas estaría contenerizandose y cuales quedarían en tierra. 
10. Menciona que muchas de las inquietudes surgen al comparar la metodología que utiliza BAM para un proyecto de esta naturaleza, y quisieran estar seguros que Escala tomo en cuenta las mismas consideraciones al plantear una arquitectura de nube. (entrevistas, revisión de código fuente, diagrama entidad-relación, etc..)
11. Rony consulta si el proceso de recolección de la información de las aplicaciones se está haciendo con el proceso correcto, y el compromiso debido.
12. Jean-Paul indica que el levantamiento se ha realizado las limitantes de tiempo e información que se tiene, y que el alcance del acelerador de Portafolio es tener un plan de migración, con propuestas a  un alto nivel sin llegar a mayor profundidad, son "borradores de arquitecturas", con el objetivo de iniciar conversaciones sobre si hace o no sentido.
13. Por otro lado, el Piloto de Migración, su objetivo es tener una experiencia de migración y que el propósito principal es lograr la migración en el tiempo estipulado del mobilize, mas allá de la aplicación per-se.
14. Luis Valle menciona que es necesario conversar nuevamente el tema con Aldo, para tomar una decisión.
15. Carlos Ramirez mencionó que es importante el involucramiento de los arquitectos de BAM en el levantamiento de la información para poder cubrir la mayoría de aspectos que se mencionaron, y ayudaría a aprobar la arquitectura planteada.
16. Se propone profundizar en esta aplicación con la EVC/célula y los arquitectos, y considera el componente administrativo. Se acordó buscar espacios para profundizar en esta  aplicación y hacer los ajustes necesarios en la arquitectura propuesta. #actionpoint
###  Bamavisa  y Bamavisa: Herramientas de Afiliación
1. Se reviso la arquitectura de la aplicación administrativa, que consistiría en una SPA (aplicación de página única) de front-end desplegada en S3 con CloudFront y una API con capacidades asociadas. Se sugirió DynamoDB para gestionar parámetros que podrían ser trasladados a la nube.
2. Se discutió la necesidad de identificar las funciones específicas del front-end que serían migradas, incluyendo el registro de usuarios, la gestión de límites y otros. El equipo enfatizó la importancia de entender qué funciones están aún en uso y cuáles podrían ser obsoletas.
3. El componente de notificación de transacciones implicaría mover transacciones filtradas relacionadas con usuarios suscritos de las instalaciones locales a la nube, utilizando DynamoDB y funciones Lambda. El equipo discutió el potencial de usar un lago de datos para almacenar todas las transacciones, lo cual podría mejorar otros servicios debido a la proximidad de los datos en la nube.
4. Los aspectos de reportes e inteligencia de negocios se tocaron brevemente, con la necesidad de discutir más adelante cómo se satisfarían las necesidades de reportes en la nueva arquitectura.
5. El equipo acordó enfocarse en las aplicaciones de **Bamavisa** como posible primera migración piloto a la nube. Planearon realizar sesiones técnicas detalladas para refinar la arquitectura y asegurar que las aplicaciones migradas serían funcionales y agregarían valor en el entorno de la nube.
6. Se propuso una reunión de seguimiento para incluir a las partes interesadas relevantes, como el equipo de arquitectura y los líderes técnicos, para profundizar en los detalles de las aplicaciones y finalizar el enfoque de migración #actionpoint
## Puntos de Acción acordados
1. Aplicación BAMAVISA: 
	1. Se propuso una reunión de seguimiento para incluir a las partes interesadas relevantes, como el equipo de arquitectura y los líderes técnicos, para profundizar en los detalles de las aplicaciones y finalizar el enfoque de migración
2.  Aplicación Desembolso de Crédito Fácil: 
	1. Se propone profundizar en esta aplicación con la EVC/célula y los arquitectos, y considera el componente administrativo. Se acordó buscar espacios para profundizar en esta  aplicación y hacer los ajustes necesarios en la arquitectura propuesta. 

## Proxima Reunión
1.  POR DEFINIR

`