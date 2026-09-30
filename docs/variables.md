# Variables del problema

En este documento se describen las variables necesarias para representar la información utilizada en el problema de planificación y trazabilidad de contenedores, pedidos y viajes. Se incluyen únicamente las variables necesarias para representar los conceptos definidos en las historias de usuario y los milestones del proyecto.

## Contenedores

### Identificador del contenedor
Identificador único que permite distinguir un contenedor de cualquier otro de la flota y consultar toda la información asociada a él.

### Situación de vacío o cargado
Indica si el contenedor se encuentra actualmente vacío o cargado. Esta información condiciona si puede utilizarse para atender un nuevo pedido.

### Mercancía que transporta o ha transportado
Indica qué mercancía transporta actualmente el contenedor o qué mercancía ha transportado. Es relevante para comprobar las restricciones relacionadas con las cargas anteriores.

### Dirección y ciudad en la que se encuentra
Indica la ubicación actual del contenedor mediante la dirección y la ciudad en la que se encuentra.

### Dirección y ciudad de destino cuando tiene un viaje asociado
Indica la dirección y la ciudad de destino del viaje que tiene asociado el contenedor.

### Fecha de finalización del viaje
Indica la fecha prevista de descarga del contenedor y, por tanto, la fecha en la que finaliza el viaje que tiene asociado.


### ADR
Indica si el contenedor dispone de ADR en vigor. El ADR está relacionado con los requisitos aplicables al transporte de mercancías peligrosas por carretera.

### Aprobación CSC
Información relativa a la aprobación o certificación CSC del contenedor. Permite comprobar si el contenedor cumple este requisito cuando el pedido exige que disponga de esta certificación relacionada con la seguridad de los contenedores.

### Capacidad
Indica la capacidad real del contenedor.

### Rompeolas
Indica si el contenedor dispone de rompeolas. El rompeolas es un elemento instalado dentro de una cisterna que sirve para reducir el movimiento del líquido durante el transporte.

### GOT
Indica si el contenedor dispone de GOT. Esta condición se consulta para determinar si el contenedor es válido para determinadas operaciones.

### Restricciones relacionadas con las mercancías transportadas anteriormente
Representa las restricciones que pueden derivarse de las mercancías que el contenedor ha transportado anteriormente. Estas restricciones se utilizan cuando es necesario determinar si el contenedor puede utilizarse para un determinado pedido.


## Pedidos

### Identificador del pedido
Identificador único que permite distinguir un pedido de cualquier otro.

### Tipo de servicio
Indica el tipo de servicio asociado al pedido, por ejemplo, servicios internacionales.

### Fecha de origen o carga
Indica la fecha en la que el contenedor debe estar disponible para realizar la carga correspondiente al pedido.

### Provincia de origen
Indica la provincia donde se debe realizar la carga del pedido.

### Fecha de destino o descarga
Indica la fecha prevista para la descarga del pedido.

### Provincia de destino
Indica la provincia donde se debe realizar la descarga del pedido.

### Requisitos o características que deben cumplir los contenedores
Representa las características que debe cumplir un contenedor para poder ser utilizado en el pedido. Estos requisitos permiten comprobar si un determinado contenedor es compatible con las necesidades del pedido.

### Contenedor asignado
Indica el contenedor que se ha asignado a un pedido.


## Viajes

### Información del viaje

Los viajes representan pedidos que ya tienen un contenedor asociado. La información del viaje permite conocer la operación que está realizando el contenedor, su origen, su destino y las fechas asociadas a dicha operación.


## Información diaria de los contenedores

### Información diaria
Representa la información de los contenedores correspondiente a cada día. Las exportaciones se obtienen diariamente, por lo que esta información permite conservar las diferentes situaciones por las que pasa cada contenedor y utilizar posteriormente esos datos para reconstruir su trazabilidad histórica.

