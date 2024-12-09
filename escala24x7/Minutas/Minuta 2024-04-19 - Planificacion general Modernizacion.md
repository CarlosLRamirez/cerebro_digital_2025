``

#minuta
## Fecha de Reunion
2024-04-19

## Asistentes

### Cliente
1. Carlos Mendez
2. Ernesto Herrera
3. Juan Pacheco
4. Pedro Gabriel
5. Rudy C
6. Wilfred Alvarez
7. Williams Coro
### Escala24x7
1. Carlos Ramirez
2. Esteban Pensotti
3. Jenny Rodriguez
4. Jose Abzum 
## Resumen

En la reunión se discutió el proceso de modernización de las aplicaciones de Cempro: AppRuteo, ODH Marcajes y Servicio Consumo NAS. Se identificaron dos líneas de trabajo paralelas: una enfocada en el proceso de transición a QA y PROD de AppRuteo, y la otra en el proceso de discovery y definición de arquitecturas para las otras dos aplicaciones. Se acordó avanzar en el despliegue de infraestructura y aplicaciones utilizando los productos de AWS Code Family.

Además, se abordó la estrategia de capacitación para el equipo de desarrollo, proponiendo la implementación de Workshops de entrenamiento para adquirir conocimientos específicos, junto con un ejercicio de transferencia de conocimiento para el ambiente de QA.

Finalmente, se avanzó en el proceso de discovery y llenado de la plantilla para la aplicación Servicio Consumo NAS. Se planificarán actividades enfocadas en esta aplicación la próxima semana, así como la organización de workshops y eventos futuros.

## Temas Discutidos

1. **Discusión sobre la Modernización de Aplicaciones**
Carlos Ramirez destaca la necesidad de alinearse en el proceso de modernización de aplicaciones, haciendo hincapié en la importancia de la planificación y la documentación para la transición a producción. Carlos Mendez y Esteban Pensotti también enfatizan la necesidad de definir un proceso claro para el traslado de conocimiento y la documentación, con el objetivo de garantizar un lanzamiento exitoso en producción.

2. **Discusión sobre Azure DevOps y Workshops**
José Abzum plantea la necesidad de definir los destinatarios de la transferencia de conocimientos y propone la realización de workshops para grupos específicos. Carlos Mendez expresa su acuerdo con continuar utilizando AWS en lugar de Azure DevOps para los repositorios, y muestra interés en la planificación de los workshops.

3. **Estrategia de Capacitación y Transición a Producción**
Jenny Rodriguez propone un plan de capacitación que incluye Workshops de DevOps y Contenedores para el equipo de desarrollo. Carlos Mendez destaca la importancia de compartir documentación y realizar sesiones de transferencia de conocimiento. Carlos Ramirez resume el plan en tres pasos: entrenamiento, preparación para el pase producción y despliegue de la aplicación en conjunto (Escala y Cempro)

4. **Discusión sobre Plataformas de Desarrollo**
Pedro Gabriel y Jenny Rodríguez debaten sobre la preferencia por Azure DevOps y la posibilidad de probar AWS, destacando la importancia de alinearse con los lineamientos del cliente. José Abzum plantea inquietudes sobre la integración de infraestructura y aplicaciones entre las plataformas.

3. **Discusión sobre el proceso de despliegue y acompañamiento en el Workshop de Despliegue**
Jenny plantea la realización de **Workshops de Capacitación** para trabajar con una aplicación ficticia, seguido de **Workshops de Despliegue** y sesiones de acompañamiento para el despliegue, con la participación activa del equipo. Carlos consulta sobre el proceso de calidad y su impacto en el despliegue, mientras que José sugiere realizar un ejercicio de transferencia de conocimiento en el ambiente de QA.

4. **Discusión detallada sobre la arquitectura y funcionamiento de la aplicación**
Jenny Rodríguez lideró una discusión detallada sobre la arquitectura y funcionamiento de la aplicación Servicio consumo NAS, abordando temas como la versión de Java, la dependencia del sistema operativo, los endpoints de la aplicación y la comunicación con el almacenamiento de Azure.

5. **Discusión sobre la modernización de la aplicación y su despliegue en contenedores.**
Jenny Rodríguez y Wilfred Álvarez revisan la disposición de los componentes de la aplicación, discutiendo la redundancia y la modernización para su despliegue en contenedores. También se aborda la comunicación entre la aplicación y el servicio de Azure, así como la necesidad de pruebas de carga en los ambientes de desarrollo y calidad.

6. **Discusión sobre Planificación y Ejecución de Proyectos**
Jenny planteó la idea de avanzar en paralelo con la próxima semana, enfocándose en la otra aplicación. Carlos expresó su acuerdo, y se acordó planificar los workshops y eventos para las próximas semanas, considerando las preferencias de los usuarios.

## Acuerdos y puntos de Acción:
- Para las tres aplicaciones a modernizar se utilizarán lo productos de AWS, como herramientas de despliegue.
- CEMPRO evaluarán para las próximas modernizaciones el uso de Azure  DevOps.
- Se acordó realizar el proceso de la transferencia de conocimiento y pase a ambientes QA y PROD para la aplicación AppRuteo en tres pasos principales:
	1. Sesiones de entrenamiento tipo Workshop para el equipo de desarrollo cubriendo temas como DevOps, Contenedores, etc.
	2. Planificación de actividad de pase a producción (QA), identificando requisitos previos, criterios de aceptación, documentación a generar, etc..
	3. Ejecución de un "Workshop de Despliegue" previamente planificado, para "acompañar" a Cempro en la transición de la aplicación de un ambiente desarrollo a un ambiente superior, el cual puede ser QA o PROD.
* La expectativa es que este proceso siente las bases y proveer a Cempro de las herramientas y el conocimiento necesario para poder realizar la transición de ambiente de el resto de aplicacióna a modernizar.

## Siguientes Pasos
- Coordinar los talleres para el equipo de desarrollo.
- Finalizar las arquitecturas objetivo de ODH Marcajes y Servicio Consumo NAS.
- Planificar la sesión de "Pase a Producción", detallando los requisitos previos, los equipos involucrados, y la documentación necesaria.
## Proxima Reunión
Por Definir  

`