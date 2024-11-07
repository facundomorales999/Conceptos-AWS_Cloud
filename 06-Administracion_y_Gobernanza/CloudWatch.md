![Config](../6-Administracion_y_Gobernanza/CloudWatch.md)

![Amazon Cloud watch](../00_assets/Administracion%20y%20gobernanza/cloudTrail-icon.png)

[Administracion y gobernanza](../06-Administracion_y_Gobernanza/)

# 1. AWS CloudWatch

## 1.1 ¿Que es?

Monitorea el estado y uso de la mayoría de los recursos que se pueden administrar en AWS 
Conceptos clave

    - Métricas estándar / personalizadas
    - Monitor de gastos "(alertas de dinero)"
    - Alarmas
    - Notificaciones

El agente de CloudWatch recopila métricas a nivel del sistema:

    - Instancias EC2
    - Servidores locales

Le permite hacer lo siguiente: 

    - Realizar un seguimiento del rendimiento de las aplicaciones y de los recursos.
    - Recopilar y monitorear archivos de registro.
    - Recibir notificaciones cuando suene una alarma.


### CT Logs

| x | Info |
|:-----:|:-----:|
| ![logs](../00_assets/Administracion%20y%20gobernanza/cwLogs-logo.png) | Se usan para monitorear, almacenar y acceder a sus archivos de registro desde instancias de Amazon EC2, AWS CloudTrail, Route 53 y otras fuentes. |
|:----:| Le permite centralizar los registros de todos sus sistemas, aplicaciones y servicios de AWS que utiliza, en un único servicio altamente escalable. Luego, puede verlos fácilmente, buscar códigos de error o patrones específicos, filtrarlos en función de campos específicos o archivarlos de forma segura para su análisis futuro. |

### CT Alarms

| x | Info ALARMA DE FACTURACION |
|:-----:|:-----:|
| ![alarms](../00_assets/Administracion%20y%20gobernanza/cwAlarms-logo.png) | Se genera una alerta cuando las cargas estimadas superan un umbral específico |
|:----:| Se debe crear usando la Región us-east-1 // el cual es el almacenamiento central de todas las métricas de facturación |
|:----:| Se basa en métricas que incluyen cargos totales y específicos por servicio |
|:----:| Se envían notificaciones por email a través de un tema de Amazon SNS. |


## Informacion suelta de algun test

    * CloudTrail provides visibility into user activity by recording API calls made on your account. While it can help in detecting unwanted actions,
    * 

<br>

>[Config](./Config.md)