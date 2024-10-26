![Amazon Cloud Watch](../00_assets/Administracion%20y%20gobernanza/cloudwatch-icon.png)

[Administracion y gobernanza](../6-Administracion_y_Gobernanza/)

# 1. CloudWatch

## 1.1 ¿Que es?

Servicio encargado de revisar el historial de los usuarios mediante auditorias tomando en cuenta 7 parámetros realizando el ciclo cada 7 dias 

Registra, monitorea de manera continua y retiene la actividad de la cuenta que se relaciona con las acciones en toda su infraestructura de AWS.

Registra :
    
    - Llamadas de la interfaz de programa de aplicaciones (API) para la mayoría de los servicios de AWS.
    - También se registra la actividad de AWS Management Console y AWS CLI


**La informacion se guarda en s3 de manera automatica una vez configurado.**

Parametros 

    1. Quién realizó la solicitud.
    2. Fecha y hora de la solicitud.
    3. Dirección de protocolo de Internet IP de origen.
    4. Cómo se realizó la solicitud.
    5. Acción realizada.
    6. Región en la que se realizó la acción.
    7. Respuesta.



![Config](../6-Administracion_y_Gobernanza/Config.md)