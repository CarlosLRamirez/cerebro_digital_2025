---
created: 2025-01-09T13:34:00
modified: '"2025-01-09 13:34", "4tc/G1T+6"'
date: 2025-01-09
type:
  - minuta
IDProyecto:
  - "11065"
---

#minuta 
#id11065
## Fecha de Reunion
2025-01-09

## Asistentes

### Cliente
* Carlos David Robayo
* Jose Miguel Vanegas
* Lina Milena Mantilla
* Luisa Daniela Carreno
* Luisa Fernanda Chilla
* Miguel Leonardo Chaparro
### Escala24x7
- Carlos Leonel Ramírez
-  Nelson Mora

## Agenda
* 
## Temas Discutidos
* Ya se pudo desplegar la infra en laboratorio! 🥳 🎉
* Ahora empiezan las pruebas de conectividad
	* ![[Pasted image 20250109133417.png]]
	* ![[Pasted image 20250109133414.png]]
	* 
	* [ ] Necesitamos las URL (endpoint) #followup #id11065
		* Ruta PI Gateway Laboratorio: [https://7n863inyi2.execute-api.us-east-1.amazonaws.com/qa](https://7n863inyi2.execute-api.us-east-1.amazonaws.com/qa)  - Informaremos los ApiKeys por cada pais pro separado
Informaremos los ApiKeys por cada pais pro separado
* [ ] Comentarios de checkops #followup #id11065 
	* Con Nelson van a ir haciendo una revisión uno por uno
* Pendiente Limpiar el resto del código comentado #followup #id11065
* Ya no tenemos ningun finding de ORCA (vulnerabilidad)
* [ ] Documentación de API  #followup #id11065
* Aplicar medidas de Seguridad a los API Keys #followup #id11065
* [ ] Parameter Store:  Quien crea los parametros?  #followup #id11065
	* Carlos David Robayo lo revisara.
	* Según Jose Miguel Vanegas, se deben crear manualmente, y los debe crear Escala24x7
	* Nelson los creará
* [ ] Los tópicos de SNS se hicieron manualmente #followup #id11065
	* Había un pendiente del módulo de Davivienda que nos bajaba la version del provider de Terraform para AWS.
		* source = "github.com/davivienda-colombia/davi-coe-aws-sns-module-iac?ref=v1.0.0"
	* DE acuerdo con Carlos Robayo, el módulo ya se actualizó


## Resumen de lo que nos falta
- Validar la comunicación hacia los endpoints de los API Key
- Nelson creará los Parametros de Parameter Store
- 
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
