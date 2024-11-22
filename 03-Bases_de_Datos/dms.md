![Amazon Aurora](../00_assets/Bases%20de%20Datos/dms-logo.png)

[Bases de Datos](../../03-Bases_de_Datos/)

# 1. Relational Data Service

## 1.1 ¿Que es?

Migración de bd a la nube de manera rápida y segura.

La base de datos de origen funciona todo el tiempo durante la migración, lo que minimiza el tiempo de inactividad de las aplicaciones que dependen de la base de datos

Permite migrar sus datos desde y hacia las bases de datos comerciales y de código abierto más utilizadas. Al utilizar este servicio, puede migrar desde el servicio del sistema de administración de bases de datos (DBMS) a otro servicio de DBMS. 
Por ejemplo, puede migrar entre estas: 

–De Oracle a Oracle
–De Microsoft SQL Server a Amazon Aurora

Durante la migración, las aplicaciones pueden permanecer activas o en ejecución





### Data Schemal Tool SCT

AWS DMS y AWS SCT permiten migrar bases de datos homogéneas(origen y destino mismo tipo/compatibles) y heterogéneas desde centros de datos en las instalaciones e instancias en la nube a AWS. 
    
Mientras se reduce el tiempo de inactividad

La mayoría de las migraciones de bases de datos constan de dos pasos: convertir el esquema con AWS SCT y migrar los datos mediante AWS DMS
    
Conversiones compatibles con SCT
SCT convierte lo siguiente 
Esquema de BD de origen / Vistas / Procedimientos almacenados / Funciones

<br>
![SCT](../00_assets/Bases%20de%20Datos/SCT.png)