![Amazon SNS](../00_assets/Integracion%20de%20Aplicaciones/stepFunctions-logo.png)

[Integracion de Aplicaciones](../9-Integracion_de_Aplicaciones/)

# 1. AWS Step Functions

## 1.1 ¿Que es?

Permite coordinar los servicios de AWS en flujos de trabajo sin servidor.

Los flujos de trabajo consisten en una serie de pasos.

El resultado de un paso es la entrada al siguiente paso.

Beneficios clave:

    - Crear y actualizar aplicaciones distribuidas.
    - Escribir menos código

Los **flujos de trabajo** consisten en una serie de pasos y transiciones entre cada paso, lo que también se conoce como máquina de estados

[flujo](../00_assets/Integracion%20de%20Aplicaciones/flujos.png)

## CICLO DE VIDA

    * Definir
        - En json
    * Virtualizar
        - a Visualizar en la consola de Step Functions
    * Monitorear
        - Cada ejecución

[pasos](../00_assets/Integracion%20de%20Aplicaciones/pasos.png)