# Requisitos funcionales · SGME

Fuente: `docs/historias.md`. Cada requisito indica la historia de usuario de la
que proviene. El sistema se describe como caja negra: qué debe hacer, no cómo.

| Código | Requisito | HU de origen | Prioridad |
|---|---|---|---|
| RF-01 | El sistema debe autenticar al usuario con su número de documento y su contraseña. | HU-01 | Must |
| RF-02 | El sistema debe mostrar un mensaje junto al campo cuando el documento o la contraseña queden vacíos. | HU-01 | Must |
| RF-03 | El sistema debe rechazar credenciales incorrectas con un mensaje único que no indique cuál de los dos datos falló. | HU-01 | Must |
| RF-04 | El sistema debe dirigir al usuario al panel correspondiente a su rol después de autenticarse. | HU-01 | Must |
| RF-05 | El sistema debe permitir solicitar la recuperación de la contraseña indicando el documento registrado. | HU-02 | Should |
| RF-06 | El sistema debe confirmar el envío de la instrucción de recuperación sin revelar si el documento existe. | HU-02 | Should |
| RF-07 | El sistema debe permitir agregar productos a una venta mediante su código de barras. | HU-03 | Must |
| RF-08 | El sistema debe mostrar por cada línea de la venta el nombre, la cantidad, el precio unitario y el subtotal. | HU-03 | Must |
| RF-09 | El sistema debe recalcular el total de la venta cada vez que se agrega o se elimina una línea. | HU-03 | Must |
| RF-10 | El sistema debe impedir cerrar una venta que no tenga al menos un producto. | HU-03 | Must |
| RF-11 | El sistema debe emitir una factura con número consecutivo al cerrar la venta. | HU-04 | Must |
| RF-12 | El sistema debe mostrar en la factura el número, la fecha y hora, el detalle de los productos y el total. | HU-04 | Must |
| RF-13 | El sistema debe permitir imprimir la factura emitida. | HU-04 | Must |
| RF-14 | El sistema debe listar los productos con nombre, categoría, precio y unidades disponibles. | HU-05 | Must |
| RF-15 | El sistema debe permitir buscar productos por nombre o por código de barras. | HU-05 | Must |
| RF-16 | El sistema debe presentar los listados sin desbordamiento horizontal en pantallas de 375 px de ancho. | HU-05 | Must |
| RF-17 | El sistema debe mostrar en el panel principal las ventas del día, el total recaudado, los productos bajo el stock mínimo y los lotes próximos a vencerse. | HU-06 | Must |
| RF-18 | El sistema debe permitir abrir el listado correspondiente desde cada indicador del panel. | HU-06 | Must |
| RF-19 | El sistema debe permitir registrar un producto con código de barras, nombre, categoría y precio de venta. | HU-07 | Must |
| RF-20 | El sistema debe rechazar un precio de venta menor o igual a cero. | HU-07 | Must |
| RF-21 | El sistema debe avisar cuando el código de barras ingresado ya está registrado. | HU-07 | Must |
| RF-22 | El sistema debe permitir marcar un producto como perecedero. | HU-07 | Must |
| RF-23 | El sistema debe permitir editar los datos de un producto existente. | HU-07 | Must |
| RF-24 | El sistema debe permitir registrar la entrada de un lote indicando producto, proveedor, número de lote, cantidad y fecha de ingreso. | HU-08 | Must |
| RF-25 | El sistema debe exigir la fecha de vencimiento únicamente cuando el producto es perecedero. | HU-08 | Must |
| RF-26 | El sistema debe rechazar una fecha de vencimiento anterior a la fecha de ingreso. | HU-08 | Must |
| RF-27 | El sistema debe permitir consultar los lotes por rango de fechas de vencimiento. | HU-09 | Must |
| RF-28 | El sistema debe ordenar los lotes del más próximo a vencer al más lejano. | HU-09 | Must |
| RF-29 | El sistema debe distinguir visualmente los lotes vencidos de los próximos a vencer. | HU-09 | Must |
| RF-30 | El sistema debe permitir anular una venta registrando el motivo. | HU-10 | Must |
| RF-31 | El sistema debe exigir que el motivo de anulación tenga mínimo 10 caracteres. | HU-10 | Must |
| RF-32 | El sistema debe mostrar los datos de la venta y advertir que la acción no se puede deshacer antes de confirmar la anulación. | HU-10 | Must |
| RF-33 | El sistema debe conservar la venta anulada cambiando su estado, sin eliminarla. | HU-10 | Must |
| RF-34 | El sistema debe permitir registrar un proveedor con NIT y razón social, y opcionalmente teléfono y persona de contacto. | HU-11 | Should |
| RF-35 | El sistema debe permitir desactivar un proveedor conservando su historial de lotes. | HU-11 | Should |
| RF-36 | El sistema debe permitir registrar un usuario con documento, nombre, apellido y rol. | HU-12 | Should |
| RF-37 | El sistema debe permitir desactivar una cuenta de usuario sin eliminarla. | HU-12 | Should |
| RF-38 | El sistema no debe mostrar en ninguna pantalla la contraseña almacenada de un usuario. | HU-12 | Should |
| RF-39 | El sistema debe permitir al usuario cambiar su contraseña indicando la actual y la nueva dos veces. | HU-13 | Should |
| RF-40 | El sistema debe avisar cuando las dos contraseñas nuevas no coinciden. | HU-13 | Should |
| RF-41 | El sistema debe exigir que la contraseña nueva tenga mínimo 8 caracteres. | HU-13 | Should |
| RF-42 | El sistema debe permitir consultar las ventas filtrando por rango de fechas y por estado. | HU-14 | Should |
| RF-43 | El sistema debe mostrar en la consulta de ventas el número de factura, la fecha, el cajero, el total y el estado. | HU-14 | Should |
| RF-44 | El sistema debe sumar el total de las ventas del periodo consultado. | HU-14 | Should |

## Cobertura

Las 14 historias de usuario quedan cubiertas: HU-01 (RF-01 a RF-04),
HU-02 (RF-05, RF-06), HU-03 (RF-07 a RF-10), HU-04 (RF-11 a RF-13),
HU-05 (RF-14 a RF-16), HU-06 (RF-17, RF-18), HU-07 (RF-19 a RF-23),
HU-08 (RF-24 a RF-26), HU-09 (RF-27 a RF-29), HU-10 (RF-30 a RF-33),
HU-11 (RF-34, RF-35), HU-12 (RF-36 a RF-38), HU-13 (RF-39 a RF-41),
HU-14 (RF-42 a RF-44).

Ningún requisito proviene de algo que no esté en `docs/historias.md`.

## Correcciones del aprendiz

Se llena con lo que Daniel detecte al revisar.

| # | Qué estaba mal o faltaba | Qué se pidió cambiar y por qué |
|---|---|---|
| | | |
