``

#minuta
## Fecha de Reunion
2024-04-04

## Asistentes

### Davivienda
1. Alejandro Ramirez Garnica
2. Dariel Alfonso Rincones Rivas
3. David Alejandro Romero Romero
4. Giovanni Callejas Castano
5. Julian Albear Zuleta Castillo
6. Lina Milena Mantilla Jimenez
7. Luisa Fernanda Chila Rojas

### Escala24x7
1. Carlos Leonel Ramírez
2. Alberto Madrid
3. Iliana Estupinian
4. Mario Cruz
5. Nelson Mora

## Agenda
Cadencia inter-diaria de seguimiento del proyecto
## Resumen:
En la reunión se discutió la imposibilidad de desplegar recursos en AWS debido a problemas con las licencias de GitHub, por lo que se planteó la posibilidad de utilizar CloudFormation o Terraform para desplegar recursos en las cuentas de AWS de la vivienda. También se mencionó la integración de Amazon CodeGuru y CodeBuild para revisiones de seguridad. Se acordó revisar una propuesta con David Alejandro y Alejandro Ramírez para evaluar su viabilidad y encontrar soluciones alternativas.

Carlos propuso utilizar las herramientas nativas de AWS, como CodeCommit, CodePipeline y CodeBuild, para avanzar en el proyecto y permitir al equipo desplegar el código. Finalmente, se acordó documentar la estrategia técnica y Carlos se comprometió a enviar la minuta de la reunión.

## Detalle de los puntos conversados

**Saludos y discusión sobre despliegue de recursos en AWS**
Se aborda la dificultad para desplegar recursos en AWS debido a problemas con las licencias de GitHub. Se propone utilizar CloudFormation o Terraform para desplegar recursos en las cuentas de AWS de la vivienda, y se discute la integración de Amazon CodeGuru integrado a CodeBuild para revisiones de seguridad.
* Acceso a GitHub y licencias
* Despliegue de recursos en AWS

**Discusión sobre despliegue seguro y acceso a GitHub**
Alberto Madrid presentó una propuesta para garantizar un despliegue seguro, seguido por una discusión sobre la viabilidad de la propuesta debido a problemas de acceso a GitHub. Se mencionó la posibilidad de un retraso de hasta dos semanas en el proyecto de Whitelist debido a problemas de licencias y configuración, lo que generó preocupación en el equipo.

**Discusión sobre la propuesta de implementación en AWS**
Luisa Fernanda planteó la importancia de aprobar la propuesta de implementación en AWS, seguido por la explicación de Carlos sobre el despliegue de recursos en cuentas de la vivienda CAM. Además, Carlos detalló la propuesta de utilizar las herramientas nativas de AWS, como CodeCommit, CodePipeline y CodeBuild, para avanzar en el proyecto y permitir al equipo desplegar el código.
* Propuesta de despliegue temporal utilizando herramientas de AWS
* Revisión de seguridad y almacenamiento de código en CodeCommit

**Discusión sobre la revisión de propuestas y estrategias técnicas.**
Lina pide a Alejandro revisar una propuesta con su equipo, mientras ofrece apoyo para documentar la estrategia técnica. Carlos confirma la creación de cuentas específicas para el proyecto y se compromete a enviar la minuta de la reunión, mientras que Mario y Alejandro discuten el control de cuentas de AWS.

## Puntos de Acción acordados

* Alejandro Ramirez Garnica validará la propuesta con su jefe y proporcionará una respuesta.
* Carlos Ramirez enviará la minuta de la reunión con la propuesta detallada.
* Mario Cruz proporcionará los IDs de las cuentas de AWS para dar seguimiento. ✅
		Davivienda-Whitelist-Dev-CECA  
		975049947086  
		  
		Davivienda-Whitelist-QA-CECA  
		590183949891  
		  
		Davivienda-Whitelist-Prod-CECA  
		533267004726
* El equipo técnico revisará la propuesta y proporcionará recomendaciones adicionales.
* Carlos Ramirez documentará la estrategia técnica y la enviará para revisión.

## Proxima Reunión
1.  9/04/2023


Detalle de la propuesta para desplegar recursos de manera temporal.

Lo que se propone es desplegar la infrastructura necesaria para el ambiente de Desarrollo en las cuentas de AWS creadas para este proyecto en la organización de Davivienda CAM, mediante herramientas de CI/CD de AWS (CodeCommit, CodeBuild, CodeDeploy y CodePipeline), para esto se propone utilizar productos de ServiceCatalog creados por Escala24x7, los cuales pueden utilizar Terraform como código de IaaC.

Tambien se propone integrar CodeBuid con la herramienta AWS CodeGuru, para garantizar una inspección de código estática y despliegue seguro.

Con respecto al código para la lógica de las lambdas, tambien se propone desplegarlo mediante las herramientas CI/CD de AWS, o hacerlo sin utilizar versionamiento como medida temporal.

Lo planteado anteriormente sería una solución transitoria; y nos permitirá avanzar con las pruebas de la aplicación y del API en el ambiente de Desarrollo, mientras se completa la gestión y se confirma el acceso al repositorio de Github oficial del proyecto, y se tiene todo listo para el despliegue por medio de pipelines con Github Actions, siguiendo los lineamientos de DevOps de Davivienda.

Cabe mencionar que eso requiere un re-proceso, ya que una vez se tenga acceso a las herramientas definitivas, el despliegue debe hacerse nuevamente, sin embargo consideramos que esto no tiene mayor impacto para el proyecto, y se estima que debe tomar 1 dia de trabajo como máximo.

Quedamos a la espera de su aprobación para poder avanzar con el proyecto.
`