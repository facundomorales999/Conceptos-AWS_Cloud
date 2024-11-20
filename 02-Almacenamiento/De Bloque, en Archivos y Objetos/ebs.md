![Amazon Elastic Block Store](../../00_assets/Almacenamiento/ebs-logo.jpeg)

[Almacenamiento](../../02-Almacenamiento/)

# 1. AWS Elastic Block Store

## 1.1 ¿Que es?

Amazon EBS proporciona volúmenes de almacenamiento de bloques persistentes e replican automáticamente dentro de su zona de disponibilidad (AZ).

Cada volumen de EBS se replica automáticamente dentro de su AZ.

Con Amazon EBS, puede aumentar o reducir su uso en cuestión de minutos

Se puede realizar una copia de seguridad automática en Amazon S3.

Con EBS se puede crear y administrar los siguientes recursos de almacenamiento en bloque

Dentro de una instancia de EC2 pueden haber 2 EBS configuradas a su vez puede que ninguna instancia este referenciada a un ebs

### Volumenes:

* Se conectan a la EC2 y se usan como se usaria un disco local conectado a una pc.
* Es responsabilidad del cliente que esten respaldadas.

    
### Snapshot (Instantaneas): 

* Copias de seguridad de los volumenes
* Se pueden copiar entre AZ


## Funcionalidades

1. **EBS Snapshots Archive**

Da la posibilidad de mover las Snapshots a un nivel de archivo para que sea un 75% mas barado. 
Restaurarla demora entre 24~72 horas 

2. **Papelera de reciclaje para EBS Snapshots**

Da la posibilidad de borrar pero recuperar lo previamente, usualmente se usa para recuperar lo que se borra por error.
El tiempo maximo de retencion es de un año

3. **Restauracion rapida instantanea (FSR)**

Para no tener latencia en el primer uso de una inicializacion completa

### Encryptation

Cuando se crea un volumen encriptado se obtiene:

- Los datos ya encriptados
- Todos los datos en trancito instancia a volumen
- Todos las SnapShots se encriptan
- Todos los volumenens creados a partir de una instancia

<< Cuando se hace el cifrado se tiene poca latencia adicional tambien mejora la seguridad ua que obtiene llaves kms(aes-256)>>

### Pasos para encriptar

1. Crear EBS SnapShots
2. Encriptar las Snapshots
3. Crear un nuevo volumen a partir de ese (El volumen estara encriptado)
4. Adjuntar el volumen cifrado original


## Informacion suelta de algun test

* Amazon EBS is block-level storage used with Amazon EC2 instances, which is not suitable for static content
* Amazon EBS snapshots are a good way to back up point-in-time state of your data but they are not meant for long-term data archiving
* It does not support lifecycle policies and is not designed for global access.


### Volumenes e Iops
![Imagen](../../00_assets/Almacenamiento/volumenes-iops.png)
<br>

### Informacion almacenamiento
![imagen](../../00_assets/Almacenamiento/instantaneas.png)

<br/>

> [Elastic File Store](./efs.md)

<br/>