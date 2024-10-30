![Amazon CloudFront](../../00_assets/Redes%20&%20Entrega%20de%20contenidos/cloudfront-logo.png)

[Redes & Entrega de Contenido](../../04-Redes_y_entrega_de_Contenido/)

# 1. AWS CloudFront

## 1.1 ¿Que es?

Entrega contenidos de forma segura con baja latencia y alta velocidad de transferencia
Los contenidos son entregados a traves de una red mundial de centros de datos denominados ubicaciondes de borde (Edge Locations)

Servicio web que acelera la distribución de contenido web estático y dinámico (como .html, .css, .js y archivos de imagen) a los usuarios

Características principales

    - Alto rendimiento
    - Baja latencia
    - Altas velocidades de transferencia de datos

Rentable

    - Pago por transferencia de datos y solicitudes para entregar contenido a los clientes
    - Sin pago inicial o compromisos mínimos

Los costos de CloudFront se calculan en función de la región geográfica, el número y el tipo de solicitudes y la cantidad de datos salientes que se transfieren.

<details>
<summary>🗒 Tarjeta: Ubicacion »</summary>

| Como funciona |
| ---- |
| Si el contenido a entregar ya se encuentra en la Edge Location con la latenica mas baja la entrega es inmediata |
| Si no se encuentra CDN lo recupera y lo manda - el precio varia segun region - |

</details> 

<br/>

> [Global Acelerator](./globalAcelerator.md)

<br/>