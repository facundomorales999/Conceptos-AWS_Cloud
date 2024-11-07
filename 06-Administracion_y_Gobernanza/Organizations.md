![Amazon Control Tower](../00_assets/Administracion%20y%20gobernanza/organizations-icon.png)

[Administracion y gobernanza](../06-Administracion_y_Gobernanza/)

# 1. AWS Organizations

## 1.1 ¿Que es?

**Infraestructura como codigo**


Servicio de gestion de cuentas que permite consolidar varias cuentas en una organizacion que cree y administre de forma centalizada 

**puede asignar recursos, agrupar cuentas y aplicar políticas de gobernanza a cuentas o grupos fácilmente dicho rústico de forma centralizada**

Permite crear cuentas nuevas de AWS sin costo adicional. 


Caracteristicas:

    - Implementacion de la facturacion consolidada
    - Hacer cumplir la gobernanza de las cuentas de AWS

Ayuda a restringir los servicios, recursos y acciones de API individuales a las que pueden acceder los usuarios y roles en cada cuenta miembro

Los componentes clave de una organización son:

    * Cuenta de administración (root)
    * Unidad organizativa (OU)
    * Cuenta de miembro
    * Política de control de servicios (SCP)


>[System Manager](./SystemManager.md)