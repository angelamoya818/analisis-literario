# Milestones

Los milestones son productos que se irán entregando durante el desarrollo del proyecto. Cada uno representa un nivel de avance sobre el problema y debe proporcionar un producto mínimamente viable sobre el que poder continuar trabajando en el siguiente.

## Milestone 0: Modelo del problema

OBJETIVO:
Construir un programa que represente los conceptos necesarios para gestionar los contenedores, los pedidos y los viajes, teniendo en cuenta la información necesaria para conocer su situación y poder realizar posteriormente la asignación de contenedores.

QUÉ SE ENTREGA:
Una representación de los contenedores, incluyendo toda la información necesaria para trabajar con ellos:

-Identificador del contenedor: Identificador del contenedor. Permite distinguir un contenedor de cualquier otro de la flota y consultar toda la información asociada a él.

-Situación de vacío o cargado: Indica si el contenedor se encuentra actualmente vacío o cargado. Esto nos condiciona si puede utilizarse para un nuevo pedido.

-Mercancía que transporta o ha transportado: Indica qué mercancía transporta actualmente el contenedor. Es relevante para las restricciones relacionadas con las cargas anteriores. Por ejemplo, puede existir una regla que impida utilizar un contenedor para una determinada mercancía si entre sus últimas cargas ha transportado determinados productos, como látex o resina.

-Dirección y ciudad en la que se encuentra: Dirección en la que se encuentra actualmente el contenedor.

-Dirección y ciudad de destino cuando tiene un viaje asociado: Dirección de destino del viaje que tiene asociado el contenedor.

-Fecha de finalización del viaje: Fecha de descarga del contenedor.

-ADR: Indica si el contenedor dispone de ADR en vigor. Es necesario comprobarlo cuando un pedido requiere transportar mercancías para las que se exige ADR, es una normativa relacionada con el transporte de mercancías peligrosas por carretera.

-Aprobación CSC: información relativa a la aprobación/certificación CSC del contenedor. Permite comprobar si el contenedor cumple este requisito cuando el pedido lo exige. Es una certificación relacionada con la seguridad de los contenedores.

-Capacidad: Capacidad real del contenedor.

-Rompeolas: Indica si el contenedor dispone de rompeolas. El rompeolas es un elemento instalado dentro de una cisterna que sirve para reducir el movimiento del líquido durante el transporte.

-GOT: Indica si el contenedor dispone de GOT. GOT es una condición que  se consulta para saber si el contenedor es válido para determinadas operaciones.

-Restricciones relacionadas con las mercancías transportadas anteriormente, cuando sean necesarias para determinar si puede utilizarse para un pedido.

Una representación de los pedidos, incluyendo:

-Identificador del pedido: Identificador único del pedido.

-Tipo de servicio: ndica el tipo de servicio asociado al pedido. Por ejemplo, internacionales.

-Fecha de origen o carga: Fecha en la que el contenedor debe estar disponible para realizar la carga del pedido.

-Provincia de origen: Provincia donde se debe realizar la carga.

-Fecha de destino o descarga: Fecha prevista para la descarga del pedido.

-Provincia de destino: Provincia donde se debe realizar la descarga.

-Requisitos o características que deben cumplir los contenedores.

-Contenedor asignado (ESTO ES LO QUE NOSOTROS TENEMOS QUE ASIGNAR)

Una representación de los viajes, entendidos como pedidos que ya tienen un contenedor asociado, incluyendo la información necesaria para conocer la operación que está realizando el contenedor, su origen, destino y fechas. 

La relación entre los contenedores, los pedidos y los viajes, de forma que pueda conocerse qué contenedor está asociado a cada pedido y qué operaciones tiene pendientes.

La representación de la información diaria de los contenedores necesaria para poder conservar posteriormente su trazabilidad.

Documentación en docs/ donde se explique el modelo construido a partir de las historias de usuario y las decisiones tomadas para representar estos conceptos.

VALIDEZ:
El milestone se considera válido cuando el modelo permite representar la información necesaria de contenedores, pedidos y viajes para comenzar a implementar la lógica de planificación y trazabilidad en el siguiente milestone.

## Milestone 1: Lógica de planificación y trazabilidad

OBJETIVO:
Implementar la lógica necesaria para utilizar el modelo anterior y comenzar a resolver las necesidades de la responsable de logística.

QUÉ SE ENTREGA:
La lógica necesaria para consultar la información histórica de un contenedor y conocer dónde se encontraba, su situación, la mercancía que transportaba y el viaje que tenía asociado en una fecha determinada.

La lógica necesaria para determinar qué contenedores pueden utilizarse para un pedido futuro teniendo en cuenta:

-Dónde se necesitan.

-Cuándo se necesitan.

-Los viajes que ya tienen asignados.

-La fecha en la que terminan esos viajes.

-Las características necesarias para realizar el pedido.

-Las restricciones derivadas de las mercancías transportadas anteriormente.

La lógica necesaria para identificar qué pedidos pueden ser cubiertos con la flota disponible y cuáles quedan sin cubrir.

Una propuesta de asignación de contenedores a los pedidos, teniendo en cuenta los viajes ya existentes y la posibilidad de aprovechar la ubicación en la que finalizan para reducir desplazamientos innecesarios de contenedores vacíos.

La posibilidad de revisar la propuesta de asignación y modificar las asignaciones cuando la responsable de logística considere que una determinada decisión no es adecuada.

Tests automatizados que permitan comprobar el comportamiento de la lógica implementada.

VALIDEZ:
El milestone se considera válido cuando, a partir de información de contenedores, pedidos y viajes, los tests automatizados comprueban que el sistema puede:

1. Consultar la trazabilidad de los contenedores.

2. Determinar qué contenedores pueden utilizarse para un pedido.

3. Detectar los pedidos que no pueden cubrirse.

4. Proponer asignaciones teniendo en cuenta los viajes existentes y las condiciones de los pedidos.

5. Permitir modificar las asignaciones propuestas.