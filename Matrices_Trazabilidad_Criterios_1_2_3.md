# Acoplamiento de Matrices de Trazabilidad (Criterios 1, 2 y 3)

## 1) Alcance revisado del proyecto

Se revisaron todos los elementos del workspace:

- Caso_Seleccionsoftwareempresarial_S12_convertido.md
- README.md
- Stakeholders_Harley_SILK (1).md
- core.png
- primeradescomposicion.png
- cun01.png
- cun02.png
- cun03.png

## 2) Nota de formato

Las matrices se presentan en formato clasico de trazabilidad (filas vs columnas), usando marca `X` para indicar relacion.

## 3) Catalogo base para trazabilidad

### 3.1 Stakeholders directos (STK)

- STK-01: Organizacion de Compras
- STK-02: Proveedores / Suministradores
- STK-03: Solicitantes internos de compra
- STK-04: Cuentas de Acreedores Comerciales
- STK-05: Logistica
- STK-06: Ingenieria / Desarrollo de Producto
- STK-07: Fabricacion / Centros de produccion

### 3.2 Requerimientos funcionales (REQ)

- REQ-01: Integrar proveedores en desarrollo de producto
- REQ-02: Desarrollar relaciones con proveedores
- REQ-03: Evaluar y seleccionar proveedores
- REQ-04: Gestionar rendimiento de proveedores
- REQ-05: Procesar requisiciones de compra
- REQ-06: Emitir ordenes de compra
- REQ-07: Gestionar recepcion de materiales
- REQ-08: Procesar facturas de proveedores
- REQ-09: Gestionar resultados de suministradores
- REQ-10: Gestionar integracion con suministradores
- REQ-11: Gestionar contactos de suministradores

### 3.3 Casos de uso (CU)

- CU-01: CUN-01 Gestionar proveedores estrategicos
- CU-02: CUN-02 Gestionar compras y abastecimiento
- CU-03: CUN-03 Gestionar informacion de suministros
- CU-04: Integrar proveedores en desarrollo de producto
- CU-05: Desarrollar relaciones con proveedores
- CU-06: Evaluar y seleccionar proveedores
- CU-07: Gestionar rendimiento de proveedores
- CU-08: Procesar requisiciones de compra
- CU-09: Emitir ordenes de compra
- CU-10: Gestionar recepcion de materiales
- CU-11: Procesar facturas de proveedores
- CU-12: Gestionar resultados de suministradores
- CU-13: Gestionar integracion con suministradores
- CU-14: Gestionar contactos de suministradores

## 4) Matriz 1: Stakeholders vs Requerimientos

| Stakeholder | REQ-01 | REQ-02 | REQ-03 | REQ-04 | REQ-05 | REQ-06 | REQ-07 | REQ-08 | REQ-09 | REQ-10 | REQ-11 |
|---|---|---|---|---|---|---|---|---|---|---|---|
| STK-01 Organizacion de Compras | X | X | X | X | X | X | X | X | X | X | X |
| STK-02 Proveedores / Suministradores | X | X | X | X |  |  | X | X | X | X | X |
| STK-03 Solicitantes internos de compra |  |  |  |  | X |  |  |  |  |  |  |
| STK-04 Cuentas de Acreedores Comerciales |  |  |  |  |  |  |  | X |  |  |  |
| STK-05 Logistica |  |  |  |  |  |  | X |  |  |  |  |
| STK-06 Ingenieria / Desarrollo de Producto | X | X | X |  |  |  |  |  |  |  |  |
| STK-07 Fabricacion / Centros de produccion |  |  |  |  |  |  | X |  |  |  |  |

## 5) Matriz 2: Requerimientos vs Casos de Uso 
| Requerimiento | CU-01 | CU-02 | CU-03 | CU-04 | CU-05 | CU-06 | CU-07 | CU-08 | CU-09 | CU-10 | CU-11 | CU-12 | CU-13 | CU-14 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| REQ-01 | X |  |  | X |  |  |  |  |  |  |  |  |  |  |
| REQ-02 | X |  |  |  | X |  |  |  |  |  |  |  |  |  |
| REQ-03 | X |  |  |  |  | X |  |  |  |  |  |  |  |  |
| REQ-04 | X |  |  |  |  |  | X |  |  |  |  |  |  |  |
| REQ-05 |  | X |  |  |  |  |  | X |  |  |  |  |  |  |
| REQ-06 |  | X |  |  |  |  |  |  | X |  |  |  |  |  |
| REQ-07 |  | X |  |  |  |  |  |  |  | X |  |  |  |  |
| REQ-08 |  | X |  |  |  |  |  |  |  |  | X |  |  |  |
| REQ-09 |  |  | X |  |  |  |  |  |  |  |  | X |  |  |
| REQ-10 |  |  | X |  |  |  |  |  |  |  |  |  | X |  |
| REQ-11 |  |  | X |  |  |  |  |  |  |  |  |  |  | X |

## 6) Matriz 3: Stakeholders vs Casos de Uso

| Stakeholder | CU-01 | CU-02 | CU-03 | CU-04 | CU-05 | CU-06 | CU-07 | CU-08 | CU-09 | CU-10 | CU-11 | CU-12 | CU-13 | CU-14 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| STK-01 Organizacion de Compras | X | X | X | X | X | X | X | X | X | X | X | X | X | X |
| STK-02 Proveedores / Suministradores | X | X | X | X | X | X | X |  |  | X | X | X | X | X |
| STK-03 Solicitantes internos de compra |  | X |  |  |  |  |  | X |  |  |  |  |  |  |
| STK-04 Cuentas de Acreedores Comerciales |  | X |  |  |  |  |  |  |  |  | X |  |  |  |
| STK-05 Logistica |  | X |  |  |  |  |  |  |  | X |  |  |  |  |
| STK-06 Ingenieria / Desarrollo de Producto | X |  |  | X | X | X |  |  |  |  |  |  |  |  |
| STK-07 Fabricacion / Centros de produccion |  | X |  |  |  |  |  |  |  | X |  |  |  |  |

## 7) Matriz 4: Requerimientos vs Requerimientos (clasica completa)

Leyenda: `I` = Incluye, `D` = Depende de, `C` = Complementa.

| REQ \ REQ | REQ-01 | REQ-02 | REQ-03 | REQ-04 | REQ-05 | REQ-06 | REQ-07 | REQ-08 | REQ-09 | REQ-10 | REQ-11 |
|---|---|---|---|---|---|---|---|---|---|---|---|
| REQ-01 | - | I |  |  |  |  |  |  |  |  |  |
| REQ-02 |  | - |  |  |  |  |  |  |  |  |  |
| REQ-03 |  |  | - |  |  |  |  |  |  |  |  |
| REQ-04 |  |  | D | - |  |  |  |  |  |  |  |
| REQ-05 |  |  |  |  | - |  |  |  |  |  |  |
| REQ-06 |  |  |  |  | I | - |  |  |  |  |  |
| REQ-07 |  |  |  |  |  |  | - |  |  |  |  |
| REQ-08 |  |  |  |  |  |  | D | - |  |  |  |
| REQ-09 |  |  |  | C |  |  |  |  | - |  |  |
| REQ-10 |  | C |  |  |  |  |  |  |  | - | I |
| REQ-11 |  |  |  |  |  |  |  |  |  |  | - |

## 8) Observaciones de consistencia

- Los 7 stakeholders directos del documento de stakeholders quedaron trazados.
- Los 3 casos de uso de primera descomposicion quedaron trazados.
- Los casos de uso expandidos de CUN-01, CUN-02 y CUN-03 quedaron trazados.
- Las relaciones include visibles en diagramas fueron preservadas en la Matriz 4.

## 9) Nota metodologica

Esta entrega evita inventar actores o funcionalidades fuera del material del proyecto.
Cuando un detalle no estaba textual en el enunciado, se uso la relacion mas conservadora visible en los diagramas de casos de uso.
