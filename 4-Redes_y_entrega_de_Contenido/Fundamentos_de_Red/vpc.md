![VPC](../../00_assets/Redes%20&%20Entrega%20de%20contenidos/vpc-logo.jpeg)

[Redes & Entrega de Contenido](../../4-Redes_y_entrega_de_Contenido/)

# 1. AWS Virtual Private Cloud

## 1.1 ¿Que es?

Permite lanzar una porcion de red aislada de manera logica para desarrollo
Puntos Positivos
    1. Admite la separacion logica de subredes
    1. Seguridad precisa
    1. Admite una conexion VPN de Hardware

*** Abarcan todas las AZ en una region y se pueden crear varias subredes en una az ***

## Informacion suelta de algun test

    * A VPN is not suitable for public web access requirements.

### Escenarios de conectividad VPC y Soluciones

![Escenarios de conectividad](../../00_assets/Redes%20&%20Entrega%20de%20contenidos/Escenarios-vpc.png)

### Caracteristicas

### Internet Gateway

| x | Info |
|:-----:|:-----:|
| ![Internet Gateway](../../00_assets/Redes%20&%20Entrega%20de%20contenidos/transitgateway-logo.png) | Permite la conexion de vpc con otra red |
|:----:| Es un componente de la VPC de escalado horizontal, redundante y de alta disponibilidad que permite la comunicación entre su VPC e internet. |
|:----:| Admite el tráfico IPv4 e IPv6. |
|:----:| No genera riesgos de disponibilidad ni restricciones del ancho de banda del tráfico de red. |



### VPC Peering

| x | Info |
|:-----:|:-----:|
| ![VPC Peering](../../00_assets/Redes%20&%20Entrega%20de%20contenidos/transitgateway-logo.png) | Permite conectar 2 subredes publicas o privadas |

<br/>

> [Transit Gateway](./transitGateway.md)

<br/>