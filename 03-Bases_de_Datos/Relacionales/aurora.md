![Amazon Aurora](../../00_assets/Bases%20de%20Datos/aurora-logo.jpeg)

[Bases de Datos](../../03-Bases_de_Datos/)

# 1. AWS Aurora

## 1.1 ¿Que es?

Motor de BD Relacional de alto rendimiento / Disponibilidad completamente administrado compatible con mySQL y PostgreMySQL

Aurora está formada por clústeres

Aurora también automatiza y estandariza la replicación y la agrupación en clústeres de bases de datos que suelen estar entre los aspectos más difíciles de la configuración y administración de bases de datos

El almacenamiento crece automaticamente arrancas con 10GB y el maximo es 128TB 

* 15 RR max y el proceso de crearlas es mas rapido 


## High Availability y Read Replicas (RR)

6 copias de archivos a traves de 3 AZ

    * 4 / 6 copias por escribir
    * 3 / 6 copias por leer
    * Tiene como una auto curacion


## Cluster

Reader Endpoint - se conecta con todas las repicas RR asi cuando el cliente se conecta las hace a una de estas


## Replicas Auto Scalling 

Agrega o saca RR para para controlar los aumentos / caidas en base a la demanda moviendo el EndPoint para que se puedan acceder


## Custom Endpoint

Se puede elegir el Endpoint y Aurora lo equilibra


## Severless

Es una configuracion bajo demanda de Auto Scalling las instancias se escalan automaticamente y se prenden o apagan en funcion de su uso
**Solo se paga por invocacion**

### Casos de uso

    * Cargas de trabajo poco frecuentes intermitentes o impredecibles


## Global

### Cross Region RR 

- Util para DR
- Simple


### Global DB (Recomendada)

* 1 Region Primaria
* Max 5 Regiones Read Only (secundaria)
* 16 RR por region
* Baja latencia
* RTO < 1min


## Backup

| Automatico | Manual |
| :---: | :---: |
| 1 a 35 dias (no se pueden desactivar) | Cuando al usuario quiera |
| :---: | :---: |
| - | Estas Snapshots las puedo conservar todo el tiempo que quiera |


## RDS & AURORA Security

At Rest Encryption

- Master y RR usando KMS - se define cuando se lanza 
- Si Master no se encripta => RR no pueden

* In flight Encryption
* IAM Autentication : con roles
* Security Groups : Control Network acess
* No SSH disponible


<details>
<summary>🗒 Mejora del Rendimiento »</summary>

| En distintas BD |
| ---- |
| - **MySQL Estandar x5** - **Postgre x3** |

</details>


## Informacion suelta de algun test

* Amazon Aurora Serverless is an on-demand, auto-scaling configuration for Amazon Aurora, adjusting capacity based on the traffic, which makes it cost-effective and efficient.


<br/>

> [RDS](./rds.md)

<br/>