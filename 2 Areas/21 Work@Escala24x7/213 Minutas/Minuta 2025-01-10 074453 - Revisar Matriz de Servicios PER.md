---
created: 2025-01-10T07:44:53
modified: '"2025-01-10 07:45", "5tc/G1T+6"'
date: 2025-01-10
type:
  - minuta
IDProyecto:
  - "11236"
---

`

#minuta 
#id11236 

[[11236-CO-Davivienda-PER]]



## Fecha de Reunion
2025-01-10

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
- Jenny Rodriguez
- Johan Blanco

## Agenda
* Revisar Matriz de Servicios

## Temas Discutidos
- Jenny trabajó en esta matriz:
	- Los de Seguridad no hicieron gran cosa
	- https://docs.google.com/spreadsheets/d/13rL1bbT9fHvnSVYEyqUAWWlJyfkP-iAVFLTG1vJPXpo/edit?usp=sharing
- Cosas que todavía necesitamos aclarar:
	- [ ] Como se va publicar el sitio externo. En el diagrama nuestro dice que el sitio se iba compartir desde CAM, pero en el diagrama de Davivienda (Jenny) aparece un Imperva en CAM. #followup #id11236
		- La pregunta es como hacen para asegurar el cloudfront? 
	- ![[Pasted image 20250110075549.png]]

- El SSO que se hace el portal inicial, esa sesión o la vamos a pasar, se debe generar una nueva sesión, pero el cliente es el portal origen, toca crearle un usuario por cada originador, cuando la banca en linea llame. Debe haber un componente intermedio.
	- A nivel de infra, es habilitar los nuevos microservicios.
	- [ ] Habilitar el Security Manager #followup #id11236
		- Eso no era parte del alcance, necesitamos preguntar si es transversal.


## Proxima Reunión
*   

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---
