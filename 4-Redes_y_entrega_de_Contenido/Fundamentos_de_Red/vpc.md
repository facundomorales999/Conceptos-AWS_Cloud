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
| ![VPC Peering](../../00_assets/Redes%20&%20Entrega%20de%20contenidos/vpcPeering-logo.png) | Permite conectar 2 subredes publicas o privadas, permite enrutar el tráfico entre ellas mediante direcciones IPv4 o IPv6 privadas |
|:----:| Las instancias en cualquiera de las VPC pueden comunicarse entre sí como si estuvieran dentro de la misma red.  |
|:----:| Puede crear una conexión de intercambio de tráfico de VPC entre sus propias VPC o con una VPC en otra cuenta de AWS. |
|:----:| Las VPC pueden estar en diferentes regiones (también conocida como interconexión de VPC entre regiones). |


### Tablas de Enrutamiento

| x | Info |
|:-----:|:-----:|
| ![Tablas de Enrutamiento]() | Contiene conjunto de reglas llamadas rutas que determinan donde se dirige el trafico de red, desde su subred o la Internet Gateway |
|:----:| Controlan cómo se dirige el tráfico de red hacia adentro, hacia afuera y alrededor de una VPC. |

<details>
<summary>🗒 Tarjeta: Enrutador »</summary>

| Tipos de escalado |
| ---- |
| Conecta varios segmentos de red en una red para formar una red mayor |
| Opera en las capaz 2 y 3 de OSI |

</details> 

### Flow Logs 

| x | Info |
|:-----:|:-----:|
| ![Flow Logs](../../00_assets/Redes%20&%20Entrega%20de%20contenidos/flowLogs-logo.png) | Permite capturar informacion sobre el tráfico de IP que entra y sale de las interfaces de red en su vpc |
|:----:| Los datos de registro de flujo se pueden publicar en las siguientes ubicaciones: CloudWatch Logs, S3 o Data Firehose. |

|:----:| Después de crear un registro de flujo, puede recuperar y ver los registros de registro de flujo en el grupo de registros, el depósito o la secuencia de entrega que haya configurado. |
|:----:| Los registros son útiles para:
    * Monitoreo
    * Diagnostico
    * Análisis |

### Nat Gateway 

| x | Info |
|:-----:|:-----:|
| ![Nat Gateway](../../00_assets/Redes%20&%20Entrega%20de%20contenidos/natGateway-logo.png) | Puede utilizar una puerta de enlace NAT para que las instancias de una subred privada puedan conectarse a servicios fuera de su VPC, pero los servicios externos no puedan iniciar una conexión con esas instancias. |
|:----:| Redundancia integrada dentro de una zona de disponibilidad |
|:----:| Requiere de una dirección IP elástica |
|:----:| Admite los protocolos:
    * Protocolo de control de transmisión (TCP)
    * Protocolo de datagramas de usuario (UDP)
    * Protocolo de mensaje de control de Internet (ICMP) |

### ACL de Red

| x | Info |
|:-----:|:-----:|
| ![ACL de Red](../../00_assets/Redes%20&%20Entrega%20de%20contenidos/acldeRed-logo.png) | Permiten o deniegan el tráfico dentro y fuera de las subredes |
|:----:| Endurece la seguridad como nivel secundario de defensa a nivel de subred |
|:----:| ACL de red predeterminada: 
    * Permite todo el tráfico entrante y saliente |
|:----:| Sin estado
    * Incluso si las reglas permiten que el tráfico fluya en una dirección, debe permitir explícitamente que las respuestas fluyan en la dirección opuesta. |

### host bastion

| x | Info |
|:-----:|:-----:|
| ![Host Bation](../../00_assets/Redes%20&%20Entrega%20de%20contenidos/hostBation-logo.png) | Proporciona acceso de subred pública a subred privada. |
|:----:| No almacene claves privadas en el host del bastión. |
|:----:| Para las instancias de Linux, utilice la función de reenvío de agentes del cliente de Secure Shell (SSH) para especificar la clave. |
|:----:| En el caso de las instancias de Microsoft Windows, descifre la contraseña con la clave en la consola de Amazon EC2 y, a continuación, añada la instancia a un dominio |



<br/>

> [Cloud Front](../Redes_Perifericas/coludFront.md)

<br/>