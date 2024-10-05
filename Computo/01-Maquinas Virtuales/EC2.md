![Amazon EC2 Auto Scalling](../../assets/Computo/EC2-logo.jpeg)

[Computo](../../Computo/)

# 1. AWS Elastic Compute Cloud

## 1.1 que es

Servicio que ofrece una capacidad informatica segura y tamaño variable en la nube
    -> Permite escalado vertical para satisfacer recursos
    ->Se puede utilizar para ejecutar una BD administrada por el cliente

## Informacion suelta de algun test

    -

# 4 Tipos

## 1- Instancias Bajo Demanda

Se ejecuta solo cuando es necesario, pero permanece activa durante la duración del proceso.
Se paga por la capacidad de computo por hora o por segundo segun las instancias que se ejecutan 
no se requiere paso por adelantado ni compromiso a largo plazo
se recomienda para
    usuarios que quieran bajo coste y flexibilidad sin compromisos 
    app con caras de trabajo a corto plazo con picos de actividad impredecibles que no se pueden interrumpir

<details>
<summary>🗒 Tarjeta: Palabras Claves »</summary>

| Instancias Bajo Demanda |
| ---- |
| Es ideal para aplicaciones con cargas de trabajo impredecibles o en pruebas y desarrollo. |

</details>

<br/>

## 2- Instancias Spot

Permiten aprovechar la capacidad de computo no utilizada a precios reducidos 90%, Sin embargo te la pueden sacar con un tiempo de anticipacion no mayor a los 2min o asi
Se recomienda para:
    -> Aplicaciones con horarios flexible (inicio/fin)
    -> Aplicaciones que son factibles a precios bajos
    -> Usuarios con necesidades informaticas

<details>
<summary>🗒 Tarjeta: Palabras Claves »</summary>

| Instancias SPOT |
| ---- |
| interrumpible - barata  |

</details>

<br/>

## 3- Instancias Reservadas

Permiten reservar capacidad de computo por 1 o 3 años con descuento significativo ~ 72% 
Se ofrecen en tres opciones de pago: 
    - All Upfront (todo por adelantado) `la mas clave`
    - Partial Upfront (parcialmente por adelantado) 
    - No Upfront (sin pago inicial).


`Reservadas convertibles` son mas caras que las `Estandars`

<details>
<summary>🗒 Tarjeta: Palabras Claves »</summary>

| Instancias Reservadas |
| ---- |
| largo tiempo  |

</details>

## 3- Instancias Dedicadas 

Estan fisicamente aisladas en el nivel de host de HW lo que significa que tus intancias 

<details>
<summary>🗒 Tarjeta: Palabras Claves »</summary>

| Instancias Dedicadas |
| ---- |
| Estas son como alquilar un cuarto en un hotel es tuyo y vos ahi haces lo que quieras |

</details>

## 3- Host Dedicados

Servidor fisico completamente dedicado para su uso con control total sobre la colocacion de instancias y visibilidad del hardWare subyacente.
Un usuario debe cumplir con los requisitos de licencia de SofrWare y cumplimiento que establecen que una carga de trabajo tiene que alojarse en un servidor fisico
Tiene compromiso de 1 o 3 años



<br/>
<details>
<summary>🗒 Tarjeta: Palabras Claves »</summary>

| Host Dedicados |
| ---- |
| fisico - aislada a nivel de nucleo |

</details>
<br/>
<details>
<summary>🗒 Tarjeta: Palabras Claves »</summary>

| Host Dedicados |
| ---- |
| Es como alquilar una casa, todo para vos |

</details>




<details>
<summary>🗒 Tarjeta: Modelo de Servicio »</summary>

| Pertenece a:  |
| ---- |
| IaaS |

</details>


<br/>

> [batch](./lightsail.md)

<br/>