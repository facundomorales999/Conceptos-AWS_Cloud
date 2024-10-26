[Bases de Datos](../../3-Bases_de_Datos/)

# 1. Bases de Datos

## 1.1 ¿Que son?

Conjunto de datos que se organiza en archivos
Ventajas:

    - Construidas con un objetivo
    - Rendimiento a gran escala
    - Completamente administradas
    - Diseñadas para cargas de trabajo críticas para la empresa

![Orden](../00_assets/Bases%20de%20Datos/ordenamiento.png)

**Relacionales:** Los archivos almacenados tienen una conexion entre ellos

**No Relacionales:** Al principio no estan relacionados los archivos aunque a futuro estos se pueden relacionar


### Motores de BD
| Relacionales           | No Relacionales |
|------------------------|-----------------|
| MySQL                  | Mongo DB        |
| Postgre Sql (elefante) | Dynamo DB       |
| Maria DB               | AWS RedShift    |
| Aurora                 | Apache HBase    |
| Sql Server             | Aurora          | 

<br/>

## Bases y Caracteristicas

![Bases y Caracteristicas](../00_assets/Bases%20de%20Datos/distintas%20bd.png)


## Servicios Administrados y no

Servicios Administrados:

    * Los servicios administrados solo requieren que el usuario los configure. El escalado, la tolerancia a errores y la disponibilidad suelen estar integrados en el servicio
    * Responsabilidades:
        - Optimizacion de aplicaciones 

Servicios No Administrados

    * En general, usted aprovisiona servicios no administrados. Gestiona el escalado, la tolerancia a errores y la disponibilidad
    * Responsabilidades: 

        - Instalación y parches del SO
        - Instalación y parches del SW de la BD
        - Copias de seguridad de la BD
        - Alta disponibilidad
        - Escalado
        - Suministro de energía, bastidores y pilas
        - Mantenimiento del Servidores

![Bases en](../00_assets/Bases%20de%20Datos/bd_en.png)

## Casos de uso

![Casos de uso](../00_assets/Bases%20de%20Datos/casos%20de%20uso.png)

## Recomendaciones 

![Recomendaciones](../00_assets/Bases%20de%20Datos/Recomendaciones.png)

