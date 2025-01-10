---
created: 2025-01-07T09:59:23
modified: '"2025-01-07 10:00", "2tc/G1T+6"'
date: 2025-01-07
type:
  - minuta
IDProyecto:
  - "11065"
---
#minuta 
#id11065`

## Fecha de Reunion
2025-01-07

## Asistentes

### Cliente
* 
### Escala24x7
- Carlos Leonel Ramírez
- Cori Arenas 
- Nelson
- Alberto Madrid

## Agenda
* Sync interno del proyecto Whitelist
## Temas Discutidos
*  Despliegue de Laboratorio en proceso 
	* Se esta creando la infra de Laboratorio (QA), están dando errores de variable
	* Hay un segundo pipeline del código de las lambdas, ese esta pendiente
* Pruebas en Laboratorio
	* Plan de pruebas, Nelson dio un borrador.
	* Que las pruebas la creen ellos. 
	* Bajarle a las sesiones hasta que hagan una buena cantidad de pruebas
	* Que no dependan de nosotros, para cargar registros por ejemplo. Las pruebas le pertenecen a ellos. Que nos reporten si hay algún error.
* Temas de Seguridad
	* El próximo checkpoint debería ser en una cuenta de Laboratorio. Cuando todo este listo le debemos avisar a Alberto.
	* Quedó pendiente generar unas Access Keys del API, el bucket y la llave no se han generado como infraestructura como código #followup #id11605
	* No deberíamos hacer credenciales, usuarios, etc.. via IAC - Buena práctica
	* Findings de ORCA: El crítico ya esta cerrado, hay otros que tambien tiene que ver con el OpenAPI. Debemos validar con Davivienda, lo podemos ver despues. Según Alberto nosotros debemos arreglar los críticos y los altos.


---
keys = [ { name = "CampainsAPIKey" }, { name = "APIKeyCR" }, { name = "APIKeySV" }, { name = "APIKeyHN" } ]

---



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
