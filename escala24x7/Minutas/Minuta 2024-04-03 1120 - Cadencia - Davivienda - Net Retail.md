``

#minuta
## Fecha de Reunion
2024-04-03

## Asistentes

### Davivienda
1. Maria Jose Guzman
2. Andres Felipe Ramírez
3. Kimberly Priscil Salas
4. Jose Allan Rodriguez
### Escala24x7
1. Carlos Leonel Ramírez
2. Abraham Brito
3. Jonathan Urbina
4. Julio Pestana
5. Yaxer Palacioes

## Agenda

## Temas Discutidos

En la reunión se discutieron ciertas temas relacionados a las herramientas y lineamientos técnicos en cuanto al proceso de despliegue y construcción de infraestctura en el proyecto:

1. Despliegue de Infraestructura en la Nube
	1. Se mencionó que Escala en otro proyecto con Davivienda ha desplegado  la infraestructura utilizado CloudFormation en conjunto con AWS CodeX. (AWS CodeCommit, AWS CodePipeline, etc...)
	2. Se indicó que tambien soportamos el uso de Terraform para el IaaC, siempre con el uso de AWS CodeX para el despliegue.
	3. Se acordó que Escala24x7 puede iniciar el despliegue de los recursos utilizando infraestructura como código (CloudFormation o Terraform), mediante las herramientas de despliegue de AWS CodeX.
2. Despliegue del código de Lambdas
	1. Se comentó que debido a que el código para las funciones lambdas será desarrollado por Escala, y este podrá ser versionado y desplegado utilizando las herramientas normalmente utilizadas por Escala (AWS CodeX en las cuentas de Davivienda), sin embargo esta decisión no quedó en firme durante la reunión y deberá ser revisada mas adelante
	2. En caso de utilizar otro repositorio diferente a AWS CodeCommit (Github) para el código de las funciones lambda, se puede presentar el incoveniente de no poder referenciar el código que tiene la lógica de las Lambdas, en el código de la IaaC, por lo que nuestra recomendación es utilizar AWS CodeX, tanto para el IaaC como la lógica.
3. Plataforma de CI/CD para el despliegue del código.
	- Se ratificó que las herramientas utilizadas por Escala, es la suite de CodeX de AWS (CodeCommit, CodeBuild, CodeDeploy Code Pipeline).
	- En el alcance de la responsabilidad de Escala24x7 no esta la construcción de pipelines en otras herramientas diferentes a CodeX (ej. Github Actions), en tal caso esto sería responsabilidad de Davivienda.
4. Repositorio de almacenamiento de código
	- Se reiteró que en caso de requerir el uso de Github como repositorio de código, es necesario de Davivienda proveea los accesos  y gestione las licencias respectivas.
5. Bloque CIDR
	- El equipo también discutió la creación de cuentas y la validación de bloques CIDR para el proyecto. Acordaron comenzar con la planificación para la creación de cuentas y el despliegue de la infraestructura. 

## Puntos de Acción
- Definir el repositorio donde se almacenará el código de la lógica de las funciones lambda. #actionpoint#davivienda

## Acuerdos alcanzados
- Se acordó que Escala24x7 puede iniciar el despliegue de los recursos utilizando infraestructura como código (CloudFormation o Terraform), mediante las herramientas de despliegue de AWS CodeX.

## Próximos pasos
- Creación de las cuentas de AWS por ambiente, en la organización de Davivienda CAM.
- Definición de los bloques de CIDR para las VPC
- Desplegar los recursos del ambiente Dev.

## Proxima Reunión
5/4/2023





- [x] Enviar minuta ultima sesión de NetRetail, y registros de deciciones de TI #id11073
