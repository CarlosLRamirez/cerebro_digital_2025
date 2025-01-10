---
type:
  - minuta
IDProyecto:
  - "10933"
modified: '"2025-01-10 14:12", "5tc/G1T+6"'
created: '"2024-05-20 16:46", "1tc/G5T+6"'
---
#minuta 
#id10933 

## Fecha de Reunion
2024-01-16

## Asistentes

### BAM
1. Jean-Paul Maggermans
2. Manuel Hernandez
### Escala24x7
1. Carlos Leonel Ramírez
2. Jose Mauricio Abzun
3. Jonathan Flores

## Agenda

## Temas Discutidos
1. 
hola por @aquí, saliendo de la daily con BAM, resumo lo conversado:
- Discovery por Migration Hub:
	- El día de hoy a las 8:00am aproximadamente se inició el escaneo de alrededor de 300 servidores, agrupados como Producción, sin embargo alrededor de las 9am, se detectó un alto consumo de CPU en un servidor virtualizado, por lo que se tuvo que detener.
	- Luego de detener el escaneo el consumo no se redujo, por lo que no se encontró relación con la actividad de Migration Hub. Ademas se observa que dichos servidores virtuales mantienen un alto CPU y este no esta balanceado dentro del mismo host.
	- Jean-Paul indicó que estaria llevando este punto con el gerente de Infraestructura de BAM para garantizar que la ejecución del agente de Migration Hub no coincida con otras actividades.
- Recomendaciones DevOps:
	- Se acordó que se generará un documento en el canal de DevOps de Teams  para tabular las recomendaciones del assessment y ponder llevar track del estatus y nivel de esfuerzo requerido.
- Entrevistas EVC:
	- Estamos a la espera de la programación para las reanudación de las entrevistas para el levantamiento de información de aplicaciones, de las cuales la ultima se realizó el pasado 9 de enero.
- Patch Management:
	- BAM menciona la necesidad de un workshop para revisar la solución de AWS de Patch Management, su mayor interes es poder contar con dashboards y reportería para poder integrarla con quicksight, les intersa que se tenga un alcance de varios SO.
	- Tambíen mencionan que tienen  un dolor sobre poder tener tracking de depreciaciones (po. ej. Lambdas, etc..)
## Proximos Pasos
1. Continuar con el escaneo con la herramienta de Migration Hub Estrategy Recomendations - Prioridad: ALTA
2. Continuar con las entrevistas con las EVC - Prioridad: ALTA
3. Generar el documento con recomendaciones de DevOps de forma tabulada - Prioridad: Media
4. Preparar el workshop de Patch Management - Prioridad: Media

## Proxima Reunión
1.  17/enero/2024

`