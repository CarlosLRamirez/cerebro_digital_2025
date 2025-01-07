#id10908 


# Resumen General de Status y Puntos de Accion
10908 - PE- Bancom - Migración iSeries a Connectria
## Actualizacion:
[[../Tracking/Daily/2023-12-01 1]]
## 1. Inicio de replicación por Mimix
- Se confirmó la disponibilidad de un LPAR adicional en Connectria sin costo, con el objetivo de realizar la replicación por Mimix durante los meses de Diciembre  y Enero, sin sacrificar los recursos del computador productivo mientras Bancom completa las pruebas de integración y funcionales.
- Es necesario conocer la fecha estimada ese espera hacer el cutover del sistema productivo una vez completadas las pruebas.
- Esta  decisión clave  se necesita lo antes posible, y en caso se esta considerando realizar el cutover en Enero, se debe iniciar con la replicación por Mimix a más tardar el 16 de Diciembre.
- En términos generales es necesario determinar si Enero es factible o debemos empezar a considerar Febrero 2024 en adelante como fechas más realistas.
- Al momento de proceder con la replicación por Mimix, esto son los pasos necesarias en su orden:
	- Instalación de Mimix y configuración de la replica (journals en el sistema origen) - Connectria
	- Full System Save del sistema origen - Bancom
	- Envio de Cinta a Connectria - Bancom
	- Recepción de Cinta en Connectria - Connectria
	- Restauración de Journals e inicio de la replica. - Connectria

**Punto de Accion:** 
- [x] Confirmar fecha estimada de cutover así como inicio de replica por Mimix. - Escala24x7/Bancom ✅ 2024-01-05
	
## 2. Runbooks Operacionales
- Necesitamos completar la información de los Runbooks Operaciones, específicamente las secciones de:
		- IBMi Escalation
		- IBMi Backup Detail Schedule
- Ya se generó el [primer draft](https://drive.google.com/file/d/1Jo5_DCRLDzKmUq1oOorg190a2MsknZgz/view?usp=drive_link) de los Runbooks para Bancom, de acuerdo a la información recibida, sin embargo luego de la revisión con Connectria, nos solicitaron incluir mayor detalle en los mismos, como información sobre los issues y acciones a ejecutar, modificadores,  así como información sobre el manejo de backups.
- Para la sección de IBMi Escalation, Bancom nos ha solicitado el apoyo de un especialista de iSeries para trabajar en conjunto con el Percy Rojas y Angel Magallanes de Bancom, para poder definir los issues 
- El 28/Nov enviamos un [correo](https://drive.google.com/open?id=10vJfPGTeal5qlOFG_KRr7AUpLRnD9DHN&usp=drive_fs) con información sobre la información sobre la gestión de backups.
- Ell 22/Nov enviamos [información](https://drive.google.com/open?id=11-USbSHQXmuMJujUk1IMYLzM2qeqMuls&usp=drive_fs) sobre las funcionalidades de BRMS incluidas en el alcance de la propuesta, para que BRMS sean consideradas en la parte de Backups de los Runbooks, según las necesidad de Banco.

**Punto de Accion:** 
- [x] Coordinar sesion(es) de trabajo conjuntas con personal de Bancom, con especialistas de iSeries, para poder avanzar en la generación de los Runbooks operacionales. - Escala24x7/Bancom ✅ 2024-01-05
## 3.  Herramienta de Monitoreo
- Bancom consultó sobre las herramientas con contará para el monitoreo de los recursos desplegados en la nube de Connectria
- Se respondió por [correo](https://drive.google.com/file/d/10nM10mRTAP0w_WF8Y2pKgrfL2dscDCAI/view?usp=drive_link) el 28/Nov con [información](https://docs.google.com/document/d/1TH54pL-8IEH9I5EJ65jWnBFl6rnCazjk/edit?usp=drive_link&ouid=113585357126348739616&rtpof=true&sd=true) acerca del esquema de monitoreo.
- Tenemos pendiente confirmar si Bancom tendrá acceso a una herramienta o portal por medo del cual pueda monitorear los recursos desplegados.

**Punto de Accion:** 
- [x] Confirmar a Bancom sobre el acceso a una herramienta para poder monitorear sus recursos en Connectria. - Escala 24x7 ✅ 2024-01-05
## 4.  Prueba de ancho de banda en Tunnel VPN Producción
- Bancom solicito realizar una prueba de ancho de band del Tunnel VPN de Producción el cual será utilizado como canal de comunicación para la replicación por Mimix.
- La herramienta recomendada es [iperf v3/](https://iperf.fr/)
- Para esto Bancom debe instalar la herramienta en un servidor ubicado en la misma red del LPAR de BANCOMPL, y habilitar el puerto 5201 hacia la red en Connectria que desee probar, en este caso la [10.141.11.64/26

**Punto de Acción
- [x] Confirmar la instalación de la herramienta iperf y la apertura del puerto 5201, para poder coordinar dicha prueba de ancho de banda en la VPN - Bancom ✅ 2024-01-05

## 5.  Preparativos de red para DR
-  Esta pendiente la configuración y habilitación de un Tunnel VPN entre la red de Bancom y la red donde estará ubicado el computador de contingencia (DR) en Connectria.
- Para esto Bancom debe llenar el formato proporcionado y enviarlo, luego debemos coordinar una sesión para validar la configuración y habilitación del tunnel.
- Tambien debemos configurar y habilitar la conexión de Direct Connect entre la red de contingencia (DR) de Connectria con la region de DR en AWS.

**Punto de Acción
- [x] Completar el formulario de VPN DR, y coordinar sesión para habilitación del tunnel - Bancom ✅ 2024-01-05
- [x] Configurar y habilitar al conexión de Direct Connect entre AWS y Connectria para la región de DR - Escala24x7 ✅ 2024-01-05

## 6.  Proceso de resguardo de cintas desde Connectria
- Bancom a indicado que actualmente realiza un proceso de envió de de cintas físicas para resguardo (archivo) hacia un proveedor externo.
- Este mismo proceso se podría replicar desde las premisas de Connectria, sin embargo esto actualmente no esta incluido en la propuesta de servicio, esto tendría un costo adicional.
- Bancom debe confirmar si considera continuar con este proceso una vez estén en Connectria, y se realizará un proceso diferente para el resguardo de backups, tomando en cuenta los nuevos servicios y tecnologias con los que contará una vez en Connectria.

 **Puntos de Acción
- [x] Definir el proceso de resguardo de cintas (Backup) que se tendrá en Connectria - Bancom ✅ 2024-01-05
- [x] Confirmar con el equipo comercial las opciones que se tienen para satisfacer las necesidades de Bancom - Escala24x7 ✅ 2024-01-05