``

#minuta
## Fecha de Reunion
2024-03-22

## Asistentes

### Cliente
1. Cesar Daniel Lemus
2. Eddy Rodrigo Barales Cruz
3. Mario Arturo Gaitan
### Escala24x7
1. Carlos Leonel Ramírez
2. Aldo Preciado
3. Eva Castaneyra
4. Jose Mellado - Seguridad
5. Juan Carlos Hernandez

## Agenda

## Temas Discutidos
1. Despliegue de Control Tower (Cloud Foundation)
	1. 6 cuentas: Audit, DevOps, Log Archive, Master, Network, Security
	2. Security y Network tiene VPC
		1. Subnets, Routing Tables, Internet Gateway
	3. Todo desde Service Catalog, con pipelines
		1. Transit GW, Roles, etc..
2. Security Baseline
	1. Inspector, Security Hub, GuardDuty, SCPs
	2. Alertas de CloudTrail y notificaciónes de Security Hub
	3. Falta que GyT indique los usuarios
		1. Grupos y permition sets.
		2. Eso es antes del PaO. Vamos a ver si hacemos PaO de CT.
	4. Avance del 95%
3. Siguientes pasos:
	1.  Migración de cuentas hacia el Control Tower, buscar un espacio la siguiente semana (Edson y Eddy) - Edson no va estar. seria hasta la proxima despues de SS.
	3. Eva hara lllegar un documento para la migración: servidores (no kubernetes), queremos dejarlo asentado en un acuerdo de cambios , a Edson y Mario - JuanK ya habló con Edson
	4. Nos falta realizar un levantamiento, pero queremos terminar primero con el control tower
	5. 
4. Dudas de Mario
	1. Los no k8s son los que no modifican el alcance (se pueden migrar en lift&shift)
	2.

===========
- Diagrama de arquitectura? o cuentas?
- Revisar el backlog y lo que ya se hizo
===========
- Edson es el jefe
- Mario es el PM
===========
- hay 8 cuentas, fuera de CT, las cuales de deben migrar
- tienen Direct Billing con nosotros
- 
## Puntos de Acción acordados
1. 

## Proxima Reunión
1.  

`