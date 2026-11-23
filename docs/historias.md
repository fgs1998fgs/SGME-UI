# Historias de usuario · SGME

Fuente: `caso.md`. Prioridad según MoSCoW (Must, Should, Could, Won't).
Roles del sistema: **cajero** y **administrador**.

| Código | Historia de usuario | Criterios de aceptación | Prioridad |
|---|---|---|---|
| HU-01 | Como **usuario del sistema** quiero ingresar con mi documento y mi contraseña para que nadie más pueda operar la caja con mi cuenta. | Pide documento y contraseña. Muestra un mensaje junto al campo si alguno queda vacío. Si las credenciales no coinciden, el mensaje no dice cuál de los dos está mal. Al entrar, lleva al panel que corresponde al rol. | Must |
| HU-02 | Como **usuario del sistema** quiero recuperar mi contraseña para volver a entrar cuando la olvide. | Pide el documento registrado. Confirma en pantalla que se envió la instrucción. No revela si el documento existe o no. | Should |
| HU-03 | Como **cajero** quiero registrar una venta agregando productos por código de barras para cobrar rápido sin anotar nada a mano. | Permite agregar productos uno a uno. Muestra nombre, cantidad, precio unitario y subtotal de cada línea. Recalcula el total al agregar o quitar una línea. No deja cerrar la venta sin al menos un producto. | Must |
| HU-04 | Como **cajero** quiero que al cerrar la venta se emita la factura con su número consecutivo para entregarle el comprobante al cliente. | Muestra número de factura, fecha y hora, detalle de productos y total. Permite imprimir. El número no se repite. | Must |
| HU-05 | Como **cajero** quiero consultar el inventario desde el celular para responderle al cliente si hay existencias sin ir hasta la bodega. | Lista los productos con su nombre, categoría, precio y unidades disponibles. Permite buscar por nombre o código de barras. Se ve correctamente a 375 px de ancho. | Must |
| HU-06 | Como **administrador** quiero ver en un panel los indicadores del día para saber en qué está el negocio apenas entro. | Muestra ventas del día, total recaudado, productos bajo el stock mínimo y lotes próximos a vencerse. Cada indicador lleva a su listado. | Must |
| HU-07 | Como **administrador** quiero registrar y editar productos para mantener el catálogo al día. | Exige código de barras, nombre, categoría y precio de venta. El precio debe ser mayor que cero. Avisa si el código de barras ya existe. Permite marcar el producto como perecedero. | Must |
| HU-08 | Como **administrador** quiero registrar la entrada de un lote para saber cuánta mercancía llegó, de qué proveedor y cuándo se vence. | Exige producto, proveedor, número de lote, cantidad y fecha de ingreso. Si el producto es perecedero, exige también la fecha de vencimiento. La fecha de vencimiento no puede ser anterior a la de ingreso. | Must |
| HU-09 | Como **administrador** quiero ver qué lotes están próximos a vencerse para sacarlos antes de perder la mercancía. | Permite consultar por rango de fechas. Ordena del más próximo a vencer al más lejano. Distingue visualmente los vencidos de los próximos a vencer. | Must |
| HU-10 | Como **administrador** quiero anular una venta dejando constancia del motivo para que quede el rastro de por qué se anuló. | Exige un motivo escrito de mínimo 10 caracteres. Muestra los datos de la venta antes de confirmar. Advierte que la acción no se puede deshacer. La venta no se borra: queda en estado anulada. | Must |
| HU-11 | Como **administrador** quiero gestionar los proveedores para saber a quién reclamarle cuando un lote sale malo. | Exige NIT y razón social. Guarda teléfono y persona de contacto. Permite desactivar un proveedor sin borrar su historial de lotes. | Should |
| HU-12 | Como **administrador** quiero gestionar las cuentas de los usuarios para dar y quitar acceso al sistema. | Exige documento, nombre, apellido y rol. Permite desactivar una cuenta sin borrarla. No muestra nunca la contraseña guardada. | Should |
| HU-13 | Como **usuario del sistema** quiero cambiar mi contraseña desde mi perfil para no depender del administrador. | Pide la contraseña actual y la nueva dos veces. Avisa si las dos nuevas no coinciden. Exige mínimo 8 caracteres. | Should |
| HU-14 | Como **administrador** quiero consultar las ventas de un periodo para cuadrar la caja y revisar las anulaciones. | Permite filtrar por rango de fechas y por estado. Muestra número de factura, fecha, cajero, total y estado. Suma el total del periodo consultado. | Should |

## Decisiones tomadas al redactar

Quedan anotadas para poder sustentarlas; no son correcciones de la bitácora.

- **El rol va nombrado.** Cada historia dice «cajero» o «administrador» en vez
  de «el usuario», salvo las tres que aplican a los dos perfiles. Sin rol, el
  criterio de aceptación no se puede verificar contra los permisos.
- **Nada de pagos en línea.** `caso.md` los deja fuera del alcance, así que no
  se redactó ninguna historia sobre ellos.
- **HU-01 y HU-02 no revelan si el documento existe.** El mensaje no distingue
  entre documento inexistente y contraseña equivocada.
- **HU-08 condiciona la fecha de vencimiento.** Solo se exige si el producto es
  perecedero, porque la tabla `lote` de la base de datos ya construida deja esa
  fecha vacía cuando no lo es.
- **Son 14 y no 8.** La guía pide mínimo 8; con 14 hay requisitos suficientes
  para sostener las 17 interfaces sin inventar pantallas.

## Correcciones del aprendiz

Esta tabla se llena con lo que Daniel detecte al revisar. Va vacía a propósito:
la bitácora registra correcciones reales, no supuestas.

| # | Qué estaba mal o faltaba | Qué se pidió cambiar y por qué |
|---|---|---|
| | | |
