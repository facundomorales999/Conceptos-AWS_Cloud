![Amazon Api GateWay](../00_assets/Integracion%20de%20Aplicaciones/apiGateway-logo.png)

[Integracion de Aplicaciones](../9-Integracion_de_Aplicaciones/)

# 1. AWS API Gateway

## 1.1 ¿Que es?

Servicio que permite a los desarrolladores, crear, mantener y protejer API a cualquier escala

Servicio totalmente administrado que gestiona: 

    - Escalado
    - Control de Acceso
    - Monitoreo


API Gateway funciona con Amazon CloudFront. Le permite utilizar ubicaciones perimetrales, que proporcionan a los usuarios la latencia más baja para las solicitudes y respuestas de la API.

Una vez que se implementa la API, API Gateway le proporciona un panel para monitorear visualmente las llamadas a un servicio.

Las aplicaciones cliente utilizan el frontend para realizar solicitudes. 

Las partes de la implementación de la API que se comunican con los demás servicios de AWS se denominan backend

<details>
<summary>🗒 Tarjeta: APIs »</summary>

| Informacion   |
| ---- |
| Sin esto no hay EC2 |

</details>

### Funcionamiento

[Funcionamiento](../00_assets/Integracion%20de%20Aplicaciones/funcionamiento.png)

## API RESTFUL
Transferencia de estado representacional (REST):

    * Se compone de 6 principios de diseño (imagen)
    * Un diseño para aplicaciones basadas en la red de bajo acoplamiento
    * La comunicación es a través de HTTPExpone los recursos en determinadas direcciones URL
    * Varias API web son RESTful


### Componentes 

[Componentes](../00_assets/Integracion%20de%20Aplicaciones/componentes.png)


>[Event Bridge](./eventBridge.md)