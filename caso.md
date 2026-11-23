# Caso de estudio · SGME — Sistema de Gestión Minimarket Express

## El negocio

El SGME es el sistema de gestión de un minimarket de barrio. Hoy las ventas se
anotan a mano en un cuaderno y el inventario se lleva en una hoja de cálculo,
de modo que nadie sabe con certeza qué hay en bodega ni qué está por vencerse.

## Usuarios del sistema

- **Cajero.** Atiende la caja: registra las ventas, cobra y emite la factura.
- **Administrador.** Hace todo lo del cajero y además gestiona los productos,
  los lotes, los proveedores, los usuarios y las anulaciones.

Cada persona entra al sistema con su número de documento y su contraseña.

## Información que maneja

- **Usuarios.** Documento, nombre, apellido, rol (cajero o administrador) y si
  la cuenta está activa.
- **Categorías.** Agrupan los productos: lácteos, granos, aseo, bebidas.
- **Productos.** Código de barras, nombre, precio de venta, categoría, si es
  perecedero y el stock mínimo a partir del cual hay que volver a pedir.
- **Lotes.** La mercancía llega por lotes. Del mismo producto puede haber dos
  lotes con fechas de vencimiento distintas, y hay que saber cuál sale primero.
  Cada lote tiene número, fecha de vencimiento, fecha de ingreso, cantidad
  disponible y el proveedor que lo trajo.
- **Proveedores.** NIT, razón social, teléfono y persona de contacto.
- **Ventas.** Fecha y hora, total y estado. Cada venta lleva varios productos,
  y de cada uno se guarda la cantidad y el precio al que se vendió ese día.
- **Facturas.** Al cerrar la venta se emite una factura con número consecutivo.
- **Anulaciones.** Una venta se puede anular; queda registrado el motivo, quién
  la anuló y cuándo. La venta no se borra.

## Necesidades que el sistema debe resolver

1. Que cada persona entre con su documento y su contraseña, y que el sistema
   sepa si es cajero o administrador.
2. Que el cajero registre una venta agregando productos por código de barras y
   vea el total en pantalla antes de cobrar.
3. Que al cerrar la venta se emita la factura con su número consecutivo.
4. Que se pueda consultar el inventario y saber cuántas unidades hay de cada
   producto.
5. Que el sistema avise qué productos están por debajo del stock mínimo y qué
   lotes están próximos a vencerse.
6. Que el administrador registre productos, lotes y proveedores.
7. Que el administrador anule una venta dejando constancia del motivo.
8. Que el administrador gestione las cuentas de los usuarios.

## Restricciones

- Solo HTML5, CSS3 y JavaScript puro. Sin frameworks ni librerías externas.
- Toda la interfaz en español.
- Debe verse bien en celular: el cajero consulta el inventario desde el pasillo.
- Los datos que aparecen en las pantallas son ficticios.

## Fuera del alcance de esta entrega

- Conexión a la base de datos. Estas evidencias cubren la interfaz gráfica.
- Pagos en línea, facturación electrónica ante la DIAN y aplicación móvil
  nativa. El sistema es web y se usa dentro del local.
- Domicilios, programa de puntos y compras a proveedores en línea.
