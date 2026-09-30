# Planificación temporal y trazabilidad histórica de contenedores cisterna

## Procedencia del problema
Depot Container Services, perteneciente a Euconsa y situada en Guadarranque, San Roque, desarrolla actividades relacionadas con la gestión y transporte de contenedores y cisternas utilizados para el transporte de mercancías líquidas a granel por carretera y ferrocarril. Transportan productos químicos como aceites lubricantes, disolventes, aditivos y jabones.
El área de logística gestiona una flota de 800 contenedores y cisternas. La gestión de estos contenedores requiere conocer en todo momento el estado de cada uno y tener en cuenta tanto sus características como las operaciones que tiene pendientes. 
Cada contenedor tiene unas características que condicionan las operaciones para las que puede utilizarse. Entre ellas su capacidad, su tamaño, que puede ser de 20, 25 o 30 pies en este depot y diferentes características técnicas, como si permite calentar el producto, si dispone de aislamiento, rompeolas u otros equipamientos. También es necesario conocer si el contenedor tiene al día las inspecciones periódicas como el CSC (inspección/certificación periódica exigida para determinados contenedores) o ADR (requisitos y documentación relacionados con el transporte de mercancías peligrosas por carretera).
El problema surge en la planificación diaria de la flota. La información disponible sobre los contenedores se obtiene diariamente y permite conocer la situación pero no planificar con antelación los próximos pedidos. Esto dificulta saber si en una fecha determinada habrá suficientes contenedores disponibles con las características necesarias y el lugar donde se necesitan. Por ejemplo, me hacen un pedido que tengo que cargar el día 8 de Octubre 10 contenedores en la zona de Barcelona y como solo sé dónde están los contenedores a día de hoy no puedo planificar para ver si para ese día tengo esos 10 contenedores allí, los tengo que posicionar, o por mi flota no me conviene hacer ese pedido.

## Desarrollo del problema
La información disponible permite conocer diariamente dónde se encuentra cada contenedor, su estado y la operación que tiene asociada. Sin embargo, cuando se necesita consultar la situación de un período anterior, resulta necesario conocer las diferentes situaciones por las que ha pasado cada contenedor durante ese período. Esta información es relevante para la responsable de logística, que necesita conocer dónde se encontraba cada contenedor durante la última semana o el último mes y cuál era su situación en cada momento, por ejemplo, si estaba vacío, cargado, limpio o sucio. Además, los contenedores pueden tener viajes ya asignados. En los datos disponibles, el identificador de viaje permite identificar el viaje asociado a cada contenedor y la fecha de fin corresponde a la descarga del contenedor. Una vez realizada dicha descarga, el contenedor vuelve a estar disponible. Por tanto, la situación actual de un contenedor no es suficiente para conocer su disponibilidad en una fecha posterior. Para ello hay que tener en cuenta que algunos contenedores están asociados a viajes que todavía no han finalizado y que cada contenedor tiene unas características determinadas. Esta situación dificulta la planificación de los contenedores cuando se necesita conocer qué contenedores estarán disponibles en los próximos días y cuál será su situación en ese momento. También dificulta reconstruir la evolución de un contenedor cuando se necesita consultar dónde estaba o qué estado tenía durante un período anterior, ya que no se nos da esta información solo donde está el día de hoy.

## Datos y aproximación del problema
Para estudiar el problema se dispone de exportaciones procedentes del sistema utilizado en la gestión logística de la empresa. Los datos necesarios han sido aportados por la responsable de logística para su uso académico, eliminando la información identificativa de los clientes.
La información disponible incluye datos sobre los contenedores, sus viajes y sus características, así como información necesaria para representar los pedidos que deben ser atendidos.

Las variables necesarias para resolver el problema están descritas en:
- [Variables](docs/variables.md)

Los datos reales anonimizados no se incluyen en esta documentación. Se utilizarán posteriormente durante el desarrollo del proyecto cuando sean necesarios.

## Planificación del proyecto
El proyecto se ha dividido en diferentes etapas. Cada milestone define un producto mínimamente viable sobre el que se podrá continuar trabajando en la siguiente etapa.
La planificación se ha realizado a partir de los usuarios del proyecto, sus necesidades y los recorridos que realizan al utilizar la solución.

- [Personas](docs/personas.md)
- [Historias de usuario](docs/historias-de-usuario.md)
- [User journays](docs/user-journays.md)
- [Milestones](docs/milestones.md)

## Role-play
![Foto del role-play](docs/role-play/roleplay.jpeg)

## Configuración del repositorio 
- [Configuración del entorno](docs/configuracion/configuracion.md)
