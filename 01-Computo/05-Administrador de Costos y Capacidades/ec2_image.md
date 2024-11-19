![Amazon AMI](../../00_assets/Computo/ec2Image-logo.png)

[Computo](../../01-Computo/)

# 1. AWS EC2 Machine Images 

## 1.1 ¿Que es?

Es una imagen proporcionada por AWS que proporciona la información necesaria para iniciar una instancia. 

Debe especificar una AMI cuando inicie una instancia. Puede iniciar varias instancias desde una sola AMI cuando necesite varias instancias con la misma configuración. 

Puede usar diferentes AMI para iniciar instancias cuando necesite instancias con diferentes configuraciones.
Un AMI incluye lo siguiente:

- Una o más instantáneas de Amazon EBS o, para las AMI respaldadas por el almacén de instancias, una plantilla para el volumen raíz de la instancia (por ejemplo, un sistema operativo, un servidor de aplicaciones y aplicaciones).
- Permisos de lanzamiento que controlan qué cuentas de AWS pueden usar la AMI para lanzar instancias.
- Un mapeo de dispositivo de bloque que especifica los volúmenes que se adjuntarán a la instancia cuando se inicia.

Personalizacion de las instancias 
permiten definir y configurar el so, configurar herramientas de moitoreo y si creo una ami todo esto se hace mas rapido pero hay que mantenerlas o compara una en marketplace


## Informacion suelta de algun test

    -

<details>
<summary>🗒 Tarjeta: Modelo de Servicio »</summary>

| Informacion   |
| ---- |
| Sin esto no hay EC2 |

</details>


<br/>

> [Elastic Load Balancer](./elb.md)

<br/>