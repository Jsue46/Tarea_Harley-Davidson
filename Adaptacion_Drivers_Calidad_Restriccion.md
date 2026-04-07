# Adaptacion de Drivers de Calidad y Restriccion (basado en el enunciado)

## 1. Requisitos / Drivers Funcionales (derivados del caso)

| ID | Driver funcional | Descripcion |
|---|---|---|
| DF-01 | Requisiciones y plazos | Gestionar requisitos/requisiciones/plazos de compras. |
| DF-02 | Documentos de compra | Crear documentos de compra (pedidos). |
| DF-03 | Recibos y seguimiento | Registrar recibos y dar seguimiento a recepcion. |
| DF-04 | Procesado de facturas | Procesar facturas de proveedores. |
| DF-05 | Resultados de suministradores | Gestionar informacion sobre resultados de proveedores. |
| DF-06 | Comunicacion e integracion | Gestionar comunicacion/integracion de suministradores. |
| DF-07 | Contactos de suministradores | Administrar contactos con proveedores. |
| DF-08 | Soporte a proyectos de producto | Soportar planificacion, recursos, costos objetivo y lanzamiento. |

## 2. Requisitos / Drivers de Atributos de Calidad (EAC)

| ID | Categoria | Escenario (formato fuente-estimulo-respuesta) | Prioridad |
|---|---|---|---|
| EAC-01 | Compatibilidad arquitectonica | Fuente: equipo SI. Estimulo: evaluar paquetes candidatos. Respuesta: soluciones compatibles con arquitectura y con iniciativas TI en marcha. | Alta |
| EAC-02 | Adecuacion funcional | Fuente: equipo SiL'K. Estimulo: revisar propuestas frente a especificacion funcional. Respuesta: seleccionar soluciones con mayor ajuste funcional. | Alta |
| EAC-03 | Disponibilidad operativa | Fuente: operaciones/fabricacion. Estimulo: cambios en procesos/sistemas. Respuesta: no afectar la continuidad de lineas de produccion. | Alta |
| EAC-04 | Gestion del cambio y adopcion | Fuente: organizacion de compras. Estimulo: implementacion de nuevo sistema. Respuesta: soporte en formacion/metodologia de cambio para adopcion real. | Alta |
| EAC-05 | Calidad, costo y plazo (QCT) | Fuente: estrategia SMS. Estimulo: operacion de compras/proveedores. Respuesta: contribuir a metas de calidad, costos y plazos. | Alta |
| EAC-06 | Visibilidad de datos para decision | Fuente: direccion/compras. Estimulo: necesidad de consolidar y analizar base de aprovisionamiento. Respuesta: disponer vision empresarial y consolidacion de datos. | Media-Alta |
| EAC-07 | Relacion de largo plazo con proveedores | Fuente: estrategia de suministros. Estimulo: pasar de transaccional a relacion de largo plazo. Respuesta: mecanismos de colaboracion y seguimiento continuo. | Media-Alta |

## 3. Drivers de Restriccion

| Tipo de restriccion | Restriccion | Implicacion para arquitectura |
|---|---|---|
| Del cliente/negocio | No buscar una solucion ERP completa; ambito bien delimitado. | Arquitectura acotada al dominio de compras/suministros; integracion selectiva. |
| Del cliente/negocio | Mantener continuidad operativa de produccion. | Despliegue e implantacion con bajo riesgo operacional. |
| Del cliente/negocio | Implementacion por fases del proyecto SiL'K. | Roadmap arquitectonico incremental por Fase 1/2/3. |
| Del cliente/negocio | Valores corporativos y enfoque de relacion con socios. | Criterios de seleccion/implantacion incluyen ajuste cultural y gestion de cambio. |
| De tecnologia/organizacion | Compatibilidad con arquitectura SI existente y proyectos TI en curso. | Evaluacion tecnica obligatoria de integracion/interconexion. |
| De tecnologia/organizacion | Heterogeneidad de sistemas de compras entre plantas/divisiones. | Necesidad de estandarizar procesos y convivir con legado durante transicion. |

## 4. Adaptacion de drivers a pasos para definir la arquitectura

| Paso | Actividad de arquitectura | Drivers de calidad aplicados | Restricciones aplicadas | Resultado |
|---|---|---|---|---|
| 1 | Delimitar ambito | EAC-02, EAC-05 | No ERP completo, ambito delimitado | Alcance tecnico del sistema SiL'K |
| 2 | Definir arquitectura objetivo | EAC-01, EAC-06 | Compatibilidad con arquitectura vigente | Principios y estructura de referencia |
| 3 | Diseñar roadmap por fases | EAC-03, EAC-04 | Implementacion Fase 1/2/3 | Arquitectura incremental |
| 4 | Diseñar capa transaccional (Fase 1) | EAC-02, EAC-03 | Continuidad operativa | Solucion para requisicion-pedido-recibo-factura |
| 5 | Diseñar capa de informacion de suministradores (Fase 2) | EAC-06, EAC-07 | Integracion con red de suministros | Solucion para resultados/comunicacion/contactos |
| 6 | Diseñar soporte a seguimiento de proyectos (Fase 3) | EAC-05, EAC-06 | Convivencia con procesos existentes | Solucion para planificacion/recursos/costos objetivo |
| 7 | Definir criterios de evaluacion tecnica | EAC-01, EAC-02, EAC-04 | Compatibilidad e implementabilidad | Matriz de decision funcional y cualitativa |
| 8 | Validar arquitectura y riesgos | EAC-03, EAC-04, EAC-05 | Restricciones operativas/culturales | Plan de mitigacion de riesgos de implantacion |

## 5. Determinacion del modelo de calidad (derivado del enunciado)

### 5.1 Modelo propuesto

Se define un modelo de calidad SiL'K con 6 ejes, construidos a partir del caso y sus anexos:

| Eje de calidad | Definicion en el contexto SiL'K |
|---|---|
| MQ-01 Adecuacion funcional | Grado en que la solucion cubre la especificacion funcional. |
| MQ-02 Compatibilidad arquitectonica | Grado de ajuste con arquitectura SI existente e iniciativas en curso. |
| MQ-03 Calidad-Costo-Plazo (QCT) | Contribucion a metas de calidad, costos y plazos en compras/suministros. |
| MQ-04 Disponibilidad operativa | Capacidad de cambio sin detener operaciones criticas. |
| MQ-05 Gestion del cambio/adopcion | Capacidad de implantacion con formacion y cambio organizacional efectivo. |
| MQ-06 Relacion de largo plazo con proveedores | Capacidad de sostener colaboracion y mejora continua con suministradores. |

### 5.2 Indicadores del modelo de calidad

| Eje | Indicador | Regla/Meta de referencia |
|---|---|---|
| MQ-01 | Porcentaje de adecuacion funcional | Referencia de alto ajuste: >= 90% (usado en evaluaciones del caso) |
| MQ-02 | Numero de incompatibilidades arquitectonicas criticas | Objetivo: 0 incompatibilidades bloqueantes |
| MQ-03 | Evidencia de mejora en QCT | Evidencia documentada de mejora en calidad, costo o plazo |
| MQ-04 | Incidentes de interrupcion por implantacion | Objetivo: sin interrupciones criticas de produccion |
| MQ-05 | Cobertura de plan de formacion/cambio | Plan definido y ejecutado para areas impactadas |
| MQ-06 | Mecanismos activos de seguimiento a proveedores | Indicadores y revisiones periodicas habilitadas |

### 5.3 Criterios de aceptacion del modelo

| Criterio | Condicion |
|---|---|
| CA-01 | Todos los DF (DF-01..DF-08) trazados a decisiones arquitectonicas |
| CA-02 | Todos los EAC (EAC-01..EAC-07) con evidencia de evaluacion |
| CA-03 | Todas las restricciones reflejadas en el diseño y plan por fases |
| CA-04 | El modelo de calidad permite comparar alternativas de solucion |

## 6. Sintesis final

| Elemento | Resultado |
|---|---|
| Base de informacion | Derivada del enunciado del caso y sus anexos relevantes |
| Formato solicitado | Estructura en tablas (drivers funcionales, EAC, restricciones, pasos, modelo) |
| Alineacion al proyecto | Coherente con CUN y con el despliegue definido para SiL'K |
