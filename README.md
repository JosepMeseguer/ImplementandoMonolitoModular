# Descripción

## Desarrollo paso a paso del projecto. 

Comenzamos con una base mínima, tomamos como ejemplo del desarrollo una empresa de transporte de paqueteria. Las funcionalidades básicas de gestión de recogida, transporte y entrega de paquetes de nuestros clientes serán las primeras a implementar. Pero el proyecto tiene un largo recorrido en cuanto añadamos capas como la de seguridad, servicios de auditoria, tracking de nuestros vehiculos en desplazamiento... 

La arquitectura basada en un Monolito Modular permite comenzar desde un negocio pequeño, pero preparado para ir creciendo progresivamente y dar paso bien microservicios por contextos bien diferenciados. Añadir complejidad solo donde sea estrictamente necesario.

El primer paso es conocer el negocio y los datos precisos para gestionarlo. A partir de un buen diseño de los agrupamientos y validaciones precisas para los datos se determina:

+ Qué datos son simples invariantes que pueden ser implementados como value objects
+ Qué agrupaciones de datos pueden ser implementadas como entidades
+ Cuándo lo que tiene sentido lógico en el movimiento de la información es trabajar con DTO's

Como en todo contexto real se trabaja con grises, en ocasiones podremos aplicar herencia o composición para construir value objects más complejos, subentidades dependientes de otras, DTO's validados o pendientes de usar.

A partir de un buen diseño de las estructura de datos se organizan las capas y las agrupaciones paralelas por contextos. Se define la arquitectura más idónea a las necesidades, un Monolito Modular suele ser la mejor opción, permite un lógico reparto de gestión de contextos entre los equipos y hace más sencillo pasar del monolito a una arquitectura de microservicios para los contextos que lo precisen.

Añadir capas de servicio, persistencia, presentación, seguridad o auditoria son los siguientes pasos.

