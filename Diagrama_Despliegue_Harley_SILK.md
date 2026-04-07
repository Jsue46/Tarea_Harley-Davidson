# Diagrama de Despliegue - Harley-Davidson SiL'K

## Objetivo

Definir la arquitectura de despliegue de SiL'K basada en lo ya establecido en el proyecto:

- CUN-01: Gestionar proveedores estrategicos
- CUN-02: Gestionar compras y abastecimiento
- CUN-03: Gestionar informacion de suministros

## Diagrama (PlantUML)

```plantuml
@startuml
title Diagrama de Despliegue - Harley-Davidson SiL'K

left to right direction
skinparam shadowing false
skinparam componentStyle rectangle

node "Dispositivo movil" as MOBILE
node "PC usuario" as PC
node "Sistema externo\n(Proveedores / Suministradores)" as EXT

node "Servidor web" as WEB {
  component "<<capa>>\nPresentacion\n(Portal interno y portal proveedores)" as PRESENT
  component "<<capa>>\nServicios web\n(API SiL'K)" as WS
}

node "Servidor aplicativo" as APP {
  package "<<capa>> Negocio" as NEG {
    component "Gestionar proveedores estrategicos" as N1
    component "Gestionar compras y abastecimiento" as N2
    component "Gestionar informacion de suministros" as N3
  }
  component "<<capa>>\nDatos\n(Acceso transaccional)" as DAT
  component "<<capa>>\nIntegracion\n(Conectores ERP/AP/INV/MDM)" as INT
}

node "Servidor BD" as DBSRV {
  database "BD SiL'K\n+ Reportes/Indicadores" as DB
}

node "Sistema de pagos\n(Cuentas por pagar)" as PAY

MOBILE --> WEB : HTTPS
PC --> WEB : HTTP/HTTPS
EXT --> WEB : HTTPS

WEB --> APP : HTTPS/REST

N1 ..> DAT
N2 ..> DAT
N3 ..> DAT
N1 ..> INT
N2 ..> INT
N3 ..> INT

DAT --> DB : JDBC/SQL
APP --> DBSRV

INT --> PAY

@enduml
```

## Trazabilidad de arquitectura con el alcance definido

- Gestionar proveedores estrategicos: evaluar y seleccionar proveedores, desarrollar relaciones, gestionar rendimiento e integrar proveedores en desarrollo de producto.
- Gestionar compras y abastecimiento: procesar requisiciones, emitir ordenes de compra, gestionar recepcion de materiales y procesar facturas de proveedores.
- Gestionar informacion de suministros: gestionar resultados, integracion y contactos de suministradores.

## Vista por capas

- Capa de acceso: dispositivo movil, PC usuario y sistema externo.
- Capa web: presentacion y servicios web (API SiL'K).
- Capa aplicativo: negocio, datos e integracion.
- Capa de datos fisica: servidor BD con base transaccional y reportes.
- Sistema externo de pagos: integrado desde la capa de integracion.

## Supuestos minimos (alineados al caso)

- La solucion no reemplaza totalmente los sistemas existentes, los integra.
- El acceso se canaliza por un servidor web unificado para usuarios y proveedores.
- La operacion requiere disponibilidad continua por impacto en compras y abastecimiento.
- Los indicadores de desempeno de suministradores se alimentan desde eventos transaccionales.
