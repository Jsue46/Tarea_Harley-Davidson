# Numeral 6 - Drivers de Restriccion, Drivers Funcionales y EAC

## Caracteristicas del Sistema

| ID | Descripcion |
|---|---|
| CAR-01 | **Compatibilidad e interoperabilidad empresarial.** La solucion debe integrarse con la arquitectura corporativa existente y con sistemas empresariales ya en funcionamiento. |
| CAR-02 | **Eficiencia operativa de compras y abastecimiento.** La solucion debe reducir complejidad operativa y responder con agilidad en procesos de requisicion, orden, recepcion y factura. |
| CAR-03 | **Seguridad y control de acceso.** La solucion debe proteger la informacion de compras y proveedores, diferenciando acceso interno y externo y auditando intentos no autorizados. |
| CAR-04 | **Disponibilidad operacional.** La solucion debe mantenerse disponible para no interrumpir procesos criticos de compras y abastecimiento. |
| CAR-05 | **Modificabilidad y mantenibilidad.** La solucion debe facilitar cambios evolutivos, reducir costos de mantenimiento y evitar obsolescencia prematura. |
| CAR-06 | **Capacidad de uso.** La solucion debe ser facil de usar para personal interno y para proveedores externos con diferentes niveles de familiaridad. |
| CAR-07 | **Portabilidad y evolucion por fases.** La solucion debe poder migrarse o evolucionar por etapas sin reescribir la logica central del negocio. |
| CAR-08 | **Trazabilidad y auditoria.** La solucion debe consolidar datos, soportar seguimiento de resultados y dejar rastro de operaciones y decisiones. |

## CDU EXPANDIDOS. Requisitos / Drivers Funcionales

| ID | Descripcion | Caracteristica asociada |
|---|---|---|
| CU-01 | Permite **evaluar y seleccionar proveedores** de acuerdo con criterios estrategicos definidos por Compras. | CAR-01 y CAR-08 |
| CU-02 | Permite **desarrollar relaciones con proveedores** estrategicos para sostener colaboracion de largo plazo. | CAR-01 y CAR-06 |
| CU-03 | Permite **gestionar el rendimiento de proveedores** considerando calidad, costes y plazos. | CAR-02 y CAR-08 |
| CU-04 | Permite **integrar proveedores en desarrollo de producto** y coordinar su participacion en actividades clave. | CAR-01 y CAR-07 |
| CU-05 | Permite **procesar requisiciones de compra** incluyendo requerimientos y plazos. | CAR-02 y CAR-06 |
| CU-06 | Permite **emitir ordenes de compra** a partir de requisiciones procesadas. | CAR-02 y CAR-08 |
| CU-07 | Permite **gestionar la recepcion de materiales** y el seguimiento de entregas. | CAR-02 y CAR-04 |
| CU-08 | Permite **procesar facturas de proveedores** vinculadas al flujo de compra. | CAR-03 y CAR-08 |
| CU-09 | Permite **gestionar resultados de suministradores** para seguimiento y toma de decisiones. | CAR-01 y CAR-08 |
| CU-10 | Permite **gestionar la integracion con suministradores** para intercambio de informacion con el ecosistema empresarial. | CAR-01 y CAR-03 |
| CU-11 | Permite **gestionar contactos de suministradores** necesarios para relacion y coordinacion operativa. | CAR-01 y CAR-06 |

## Drivers de Restriccion

| Tipo de restriccion | Descripcion |
|---|---|
| Del negocio / cliente | La solucion debe apoyar los objetivos de **calidad, costes y plazos (QCT)** y mejorar la coordinacion de abastecimiento en toda la empresa. |
| De la organizacion | La solucion debe ser **compatible con la arquitectura de sistemas de informacion existente** y con las iniciativas de TI ya en marcha en Harley-Davidson. |
| Tecnologica | La solucion debe ofrecer **funcionalidad Internet inmediata**, integracion con sistemas corporativos y **portabilidad de plataforma**. |
| Operativa | La solucion debe soportar usuarios internos y externos; aunque Compras ronda las 200 personas, mas de **2,000 empleados generan solicitudes** de compra. |
| De evolucion | La solucion debe poder implementarse y evolucionar por fases, reduciendo complejidad y costos de mantenimiento / obsolescencia. |

## CDU EXPANDIDOS. Requisitos / Drivers de Atributos de Calidad

| ID | Categoria | Escenario | Prioridad |
|---|---|---|---|
| EAC-01 | Desempeno | **Fuente del estimulo:** usuario interno. **Estimulo:** registra una requisicion o consulta informacion de abastecimiento. **Artefacto:** portal interno y modulo de Compras y Abastecimiento. **Entorno:** operacion normal. **Respuesta:** el sistema procesa y confirma la operacion con agilidad para no afectar la operacion diaria. **Medida:** cumplimiento operativo de los procesos de requisicion, pedido, recepcion y factura. | Alta |
| EAC-02 | Disponibilidad | **Fuente del estimulo:** falla de infraestructura. **Estimulo:** el servidor web o aplicativo deja de responder en horario laboral. **Artefacto:** plataforma SiL'K desplegada. **Entorno:** operacion normal. **Respuesta:** el servicio se restablece sin comprometer la continuidad del proceso de compras. **Medida:** continuidad operativa del proceso de compras y abastecimiento. | Alta |
| EAC-03 | Seguridad | **Fuente del estimulo:** proveedor externo o atacante. **Estimulo:** intenta acceder a informacion no autorizada o interceptar la comunicacion. **Artefacto:** portal de proveedores e identidad. **Entorno:** acceso por Internet. **Respuesta:** el sistema autentica, autoriza, cifra y registra el intento. **Medida:** 100% de trafico cifrado y 100% de intentos no autorizados auditados. | Alta |
| EAC-04 | Compatibilidad / interoperabilidad | **Fuente del estimulo:** sistema corporativo externo. **Estimulo:** intercambio de datos con sistemas empresariales existentes (incluyendo ERP cuando aplique). **Artefacto:** integraciones de la solucion. **Entorno:** operacion normal o sincronizacion programada. **Respuesta:** procesa datos validos, gestiona errores y mantiene trazabilidad del intercambio. **Medida:** compatibilidad con la arquitectura existente y con iniciativas TI en marcha. | Alta |
| EAC-05 | Modificabilidad | **Fuente del estimulo:** equipo del proyecto. **Estimulo:** ajuste de reglas o procesos durante la evolucion por fases. **Artefacto:** procesos y configuracion funcional. **Entorno:** mejora continua. **Respuesta:** el cambio se incorpora preservando el ambito delimitado del proyecto. **Medida:** evolucion por fases con control de complejidad y mantenimiento. | Alta |
| EAC-06 | Usabilidad | **Fuente del estimulo:** usuarios internos y proveedores. **Estimulo:** uso de funcionalidades de compra y suministro durante la operacion normal. **Artefacto:** interfaz y flujo funcional de la solucion. **Entorno:** operacion normal. **Respuesta:** uso claro de funcionalidades y soporte al trabajo diario de las partes implicadas. **Medida:** facilidad de uso considerada en la evaluacion funcional y cualitativa. | Media-Alta |
| EAC-07 | Portabilidad | **Fuente del estimulo:** evaluacion de proveedores. **Estimulo:** comparar alternativas de software para sostenibilidad futura. **Artefacto:** plataforma propuesta por el proveedor. **Entorno:** proceso de seleccion. **Respuesta:** la solucion presenta capacidad de portabilidad de plataforma. **Medida:** criterio de portabilidad evaluado en la decision final. | Media |

## Modelo de calidad seleccionado

| Elemento | Decision |
|---|---|
| Enfoque de evaluacion funcional | Adecuacion de funcionalidades a la especificacion requerida. |
| Enfoque de evaluacion cualitativa | Calificacion de criterios como relaciones a largo plazo, gestion del cambio, compatibilidad de arquitecturas, portabilidad y funcionalidad Internet. |
| Decision de calidad para la propuesta | Combinar evaluacion cuantitativa + cualitativa para seleccionar la alternativa con mejor ajuste al contexto SiL'K. |

## Relacion de los EAC con la arquitectura propuesta

| EAC | Decision arquitectonica reforzada |
|---|---|
| EAC-01 | Separacion entre clientes web, servidor web, servidor aplicativo y BD |
| EAC-02 | Despliegue desacoplado por nodos para continuidad operacional |
| EAC-03 | Portal de proveedores y controles de seguridad / auditoria para acceso externo |
| EAC-04 | Capa de integracion empresarial compatible con arquitectura existente |
| EAC-05 | Aplicacion modular en capas con separacion de negocio, integracion y servicios transversales |
| EAC-06 | Portal interno de compras y portal de proveedores como fronteras diferenciadas |
| EAC-07 | Despliegue por nodos y desacoplamiento entre negocio e infraestructura |

## Nota de sustento con el enunciado

Estas tablas se apoyan en el caso Harley-Davidson porque:

1. La SMS busca mejorar **calidad, costes y plazos**.
2. La nota 10 liga la gestion de proveedores con relaciones, rendimiento y mejora QCT.
3. El caso exige compatibilidad con la arquitectura corporativa existente.
4. Se descartan candidatos por incompatibilidad arquitectonica.
5. En los criterios de seleccion aparecen compatibilidad de arquitecturas, portabilidad y funcionalidad Internet inmediata.
6. El caso habla de consolidacion de datos, vision empresarial y acceso de proveedores a informacion relevante.
