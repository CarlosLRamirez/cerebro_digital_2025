---
created: 2024-12-30T20:47:08
modified: '"2024-12-30 20:47", "1tc/G12T+6"'
type: 
aliases: 
tags:
  - AWS
---



## AWS Account 175084778683
- ID 175084778683
- URL
	  https://carloslrm.signin.aws.amazon.com/console
- Root
	- carloslrm@gmail.com
	- MFA: Google Authenticator
- Info General
	- Account 175084778683
- Recursos/Bitacora:
	- ~~aqui estan los recursos desplegados para Macoinsa~~
    - ~~Marzo/21/2023 borre casi todos los recursos, solo deje los snapshots de las EC2~~
    - **Aqui esta el DNS de Syprotec y de carloslramirez.com**
    - 24/Mayo/2023: borre los snapshots de las EC2 y desactive Security Hub
    - 24/Mayo/2023: Borre la organización, quedo como cuenta stand-alone
    - TODO: aquí quiero crear un bucket S3 para guardar mi información importante en Glacier Deep Archive
- Consumos:
	- 24/Mayo/2023: consumo \$1.00 de R53 mensual, + ( ~~$.03 Security Hub, $.02 EC2other~~   centavos por los Logs de CloudTrail)—> diario
    - 03/Abril/2024: Facturación $1.06
    - 8/abril/2024
	    - IAM: clramirez
	    - Google Authenticator
	    - Facturacion $ 1.00

## AWS Account  211125564016 (CERRADA)
- Root
	- carloslrm+mys@gmail.com
    - C^69Q7Hz1J%KJ3N&6z^^!&xX
    - MFA: MS Authenticator, Escala Key
- Info general
        - Account ID: 211125564016
        - 895591877452
        - cuenta stand-alone
        - https://211125564016.signin.aws.amazon.com/console
- User IAM: carlos.ramirez
        - 9$@x8WjnhQnCvEoqY5mC
        - MFA: Escala Key
- Bitacora
        - 28/Enero/2024: Aqui voy a desplegar recursos para el curso de modelado y simulación
        - 2/Mayo/2024: **Inicié el proceso de borrado de la cuenta**
        - 8/Junio/2024: aparentemnete esta cerrada
        - 10/Junio/2024: esta cuenta en Mayo 2024 todavia me genero USD 19.50 🚩
        - ![](Pasted%20image%2020240610113139.png)

## Organización Syprotec

### URL

SSO URL: https://syprotec.awsapps.com/start
Correo: carlos.ramirez@syprotec.com.gt
### Organización

- SyprotecMaster
	- Management Account
	- 245923315880
	- carlos.ramirez@syprotec.com.gt
-   Labs General Account
	- 412462643366
	- carlos.ramirez+lab_general@syprotec.com.gt
- Audit
	- 180091017331
	- carlos.ramirez+audit@syprotec.com.gt
- Log Archive
	- 547190111891
	- carlos.ramirez+logs@syprotec.com.gt
### Bitacora
- 245923315880: el 15/01/2023 removí el usuario IAM
	- Root MFA: EscalaKey y GoogleAuth en el Iphone
	-  24/05/2023: Despliegue Control Tower, según esta [guía](https://catalog.workshops.aws/control-tower/en-US):
	- 07/01/2024: Esta generando un costo de $USD 0.7 mensualmente  
	- 10/06/2024: Facturación $0.42/m aprox,
-  Labs General Account 412462643366



## Organización CarlosVsSAP

SSO URL: [https://carlosvssap.awsapps.com/start/#/](https://carlosvssap.awsapps.com/start/#/)
- `https://carlosvssap.awsapps.com/start`
- SSO federado a la cuenta de Syprotec
Estan asociadas al correo carlosvsccnp@gmail.com

- CARLOSVSSAP-GENERAL
	- Management Account
    - 895591877452
    - carlosvsccnp+general@gmail.com
    - [https://carlosvssap-general.signin.aws.amazon.com/console](https://carlosvssap-general.signin.aws.amazon.com/console)
    - Root MFA
	    - EscalaKey
	    - 
- CARLOSVSSAP-PRODUCTION
    - 895591877452
    - carlosvsccnp+production@gmail.com
    - [https://carlosvssap-production.signin.aws.amazon.com/console](https://carlosvssap-production.signin.aws.amazon.com/console)
- CARLOSVSSAP-DEVELOPMENT
    - 218378085552
    - [carlosvsccnp+development@gmail.com](mailto:carlosvsccnp+development@gmail.com)
    - created from the AWS Organizaton
    - Esta voy a user para el Terraform Bootcamp
- learning-awsdeveloper Account 058264233782
	- Cuenta nueva creada el 17/julio/2024 desde AWS Organizations
	- carlosvsccnp+devopsdev@gmail.com
	- No root password
	- 11/Ago/2024: Aqui voy a crear un custon VPC siguiente el tutorial de Adrian Cantril




## Nuevas cuentas standalone para Laboratorios 2025
- DevOps2024 General
	- Account
		- 730335545146
		- https://devops2025-general.signin.aws.amazon.com/console
	- Root
		- carlosvsccnp+devops2024genera@gmail.com
	- usuario IAM: IAMAdmin
		- MFA: Google Authenticator
		- MFA: EscalaKey
- DevOps2024Production
	- Account:
		- 796973506233
		- https://devops2025-production.signin.aws.amazon.com/console
	- Root
		- carlosvsccnp+devops2024production@gmail.com
	- usuario IAM: IAMAdmin
		- MFA: EscalaKey
		- MFA: PassKey(MAC/Brave)??



carlosvsccnp+awspractical1@gmail.com
AWSPractical1
257394448697
ufs#4vP$hc#N4d!KBU$11*mq
Solicitud de cierre el 12Nov2024




carlosvsccnp+awspractical2@gmail.com
AWSPractical2
474668419929
Retalhuleu1@334..
Solicitud de cierre el 12Nov2024



## Historial de Consumos



| Mes      | 175084778683<br>carloslrm@gmail.com | 211125564016<br>carloslrm+mys@gmail.com | Organizacion <br>Syprotec <br>245923315880 | Organización<br>CarlosvsSAP |
| -------- | ----------------------------------- | --------------------------------------- | ------------------------------------------ | --------------------------- |
| Ene 2024 | 1.06                                | 0.67                                    | 0.56                                       | 0.01                        |
| Feb 2024 | 1.06                                | 28.15                                   | 0.41                                       | 0.01                        |
| Mar 2024 | 1.06                                | 0.62                                    | 0.47                                       | 0                           |
| Abr 2024 | 1.06                                | 0.65                                    | 0.42                                       | 0                           |
| May 2024 | 1.06                                | 19.50                                   | 0.45                                       | 0                           |
| Jun 2024 | 1.03                                | -                                       | 0.63                                       | 0                           |
| Jul 2024 |                                     | -                                       |                                            |                             |
| Aug 2024 |                                     | -                                       |                                            |                             |
| Sep 2024 |                                     | -                                       |                                            |                             |
| Oct 2024 |                                     | -                                       |                                            |                             |
| Nov 2024 |                                     | -                                       |                                            |                             |
| Dic 2024 |                                     | -                                       |                                            |                             |
