# Mapa de navegación · SGME

Cada nodo corresponde a una pantalla del prototipo (`prototipo/`) y a su
interfaz final. Entre paréntesis van los requisitos funcionales que cumple.

```mermaid
flowchart TD
    I[Ingreso<br/>RF-01 a RF-04] -->|Credenciales correctas| P[Panel principal<br/>RF-17 · RF-18]
    I -->|Olvidé mi contraseña| R[Recuperar contraseña<br/>RF-05 · RF-06]
    R -->|Volver| I

    P --> NV[Nueva venta<br/>RF-07 a RF-10]
    P --> LV[Consulta de ventas<br/>RF-42 a RF-44]
    P --> LP[Productos<br/>RF-14 a RF-16]
    P --> RV[Reporte de vencimientos<br/>RF-27 a RF-29]

    NV -->|Cobrar| F[Factura emitida<br/>RF-11 a RF-13]
    F -->|Nueva venta| NV
    F -->|Volver| P

    LV -->|Ver| DV[Detalle de la venta<br/>RF-43]
    DV -->|Anular| AV[Anular venta<br/>RF-30 a RF-33]
    AV -->|Cancelar| DV

    LP -->|Registrar / Editar| NP[Registrar producto<br/>RF-19 a RF-23]
    NP -->|Cancelar| LP

    P --> LL[Lotes en bodega<br/>RF-28 · RF-29]
    LL -->|Registrar entrada| EL[Entrada de lote<br/>RF-24 a RF-26]
    EL -->|Cancelar| LL
    LL -->|Consultar vencimientos| RV
    RV -->|Ver lotes| LL

    P --> LPR[Proveedores<br/>RF-34 · RF-35]
    LPR -->|Registrar / Editar| NPR[Registrar proveedor<br/>RF-34]
    NPR -->|Cancelar| LPR

    P --> LU[Usuarios<br/>RF-36 a RF-38]
    P --> PF[Mi perfil<br/>RF-39 a RF-41]

    E404[Página no encontrada<br/>Error 404] -->|Ir al panel| P

    I -->|Cerrar sesión desde cualquier pantalla| I
```

## Cómo se recorre

El ingreso es la única puerta: sin autenticarse no se llega a ninguna otra
pantalla. Desde el panel principal se alcanza todo el sistema, y el menú
superior está presente en todas las pantallas internas, de modo que ninguna
queda sin salida.

Hay tres recorridos que importan:

1. **Vender.** Ingreso → Panel → Nueva venta → Factura. Es el camino que más
   se repite en el día y por eso «Nueva venta» es la segunda opción del menú.
2. **Anular.** Panel → Consulta de ventas → Detalle → Anular. La anulación
   queda a tres clics y detrás de una confirmación, porque es irreversible.
3. **Controlar el vencimiento.** Panel → Reporte de vencimientos → Lotes. El
   indicador de «lotes por vencer» del panel lleva directo al reporte.

## Comprobación

El generador del prototipo verifica dos cosas antes de escribir los archivos y
se detiene si alguna falla:

- que todo enlace apunte a un nodo que exista, de modo que no haya enlaces
  rotos;
- que ninguna pantalla quede sin salida.

Las 18 pantallas pasaron las dos comprobaciones.
