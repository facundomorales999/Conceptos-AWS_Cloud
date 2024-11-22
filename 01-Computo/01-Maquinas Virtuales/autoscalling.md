![Amazon EC2 Auto Scalling](../../00_assets/Computo/EC2AutoScalling-Logo.jpeg)

[Computo](../../01-Computo/)

# 1. AWS Auto Scalling

## 1.1 ¿Que es?

Permite mantener mantener la disponibilidad de las aplicaciones y permite añadir o eliminar automáticamente instancias (escalar) según condiciones definidas.

Tiene tres partes: 

1. Plantilla de lanzamiento
2. Grupo de Auto Scaling
3. Políticas de escalado

El escalado puede basarse en: 

* El estado de la instancia 
* Las alarmas de Amazon CloudWatch 
* El cronograma de duración o el uso anterior (predicción)


<details>
<summary>🗒 Tarjeta: Escalado Vertical »</summary>

| Tipos de escalado |
| ---- |
| Permite agregar mas servidores cuando se requiera, mejorando el rendimiento de manera global. |

</details> 

<details>
<summary>🗒 Tarjeta: Escalado Horizontal »</summary>

| Programa Orientado a Objetos |
| ---- |
| A diferencia del horizontal aca se potencia una maquina nomas. |

</details>

## Caracteristicas

###     -> Monitoreo
    como si fuera un hospital

###     -> Controles de salud personalizados
    como tener remedios en casa

###     -> Equilibrio de capacidad entre zonas de disponibilidad
    ir a otro super para ver si hay lo que busco

###     -> Múltiples tipos de instancias y opciones de compra
    ir a al barrio de los judios

###     -> Reemplazo automático de instancias Spot
    a todo el mundo le gustan las ofertas

###     -> Equilibrio de carga
    mira que aca todos se quieren aparece corrrelacion con [Elastic Load Balancer](../05-Administrador%20de%20Costos%20y%20Capacidades/elb.md)

###     -> Escalabilidad
    cuando hay drop todos van a comprar pero cuando no nadie va 

###     -> Actualización de instancia

## Politicas 

### 1. Dinamico

* Escalado de seguimiento de objetivos
    - Facil de configurar
* Simple / Escalado
    - Este va que definas alarmas de [Cloudwatch](../../06-Administracion_y_Gobernanza/CloudWatch.md) y cuando superen un umbral haga el escalado.

### 2. Programado

* Basado en patrones conocidos
* Dentro de un horario

### 3. Predective

* En base al historial aumenta segun rachas

## Metricas para escalar

1. CPU utilizada
2. Request per target
3. Aplicacion vinculada de entada o salida
4. Lo que te pinte

Despues de escalar se tienen que esperar 300 segundos de enfriamiento para regular el sistema, durante ese tiempo asg no hace nada con las instancias



<br/>

> [Batch](./batch.md)

<br/>