
`Minuta 2023-12-07 - Reunion BANCOM sobre Runbooks
#minuta
##  Fecha de Reunion
2023-12-07

## Asistentes

### Bancom
1. Juan Carlos Miranda
2. Angel Magallanes
3. Percy Rojas
### Escala24x7
1. Carlos Leonel Ramírez
2. Cesar Gomez
3. Gabriel Fernandez

## Objetivo de la Reunión
Sesión de trabajo para generación de runbooks operaciones IBMi
## Temas Discutidos

### **1. Encriptación de Backups** 
- Bancom solicita conocer con que mecanismos podría contar (ya sea dentro del alcance actual o como alcance adicional) para poder tener backup encriptados.
- Necesita que confirmemos si contaría con encriptación en alguna estas opciones:
	- a nivel de Tape
	- a nivel de SW en el LPAR (BRMS)
	- utilizando IBM Security Key Lifecycle Manager (SKLM)
- Actualmente Bancom no realiza cifrado de sus backups
- Bancom solicita que confirmemos si se utilizarán Tapes físicos o serán Tape virtuales (y como se garantiza que estos sean encriptados)
- Según sean aclaradas las consultas anteriores, se tendrá mayor claridad sobrela información a colocar en los backups.

### **2. Backup, Recovery and Media Services (BRMS)**
- Bancom solicita conocer cuales serian los costos asociados por contar con las funcionalidades avanzadas de BRMS.
- Relacionado al punto no. 1

### **3. Resguardo de cintas (archive)**
- Bancom solicita que confirmemos cuales son las opciones propuestas para el resguardo de cintas (archivo), esto se relaciona con la consulta sobre si se tendran cintas físicas o virtuales
- En la operación actual, Bancom envía una copia del backup diario a su proveedor (Iron Mountain) en el Perú.
- También solicita conocer cual seria el tiempo de respuesta, en caso de recuperación a partir de cinta.

### **4. Cierres en la Operación diaria de Bancom** 
- Bancom inidica que en su operación diaria realiza "cierres" a las 8:30PM, sin embargo estos pueden retrasarse hasta las 11PM.
- El operador realiza un backup previo al cierre y otro al finalizar el cierre. 
- Cuando este backup no se puede realizar el backup por haber usuarios conectados, realizar un "backup a contingencia", es decir detienen Mimix y realizar el backup en el LPAR de contingencia, luego trasladan la cinta manualmente al sitio principal.
- Es necesario definir como funcionaría esta operación una vez en Connectria, y esto de alguna forma debe quedar reflejado en los runbooks operacionales.
- Este punto esta relacionado a la disponibilidad de la solución de BRMS

### **5. Escalamientos para eventos iSeries**
- Juan Carlos Miranda indicó que actualmente se monitorean subsistemas, time-outs, canales, umbrales de ASP, entre otros; este detalle está especificado en el Libro de Operaciones de Telefónica.
- El señor Miranda indicó que solicitará el Libro de Operaciones a Telefonica para utilizarlo como base.

## Puntos de Acción acordados
- Trasladar las consultas de Bancom en relación a la gestión de respaldos, y coordinar alguna sesión técnica para aclarar dudas con el equipo de operaciones de Escala24x7/Connectria - Carlos Ramírez
- Solicitar el Libro de Operaciones de Telefónica, para poder tomarlo como base para la construcción de los runbooks operacionales .

## Proxima Reunión
Por Definir  

===========

Hola a todos

  

Adjunto por este medio la minuta de lo conversado en la última reunión, con respecto al tema de los runbooks operacionales, así como los puntos de acción acordados.

## Fecha de Reunión

## 

2023-12-07

## [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_asistentes)Asistentes

### [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_bancom)Bancom

## 

1. Juan Carlos Miranda
2. Angel Magallanes
3. Percy Rojas

### [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_escala24x7)Escala24x7

## 

1. Carlos Leonel Ramírez
2. Cesar Gomez
3. Gabriel Fernandez

## [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_objetivo-de-la-reuni%C3%B3n)Objetivo de la Reunión

## 

Sesión de trabajo para generación de runbooks operaciones IBMi

## [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_temas-discutidos)Temas Discutidos

### [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_1-encriptaci%C3%B3n-de-backups)1. Encriptación de Backups

## 

- Bancom solicita conocer con que mecanismos podría contar (ya sea dentro del alcance actual o como alcance adicional) para poder tener backup encriptados.
- Necesita que confirmación cs si contaría con encriptación en alguna estas opciones:
    - a nivel de Tape
    - a nivel de SW en el LPAR (BRMS)
    - utilizando IBM Security Key Lifecycle Manager (SKLM)
- Actualmente Bancom no realiza cifrado de sus backups
- Bancom solicita que confirmar si se utilizarán Tapes físicos o serán Tape virtuales (y cómo se garantiza que estos sean encriptados? )
- Según sean aclaradas las consultas anteriores, se tendrá mayor claridad sobre la información a colocar en los backups.

### [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_2-backup-recovery-and-media-services-brms)2. Backup, Recovery and Media Services (BRMS)

## 

- Bancom solicita conocer cuáles serían los costos asociados por contar con las funcionalidades avanzadas de BRMS.
- Relacionado al punto no. 1

### [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_3-resguardo-de-cintas-archive)3. Resguardo de cintas (archive)

## 

- Bancom solicita confirmación sobre cuales son las opciones propuestas para el resguardo de cintas (archivo), esto se relaciona con la consulta sobre si se tendrán cintas físicas o virtuales
- En la operación actual, Bancom envía una copia del backup diario a su proveedor (Iron Mountain) en el Perú.
- También solicita conocer cuál sería el tiempo de respuesta, en caso de recuperación a partir de cinta.

### [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_4-cierres-en-la-operaci%C3%B3n-diaria-de-bancom)4. Cierres en la Operación diaria de Bancom

## 

- Bancom indica que en su operación diaria realiza "cierres" a las 8:30PM, sin embargo estos pueden retrasarse hasta las 11PM.
- El operador realiza un backup previo al cierre y otro al finalizar el cierre.
- Cuando este backup no se puede realizar el backup por haber usuarios conectados, realizar un "backup a contingencia", es decir detienen Mimix y realizar el backup en el LPAR de contingencia, luego trasladan la cinta manualmente al sitio principal.
- Es necesario definir cómo funcionará esta operación una vez en Connectria, y esto de alguna forma debe quedar reflejado en los runbooks operacionales.
- Este punto está relacionado a la disponibilidad de la solución de BRMS

### [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_5-escalamientos-para-eventos-iseries)5. Escalamientos para eventos iSeries

## 

- Juan Carlos Miranda indicó que actualmente se monitorean subsistemas, time-outs, canales, umbrales de ASP, entre otros; este detalle está especificado en el Libro de Operaciones de Telefónica.
- El señor Miranda indicó que solicitará el Libro de Operaciones a Telefonica para utilizarlo como base.

## [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_puntos-de-acci%C3%B3n-acordados)Puntos de Acción acordados

## 

- Trasladar las consultas de Bancom en relación a la gestión de respaldos, y coordinar alguna sesión técnica para aclarar dudas con el equipo de operaciones de Escala24x7/Connectria - Carlos Ramírez
- Solicitar el Libro de Operaciones de Telefónica, para poder tomarlo como base para la construcción de los runbooks operacionales .

## [](https://mail.google.com/mail/u/0/#m_-5368660169419335912_proxima-reuni%C3%B3n)Próxima Reunión

## 

Por Definir