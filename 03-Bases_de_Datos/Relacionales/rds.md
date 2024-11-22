![Amazon Aurora](../../00_assets/Bases%20de%20Datos/rds-logo.jpeg)

[Bases de Datos](../../03-Bases_de_Datos/)

# 1. Relational Data Service

## 1.1 ¿Que es?

BD relacionales faciles de administrar optimizadas para el costo total de propiedad 

Puede generar copias de seguridad de distintas maneras

    1. Automatizada guardando en distintas AZ
    2. Manual

**RDS es basicamente una ec2 pero en la cual te toca administrar el motor de la bd el so lo gestiona el AWS Product Team**


## Ventajas de usar RDS vs desplegar una Base de datos en [EC2](../../01-Computo/01-Maquinas%20Virtuales/EC2.md)

RDS es un servicio administrado "Te proporciona cosas ademas de la BD"

- Aprovisionamiento esta automatizado
- Aplicaciones de parches del Sistema operativo subyacente
- Copias de seguridad (continuas o Snapshots)
- Monitoreo
- Despliegue Multi AZ 
- Escalabilidad
- Archivo esta respaldado por EBS


## RDS - Storage Auto Scalling

Sirve para todos los motores de RDS
Cuando se crea una DB RDS hay que decir cuanto almacenamiento se quiere por lo tanto esta funcion evita que te preocupes por el almacenamiento ya que escala manualmente solo cuando te quedas sin espacio


## Read Replicas for Reading Replicas

- Escalar lecturas (copia de lectura para no tocar la principal)
- Se pueden crear hasta 15 replicas en la misma AZ, a traves o cross region
- Replicas se pueden transformar en su propia BD
- Se actualizan de manera ASYNCRONICA
- USAR SOLO SENTENCIA SELECT

**USAR RR EN LA MISMA REGION ES GRATIS, EN EL CASO DE USAR CROSS REGION COBRA**


## Multi AZ (Disaster Ricovery)

- SYNC replica
- Tienen un nombre de DNS
- Aumenta la disponibilidad
- Si pierdes una AZ no pasa nada

Para pasar de 1AZ a varias no hay tiempo de demora, solo se tiene que modificar 

##### RR se pueden establecer como Multi-AZ para DR


## Custom 

##### **SIRVE UNICAMENTE PARA ORACLE, MICROSOFT SQL SERVER**
Permite personalizar el SO y BD ademas de los beneficios de RDS
Cuando se hacen personalizaciones se recomienda detener la automatizacion para no hacer cagadas


## Backup

| Automatico | Manual |
| Diariamente | Cuando al usuario quiera |
| Cada 5 min se hacen las transacciones | Estas Snapshots las puedo conservar todo el tiempo que quiera |
| permiten volver a cualquier punto guardado | 


## RDS & AURORA Security

At Rest Encryption

- Master y RR usando KMS - se define cuando se lanza 
- Si Master no se encripta => RR no pueden

* In flight Encryption
* IAM Autentication : con roles
* Security Groups : Control Network acess
* No SSH disponible


## Proxy

Reduce las fallas de opciones de restaurar en un 68%
Sin servidor, Auto Scalling, alta disponibilidad(Multi-AZ)
- Mejora el rendimiento bajando el estres de los recursos y minimizando los tiempos de conexion

No hay que tocar el codigo
solo se accede por una VPC


<br>
<details>
<summary>🗒 RDS »</summary>

| Tipo de servicio |
| ---- |
| SaaS |

</details>


## Informacion suelta de algun test

* Amazon RDS is a relational database service, not meant for storing and serving static website content.
* Amazon RDS para SQL Server es un servicio de bd sql completamente administrado al que puede migrar su bd local.
* No se necesita refactorizar ni cambiar su bd local y puede realizar migraciones homogeneas con facilidad