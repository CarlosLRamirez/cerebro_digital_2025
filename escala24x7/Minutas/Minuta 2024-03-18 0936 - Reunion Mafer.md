``

#minuta
## Fecha de Reunion
2024-03-18

## Asistentes


### Escala24x7
1. Maria Fernanda Juarez
2. Carlos Leonel Ramírez
3. Lilibeth Alvarez
4. Jenny Rodriguez
5. Ivan Gil

## Agenda

## Temas Discutidos
- Mafer se va de vacaciones lunes 25, regresa el 11 de abril
- Horas Davivienda Cyberbank
	-  Actividades de NGINX en el listado con mayor consumo horas.
	- Sandra para poder justificar internamente porque va necesitar mas horas, necesita de las horas que faltan, cuantas van a requerir para terminar.
	- Hacer un cuadrito con estimación de horas:
		- 24h
		- Redondear que quede en 400 y algo.
- Reunion de Sync de EMX
	
	- Nos vamos a enfocar en los clientes Enterprise 1, Enterprise 2, SMB 1
		- La mayoria tiene Plan EMX Ultra
		- Unicomer quisa se va ir de este listado
		- Altarmirano no debe ir aqui
		- SIFCO no hemos hablado con ellos
		- Los top 5  prioritarios son
			- Magdalena
			- Bowpi
			- Banco Cuscatlan (grupo, incluye NIU)
			- Davivienda (grupo)
			- Interbanco
	- Top 5 clientes
		- Ingenio Magdalena
			- Mafer va buscar una sesión esta semana para conocer sus planes 2024, crear un roadmap, presentar al equipo EMX
		- Bowpi
			- Igual, se va buscar una reunion de presentación
		- Banco Cuscatlan (grupo)
			- Ya estamos teniendo sesiones de seguimeinto
			- Esta implementando Fabrica Digital
				- se lanzo en el 2022, la primera fase, nosotros hicimos una estimación y implementamos lo componenetes de infraestructura
				- Van a lanzar una aplicacion App3.0, banca en linea
				- Tomarion la misma infraestructura para App3.0, se requeiren mas PODS, hicieron un copy-paste, sin consultarnos.
				- El codigo que esta haciendo ellos hace que Fargate crezca unicamente hacia arriba.
				- Se estan descontrolando los costos de Fargate
				- le estan echando la culpa a la infra, pero en realidad es por la forma como funciona el código
				- se les propuso EC2 para manejar contenedores, en lugar de Fargate, pero eso les genera problemas, por la forma en vendieron el proyecto a  JD.
				- Podríamos ofrecer un assessment, para comparar precios de Fartgate vs Ec2.
				- Hay un RFP de fabrica digital honduras
					- hay una sesion el martes 19, sobre este tema.
				- Manejo operativo de EMX: Vamos a hacer una sola presentación y un solo cliente en JIRA.
				- NIU si debe estar separada
				- Se va cambiar a un modelo a un bolson de horas.
			- Davivienda (grupo)
				- Presentaciones individuales por pais, estas se le presentarán tambien a Colombia
				- Debemos incluir a Davivienda Panama, y luego a Honduras
				- Quizá mas adelante lo unifiquemos, y hagamos una aparte para Colombia 

## Puntos de Acción acordados
1. Tener sesiones de presentación de EMX para las Top 5  - Mafer
2. Sesiones de sync interna para los Top 5 - Quincenal - Carlos ✅
	 * Los clientes que no pertenecen al Top 5, se verán cada dos sesiones quincenales.
3. Los temas de operaciones no deben pasar por Mafer, deben ser canalizadas por Ivan Gil -Ivan Gil
4. Necesitamos tener un mejor control de consumo de horas de soporte (Bolson de horas). - Ivan Gil

## Proxima Reunión
1.  

`