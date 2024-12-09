``

#minuta
## Fecha de Reunion
2024-02-01

## Asistentes

### Cliente
1. 
### Escala24x7
1. Carlos Leonel Ramírez
2. 

## Agenda

## Temas Discutidos
1. Discovery
	1. Ya hay dos servidores descubiertos (Windows y Linux), hoy en la tarde se trabaja en la base de datos.
	2. Siguientes pasos:
		1. Modificar la GPO a [Disabled](https://learn.microsoft.com/en-us/windows/security/threat-protection/security-policy-settings/user-account-control-admin-approval-mode-for-the-built-in-administrator-account).  #riesgo #id10933 
			1. Probablemente se va necesitar una documentación para poder soportar la solicitúd. Así como un período de tiempo. Esto no está en la documentación de AWS, es algo que Escala lo ha encontrado en experiencias previas.
			2. Una Alternativa sería ir haciendo el cambio por grupo de servidores. La politica tiene que estar en disabled, mientras el Estrategy este en comunicación con con los agentes.
			3. Manuel no tiene claro porque debemos deshabilitar la política.
			4. punto de accion: Edgar compartira documentación para sustentar el cambio #actionpoint #id10933 
			5. punto de accion: Edgar elevará el tema con AWS #actionpoint #id10933
			6. 
		2. Instalación desatendida
	3. Riesgo: La autorización de la modificación de la GPO , sera complicada ya que implica un riesgo de Cyberseguridad.
	4. 

## Puntos de Acción acordados
1. 

## Proxima Reunión
1.  

`