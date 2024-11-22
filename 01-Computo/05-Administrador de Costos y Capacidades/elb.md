![Amazon Elastic Load Balancer ](../../00_assets/Computo/elb-logo.jpeg)

[Computo](../../01-Computo/)

# 1. AWS Elastic Load Balancing

## 1.1 ¿Que es?

Elastic Load Balancing distribuye automáticamente el tráfico entrante entre varios destinos, por ejemplo, instancias EC2, contenedores y direcciones IP en una o varias zonas de disponibilidad. 

Monitorea el estado de los destinos registrados y enruta el tráfico solamente a destinos en buen estado. 

ELB escala de forma automática su capacidad de equilibrador de carga en respuesta a los cambios en el tráfico entrante.

Es administrado por AWS si yo lo quiero administrar sale menos

Características:

* Alta disponibilidad
* Comprobaciones de estado
* Características de seguridad

Por que usar

* Tener un punto de acceso DNS para la aplicacion
* Checkeos de salud de las instancias
* Separa el trafico privado del publico

## 4 Tipos

### 1. Classic Load Balancer (CLB)

* Compatible con HTTP, HTTPS, TCP, SSL o CP de seguridad
**NO USAR ESTA OBSOLETO (pero se puede usar)**

### 2. Aplication Load Balancer (ALB)

* Compatible con HTTP, HTTPS, WebSocket
Funciona en la Capa 7.
Toma decisiones de enrutamiento con base en el contenido.
Por lo general se usa en arquitecturas de microservidores y contenedores.

Permite equilibrar la carga de varias aplicacines en la misma instancia EC2
Puede redirigir HTTP a HTTPS

    - Rutas basadas en URL
    - Rutas basadas en HostName
    - Rutas basadas en encabezados

#### A quien se dirige

* EC2 - HTTP (a traves de [Autoscalling](../01-Maquinas%20Virtuales/autoscalling.md))
* ECS - HTTP (a traves del propio [ECS](../03-Contenedores/ECS.md))
* [Lambda](../02-Sin_Servidor/lambda.md) - HTTP por JSON event
* IP adress

### 3. Network Load Balancer (NLB)

* Compatible con TCP, TLS (secure TCP) y UDP (Trafico para las instancias)
Opera en la capa 4
Soporta millones de solicitudes por minuto
Ultra baja latencia

Tiene una IP elastica por AZ

###### Pique de examen: Si la aplicacion puede acceder por limitadas cantidad de IP => NLB de cabeza // Trabaja sin cookies

### 4. Gateway Load Balancer (GWLB)

* Opera en la capa de Red 3 (OSI) - IP Protocol
Se implementa paara escalar y administrar su flota de red de 3ros

opera con el puerto 6081

Objetivos

* EC2
* IP adress (Privadas)

## Sticky Sessions (Session Afinity)

Permiten que los usuarios trabajen con sola una instancia evitando asi la perdida de informacion
Funciona con CLB, ALB, NLB y se trabajan mediante el uso de **COOKIES** las cuales tienen fecha de caducidad

hay 2 tipos de Cookies

| x | Aplicacion Based | Duration Based |
| :--: | :--: | :--: |
| Quien la genera: | Generada por la aplicacion se puede personalizar | Generada por el load Balancer |
| :--: | :--: | :--: |
| Nombre: | Tiene que tener un nombre | ALB - AWSALB  |
| :--: | :--: | CLB - AWSELB |

## Cross Zone Load Balancer

Cada instancia se distribuye entre AZ con el fin de equilibrar la carga

ALB

1. Esta funcion esta habilitada por defecto
2. No hay cargos por mover entre AZ

NLB y GWLB

1. Esta funcion esta deshabilitada por defecto
2. Hay cargos por mover entre AZ 

CLB 

1. Esta funcion esta deshabilitada por defecto
2. No hay cargos extra

## SSL Certificate (Secure Socket Layer)

Permiten el trafico entre los clientes y el ELB estar encriptado

## TLS Certificate Transport Layer Security

Version nueva, se usa mas pero algunos usuarios prefieren usar ssl

ELB

    * Usa X.509 Certificate (SSL/TLS) 
    * Se pueden administrar los certificados con [ACM](../../05-Seguridad_Identidad_y_Cumplimiento/Proteccion%20de%20datos/acm.md)
    * Tambien puedo subir mis propios

ELB
    * SSL

CLB
    * Soporta 1 SSL
    * Se deben usar multiples CLB con hostnames con multiples SSL

ALB - NLB
    * Soporta multibles agentes con multiples SSL
    * usa SNI  para hacerlos Funcional

## Server Name Indicator (SNI)

Soluciona el problema de tener muchos certificados pen un servidor y que estos sirvan para distintos sitios web
Solo funciona con ALB y NLB

## Derestration Delay

Especifica la cantidad de tiempo que tiene ELB que esperar para cambiar de estado
"Tiempo para que salgas antes que se muera"
Se llama asi si se usan ALB y NLB 
Si se usa CLB se llama Conection Draining

# Resumen

| - | CLB | ALB | NLB | CWLB | 
| :--: | :--: | :--: | :--: | :--: |
| Capa | :--: | Capa 7 Aplicacion | Capa 4 Transporte | Capa 3 |
| :--: | :--: | :--: | :--: | :--: |
| Protocolos | :--: | :--: | :--: | :--: |
| :--: | :--: | :--: | :--: | :--: |
| Grupos objetivos | :--: | :--: | :--: | :--: |
| :--: | :--: | :--: | :--: | :--: |
| Health Checks | :--: | Aplication Level | Network level | Instance level |
| :--: | :--: | :--: | :--: | :--: |
| Soporte de protocolo | :--: | :--: | :--: | :--: |
| :--: | :--: | :--: | :--: | :--: |
| cookie de adherencia | :--: | :--: | :--: | :--: |
| :--: | :--: | :--: | :--: | :--: |
| caracteristicas | :--: | :--: | :--: | :--: |
| :--: | :--: | :--: | :--: | :--: |
| escalabilidad | :--: | :--: | :--: | :--: |
| :--: | :--: | :--: | :--: | :--: |
| casos de uso | :--: | :--: | :--: | :--: |



<details>
<summary>🗒 Tarjeta: Modelo de Servicio »</summary>

| Tipos  |
| ---- |
| ![Tipos ELB](../../00_assets/Computo/Tipos_ELB.png) |

</details>


<br/>

> [Saving Plans](./saving_Plans.md)

<br/>