---
created: 2025-01-08T10:30:44
modified: '"2025-01-08 10:31", "3tc/G1T+6"'
date: 2025-01-08
type:
  - minuta
IDProyecto:
  - "11248"
---

`

#minuta 
#id11248

## Fecha de Reunion
2025-01-08

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
-  

## Agenda
* 
## Temas Discutidos
* Issue con el bucket S3 para desplegar el ambiente de Desarrollo
	* Terraform state.
	* Se están haciendo pruebas con alguna política del bucket, el estado queda local, eventualmente pueda subirse al bucket S3 para hacer el despliegue. Se sigue haciendo pruebas con una policy cargando el estado remoto.
	* Con usuario programático.
	* Se espera tener respuesta hoy al final del dia
* Creación de llave KMS - ya esta completado, están desplegadas las llaves ✅
* La creación del cluster de DevOps aún esta en proceso.
* Usuario de Cori ya esta ✅
* Mayela nos va pasar el URL para la VPN, y nos confirmará por Slack las pruebas
* Las cuentas shared Escala crearía la solicitud del attachment del ambiente desarrollo
	* Esta relacionado con el despliegue, una vez resuelto el tema del bucket se puede completar y hacer la solicitud del attachment.
	* [https://we.tl/t-C0YcdsfhKh](https://we.tl/t-C0YcdsfhKh)
* Version del EKS
	* Yaxer podría buscar en el repo de Honduras.
	* Se utilizaría la misma 


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
