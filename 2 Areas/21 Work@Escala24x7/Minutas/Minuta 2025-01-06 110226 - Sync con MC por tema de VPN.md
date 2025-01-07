---
created: 2025-01-06T11:02:26
modified: '"2025-01-06 11:04", "1tc/G1T+6"'
date: 2025-01-06
type:
  - minuta
aliases:
  - Sync con MC por temas de VPN el 6 de Enero 2025
tags:
  - Escala24x7
IDProyecto:
---

`


## Fecha de Reunion
2025-01-06

## Asistentes

### Mobile Computing
* Federico Punta
* Martín Vasconcelos
* Nahuel Moyano
### Escala24x7
- Carlos Leonel Ramírez
- Johan Blanco
- Iliana Estupinian

## Agenda
* Objetivo: Pasarle a Fede el DevOps para construir la VPN
## Temas Discutidos
*  VPN: para Acceder desde Mobile a los recursos de AWS
	* Formulario
	* Default Gateway
	* No tienen usuario de Mobile Computing
	* Acceso Gráfico: Administración no deberían hacer ellos nada, eso lo hace Escala. Lo podemos ver con Jenny
		* Johan dice que se deben crear perfiles para MC
	* VPN IP-SEC
---
- VPN: OpenVPN Connect
	- Github Enterprise
	- Desde allí es donde va
	- Ellos tienen una IP publica fija (Mobile Computing)
	- Appliance pfsense
	- Ellos nos van a proveer la IP publica para Github
	- Ellos pueden natear la IP publica estática
---
- Accesos a endpoints del Banco
	- Una forma es tablas de enrutamiento por medio de AWS
	- Estamos revisando con Arquitectura, eso debemos definirlo en las discusiones de Arquitectura


## Puntos de Acción acordados
- Federico me comparte la IP Pública 
- Johan Blanco espera tener los CIDR, y luego nos envia el formulario


## Proxima Reunión
*   

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---
[[2025-01-02 - Indice Minutas Escala24x7]]
