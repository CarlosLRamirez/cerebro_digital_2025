---
created: 2025-01-07T13:32:22
modified: '"2025-01-07 13:33", "2tc/G1T+6"'
date: 2025-01-07
type:
  - minuta
IDProyecto:
  - "11065"
---

`

#minuta 
#id1165

## Fecha de Reunion
2025-01-07

## Asistentes

### Cliente
* Carlos David Robayo
* Freddy Alexander
* Jose Miguel Vanegas
* Lina Milena Mantilla
* Miguel Leonardo Chaparro
* Luisa Fernanda Chila
### Escala24x7
- Carlos Leonel Ramírez
- Nelson Mora
- Iliana Estupinian
- Cori Arenas

## Agenda
* Sync de proyecto con el cliente
## Temas Discutidos
*  Existe un issue en el despliegue con el pipeline de IaC hacia laboratorio en el Apply
	* Carlos Robayo dice que esta relacionado con el código
	* Cori dice que esta trabajando el los fixes necesarios
* En el repositorio que tiene el código de las Lambdas
	* Este depende que el de infraestructura este desplegada
	* Jose Miguel Vanegas indica que se necesitan unas credenciales de AWS (el ARN del usuario). - arn:aws:iam::590183949891:role/OIDC-Davivienda-CAM-Role-3WXCI0o75Qor
		* Con eso se puede obtener la credencial
* Siguientes pasos
	* Revisar comunicación con Ciberseguridad Banco y Escala24x7
* Pruebas funcionales
	* Costa Rica ya tiene un plan de pruebas, lo vamos a ver el jueves, ya que tienen algunas dudas sobre los documentos que deben ambientar, ellos ya tienen un set de pruebas propuesta, Lina espera compartirmelo entre el jueves o viernes.
* 

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
