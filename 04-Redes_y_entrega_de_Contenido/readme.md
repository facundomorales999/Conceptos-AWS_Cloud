[Redes & Entrega de Contenido](../../04-Redes_y_entrega_de_Contenido/)

# 1. REDES

## Seguridad para la red

### Red Publica y Privada

**IPV4 -> la mas comun**
**IPV4 -> es mas nueva y suele ir con IOT**

Public IP:

* Cualquier dispositivo en la red se puede conectar
* IP es unica 
* Se puede Localizar

Private IP:

* Solo dispositivos privados se pueden conectar
* IP es unica pero en la red privada pero fuera de ella se puede repetir
* Nat + Internet Gateway(Proxy) para conectarte

Elastic IP:

* Si yo detengo una EC2 la IP cambia
* Es una IP publica que te pertenece si no la borras
* Propias de mi cuenta puedo tener 5 de estas como maximo
* Usarlas es considerado una mala practica

### Proteja la red mediante un diseño en capas. 
    
* Una red de capas puede aprovechar las siguientes ventajas:

    - Tablas de enrutamiento para controlar el flujo de tráfico
    - Listas de controles de acceso a la red(NACL) para controlar el tráfico hacia y desde las redes
    - Grupos de seguridad(SG) para controlar el tráfico hacia anfitriones y servicios
    - Acceso seguro para administración mediante
    - Anfitriones de Bastión para acceder a anfitriones basados en Linux
    - Host bastión para escritorio remoto (RDP) para Windows

Al solucionar problemas:

- Verifique que el recurso esté disponible
- Compruebe si hay NACL o SGS bloqueantes
- Compruebe que el enrutamiento sea correcto para el host o el servicio

## Protocolos de internet IP

    Establece las reglas para transmitir y enlutar los datos en internet

## Direcciones IP: 
    
    Para identificar de manera única un único dispositivo en una red

## Subredes IP:

Rango ip en una vpc / particiones lógicas de una red física en subredes mas chicas
Ventajas : 

    - Mayor Velocidad, 
    - Mayor seguridad y menor trafico de red 

## Protocolos

![Protocolos](../00_assets/Redes%20&%20Entrega%20de%20contenidos/Protocolos.png)

## Solucion de problemas

### Conexion de las Instncias

![1](../00_assets/Redes%20&%20Entrega%20de%20contenidos/Problema1.png)

### Conexion SSH

![1](../00_assets/Redes%20&%20Entrega%20de%20contenidos/Problema2.png)

### 3

![1](../00_assets/Redes%20&%20Entrega%20de%20contenidos/Problema3.png)

### Interconexion VPC

![1](../00_assets/Redes%20&%20Entrega%20de%20contenidos/Problema4.png)

<br>
[Informacion extraida de:](https://aws.amazon.com/es/products/networking/)
<br/>

# Modelo de interconexion de sistemas abiertos OSI

OSI define un modelo estandar para que distintos equipos puedan compartir informacion a traves de una red
