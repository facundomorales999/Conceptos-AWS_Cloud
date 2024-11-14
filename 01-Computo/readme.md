# Grupos de Seguridad

Son Firewall en las Instancias.
Una instancia puede permanecer a varios Security Group y a la vez estos se pueden referenciar.

Se utiliza para permitir el tráfico hacia o desde una interfaz de red elástica.
Se configura de forma predeterminada para:
    - Denegar todo el tráfico entrante
    - Permitir todo el tráfico saliente

***Con estado:*** si las reglas permiten que el tráfico fluya en una dirección, las respuestas pueden fluir automáticamente en la dirección opuesta.

Normalmente administrado por desarrolladores de aplicaciones


Regulan :

    * El acceso a los puertos

Puertos

| Numero | Codigo | Explicación |
| :---: | :---: | :---: |
| 22 | SSH (Security Shell) | Log into Linux |
| :---: | :---: | :---: |
| 21 | FTP (File Transfer Protocol) | Subir Archivos |
| :---: | :---: | :---: |
| 22 | SFTP (Simple File Transfer Protocol) | Subir Archivos con SSH |
| :---: | :---: | :---: |
| 80 | HTTP | Acceder a sitios desprotejido |
| :---: | :---: | :---: |
| 443 | HTTPS | Acceder a sitios protejido |
| :---: | :---: | :---: |
| 3389 | RDP | Log into Windows |

## Elastic Network Interfaces (ENI)

Representan una tarjeta virtual la cual le da acceso a la EC2 a la red pero no se usan en las EC2.
Son propias de la AZ en la que fueron creadas (no se pueden mover )

Atributos:
 
- Una dirección IPv4 privada principal del rango de direcciones IPv4 de su subred
- Una dirección IPv6 principal del rango de direcciones IPv6 de su subred
- Direcciones IPv4 privadas secundarias del rango de direcciones IPv4 de su subred
- Una dirección IP elástica (IPv4) para cada dirección IPv4 privada
- Una dirección IPv4 pública
- Direcciones IPv6 secundarias
- Grupos de seguridad
- Una dirección MAC
- Una bandera de verificación de origen/destino
- Una descripción

## EC2 Hibernadas

La RAM se conserva pq el SO no se detiene sin no que se guarda en un volumen raiz de [EBS](../02-Almacenamiento/De%20Bloque,%20en%20Archivos%20y%20Objetos/ebs.md)
El tiempo max de hibernacion es de 60 dias