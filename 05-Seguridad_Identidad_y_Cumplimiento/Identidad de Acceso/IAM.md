![Amazon IAM](../../00_assets/Seguridad,%20identidad%20y%20cumplimiento/IAM-logo.png)

[Seguridad, Identidad y Cumplimiento](../../05-Seguridad_Identidad_y_Cumplimiento/)

# 1. AWS Identity Access Manager

## 1.1 ¿Que es?

Crear y gestionar permisos para usuarios recursos y roles
Permite adminitrar de forma centralizada la autenticacion y el acceso a los recursos de aws

    - Es gratis
    - Creacio de usuarios grupos y roles
    - Aplicar politicas para control de acceso

## Cuentas

### Root Acount

* Es la que se crea por defecto **No es recomendado usarla** en cambio se recomienda crear usuarios con ella

<details>
<summary>🗒 Tarjeta: USUARIO »</summary>

| info |
| ---- |
| Representa una persona en la organizacion |
| Se pueden agrupar en grupos |


</details>
<br>
<details>
<summary>🗒 Tarjeta: Grupo »</summary>

| info |
| ---- |
| Un grupo es una asociacion de usuarios |
| Se pueden agrupar en grupos |

</details>

* Los grupos se crean mas que nada para controlar el tema de los permisos
<details>
<br>
<summary>🗒 Tarjeta: Permisos »</summary>

|  |
| ---- |
| Se escriben en formato JSON Documentation |

</details>

<br>

### IAM Politicas

Las proliticas se aplican a nuvel de grupo y afectan a los usuarios en estas, a su vez si un usuario pertenece a dos grupos le afectan ambas politicas
En cambio las politicas de linea afectan a usuarios sin grupo

Estructura:

- Version   : Lenguaje
- ID        :  identificador (opcional)
- Statement : 

    - Sid       : ID
    - Effect    : Allow / Deny (una de las 2)
    - Action    : Que puede hacer
    - Resourse  : Que recursos puede usar

#### IAM Politicas de Contraseña

Como la vida real una mejor contraseña mayor es la seguridad a su vez se aplica: 
    
    lo de usar distintos caracteres
    Cambiar la contraseña cada tanto tiempo etc

#### IAM Politicas de Contraseña Multifactor Autenticator MFA

Metodo de seguridad para el Root y IAM User.
When you enable MFA, this adds another layer of security. Even if your password is stolen, lost, or hacked your account is not compromised. 
MFA = Contraseña + otra verificacion

Dispositivos:

1. Virtual MFA  - Google Autenticatior / Authy (Celular)    -> Soporta multiples Token
2. U2F          - Yubikey (Fisico)                          -> Multiple Root (users tmb pero se necesita una llave)
3. etc

### IAM Roles

Los roles son las politicas de los servicios


#### IAM Security Tools (Tema auditorias)

1. IAM Credential Reports (A Nivel de Cuenta)

Este reporte tiene todos los usuarios de las cuentas y el estado de sus credenciales.
IAM Credentials report lists all your AWS Account's IAM Users and the status of their various credentials.

2. IAM Access Advisor (A nivel de Usuario)

Este reporte muestra los permisos de servicios otorgados y cuando se accedieron por ultima vez

<details>
<summary>🗒 Tarjeta: IAM USER »</summary>

| Para acceder a la CLI |
| ---- |
| Acess Key ID |
| Secret access Key |

</details>


<br/>

> [ACM](../Proteccion%20de%20datos/acm.md)

<br/>