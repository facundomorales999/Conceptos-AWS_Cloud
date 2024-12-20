![Amazon Global Aceletator](../../00_assets/Redes%20&%20Entrega%20de%20contenidos/route53-logo.png)

[Redes & Entrega de Contenido](../../04-Redes_y_entrega_de_Contenido/)

# 1. Route 53

## 1.1 ¿Que es?

Gestor de dominios (DNS) e IP`s gestión de trafico en la nube escalable y de alta disponibilidad

Funcionalidades:
    
- Se puede utilizar para proporcionar un nombre de dominio personalizado para un sitio web estático alojado en Amazon S3
- direccionamiento del trafico de red
- Comprobacion del estado de los recursos (salud del dns)

El direccionamiento basado en la latencia (LBR) le permite utilizar DNS para redirigir las solicitudes a la región de AWS que dará a los usuarios el tiempo de respuesta más rápido.

Altamente disponible, escalable y completamente administrado donde el cliente tiene control total sobre el DNS (Se puede registrar)

Registros :

* Como el cliente enruta el trafico 
* Contienen 
    * Dominio / Subdomino Name
    * Record Type
    * Valor
    * Politica de enrutado
    * TTL - Time to live

## Record Type

A       - Mapear un HOSTNAME IPV4
AAAA    - Mapear un HOSTNAME IPV6
CName   - Mapear im HOSTNAME en otro
NS      - Nombrar servidores en Hosted Zones

## Hosted Zones

Definen como enrutar el trafico a un dominio y subdominio
Crear una cuesta $0,50 por mes cada una

2 Tipos

1. Public HZ 
    
    * Contienen registros que especifican como enrutar trafico en la internet

2. Private HZ

    * Contienen registros que especifican como enrutar trafico dentro de 2 o + VPC

## Time to Live (TTL)

Determina cuanto tiempo se debe almacenar en cache una consulta con el proposito de no consultar todo el tiempo

| Alto TTL | Bajo TTL |
| :--: | :--: |
| Menos Trafico | Mayor trafico => $$ |
| :--: | :--: |
| Posibles registros obsoletos | Registros obsoletos por menos tiempo |
| :--: | :--: |
| _ | Facil de Cambiar |

## CNAME vs ALIAS

AWS resourses exponen el HOSTNAME y lo que deseo que aparezca un HOST mio

2 opciones :

* CNAME : 

    * Permite apuntar un HOSTNAME a cualquier otro 
    * Solo funciona si el nombre no es raiz

* ALIAS : 

    * Permite apuntar un HOSTNAME a otro recurso de AWS
    * Solo funciona si el nombre no es raiz
    * Libre de cargo

## Politicas

Cuando crea un registro, elige una política de enrutamiento, que determina cómo responde Amazon Route 53 a las consultas DNS. Las políticas de enrutamiento disponibles son:

### Simple Routing

Se utiliza cuando sólo necesita un único registro en su DNS con una o más direcciones IP detrás del registro en caso de que desee equilibrar la carga. Si especifica múltiples valores en una política de Enrutamiento Simple, Route53 devuelve una IP aleatoria de entre las opciones disponibles.

### Weighted Routing 

Se **utiliza cuando se desea dividir el tráfico en función de pesos asignados**. Por ejemplo, si desea que el 80% de su tráfico vaya a una AZ y el resto a otra, utilice el Enrutamiento ponderado. Esta política es muy útil para probar cambios de características y, debido a las características de división del tráfico, puede servir también para realizar despliegues «azul-verde». Al crear el Enrutamiento ponderado, debe especificar un nuevo registro para cada dirección IP. No se pueden agrupar varias IPs en un solo registro, como ocurre con el Enrutamiento Simple.


### Latency Based Routing

El enrutamiento basado en la latencia, como su nombre indica, **se basa en configurar el enrutamiento en función de cuál sería la latencia más baja para un usuario determinado**. Para utilizar el enrutamiento basado en la latencia, debe crear un conjunto de registros de recursos de latencia en la misma región que el recurso EC2 o ELB correspondiente que recibe el tráfico. Cuando Route53 recibe una consulta para su sitio, selecciona el conjunto de registros que proporciona al usuario la velocidad más rápida. Al crear el enrutamiento basado en la latencia, debe especificar un nuevo registro para cada IP.


### Failover Routing

El enrutamiento de conmutación por error se utiliza **cuando se desea configurar una conmutación por error activo-pasivo**. Route53 monitorizará la salud de su primario para que pueda conmutar por error cuando sea necesario. También puede configurar manualmente los controles de salud para supervisar todos los puntos finales si desea reglas más detalladas.


### Geolocation Routing

**Permite elegir dónde se enviará el tráfico en función de la ubicación geográfica de sus usuarios.**


### Geo-proximity Routing


Le **permite elegir dónde se enviará el tráfico en función de la ubicación geográfica de sus usuarios y sus recursos.** Puede elegir enrutar más o menos tráfico basándose en un peso específico que se denomina sesgo. Este sesgo amplía o reduce la disponibilidad de una región geográfica, lo que facilita el desplazamiento del tráfico de los recursos de una ubicación a los de otra. Para utilizar este método de enrutamiento, debe habilitar el flujo de tráfico Route53. Si desea controlar el tráfico global, utilice el enrutamiento por geoproximidad. Si desea que el tráfico permanezca en una región local, utilice el enrutamiento por geolocalización.


### Multivalue Routing

Es más o menos lo mismo que Simple Routing, pero Multivalue Routing **le permite poner controles de salud en cada conjunto de registros.** Esto asegura entonces que sólo una IP saludable será devuelta aleatoriamente en lugar de cualquier IP.

Multivalue routing can do random load balancing according to the AWS website: To route traffic approximately randomly to multiple resources, such as web servers, you create one multivalue answer record for each resource and, optionally, associate a Route 53 health check with each record. 

## Health Checks

-> Estan integrados con [Cloudwatch](../../06-Administracion_y_Gobernanza/CloudWatch.md)

Si una region se cae no permite que se envien instancias ahi en otras palabras monitorea endpoints
por lo menos 15 Health cheakers veran la salud de los endpoints

* Se puede definir un umbral para ver sanidad
* Soporta protocolo HTTP / HTTPS y TCP