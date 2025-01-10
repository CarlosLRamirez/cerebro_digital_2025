---
created: 2025-01-09T10:31:13
modified: '"2025-01-09 10:31", "4tc/G1T+6"'
date: 2025-01-09
type:
  - minuta
IDProyecto:
  - "11248"
---
#minuta 
#id11248

## Fecha de Reunion
2025-01-09

## Asistentes

### Cliente
* Isaias Palacios
* Carmen Yanes
* Alejandro Amaya
* Jonathan Cruz
### Escala24x7
- Carlos Leonel Ramírez
- Jenner Fernandez

## Agenda
* 
## Temas Discutidos
*  Siguen los inconvenientes para desplegar el ambiente Dev #followup #id11248
	* No deja leer el archivo que es parte del código, lo cual sirve para completar el despliegue del EKS.
	* Se está pensando en la alternativa de hacer el despliegue de ese cluster desde el Jenkins de El Salvador, y paralelamente seguir trabajando en los permisos de los buckets.
* Cluster de CI/CD (DevOps)
	* El VPC ya pasó.
* Si logramos resolver el tema del despliegue del ambiente de Dev pudiéramos continuar de esta manera, hasta tanto se tenga el ambiente CI/CD.
	* Si no lo podemos hacer el día de hoy, ya habría que levantar la mano. Porque ya nos quedaría tres días para trabajar.


## Puntos de Acción acordados
- 

## Proxima Reunión
*   

--- 
## Pendientes

```dataview
TASK
WHERE contains(tags, "#followup") AND contains(tags, "#id" + this.IDProyecto) AND !completed
```

---
