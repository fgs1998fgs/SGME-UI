# Componentes reutilizables · SGME

Componentes que se repiten en las pantallas del prototipo. Cada uno se define
una sola vez en `styles.css` y se muestra en `componentes.html` con sus
estados. Ninguna pantalla define estilos propios.

| Componente | Elemento HTML | Clase CSS | Pantallas donde aparece |
|---|---|---|---|
| Encabezado | `<header>` | `.cabecera` | Todas menos ingreso, registro, recuperar y 404 |
| Menú de navegación | `<nav>` | `.menu` / `.menu a.activo` | Las mismas del encabezado |
| Pie de página | `<footer>` | `.pie` | Todas |
| Tarjeta de indicador | `<article>` | `.tarjeta` | Panel principal |
| Rejilla de tarjetas | `<section>` | `.rejilla` | Panel principal |
| Tabla de datos | `<table>` | `.tabla` | Productos, lotes, proveedores, usuarios, ventas, reporte |
| Envoltura de tabla | `<div>` | `.tabla-scroll` | Las mismas de la tabla |
| Barra de búsqueda y filtros | `<form>` | `.filtros` | Productos, ventas, reporte de vencimientos |
| Formulario | `<form>` | `.formulario` | Nuevo producto, nueva venta, entrada de lote, perfil, anular |
| Campo de formulario | `<div>` | `.campo` | Dentro de cada formulario |
| Etiqueta | `<label>` | — | Dentro de cada campo |
| Mensaje de error de campo | `<p>` | `.error` | Dentro de cada campo con validación |
| Botón principal | `<button>` | `.btn` | Todas las pantallas con acción |
| Botón secundario | `<button>` / `<a>` | `.btn.btn-sec` | Formularios y confirmaciones |
| Botón de peligro | `<button>` | `.btn.btn-peligro` | Anular venta |
| Marca de estado | `<span>` | `.marca` + modificador | Ventas, lotes, usuarios, proveedores |
| Aviso | `<p>` | `.aviso` + modificador | Confirmaciones, advertencias y mensajes de éxito |
| Ficha de datos | `<dl>` | `.ficha` | Detalle de venta, factura |
| Barra de acciones | `<div>` | `.acciones` | Pie de los formularios |
| Título de página | `<h1>` + `<p>` | `.titulo-pagina` / `.codigo-rf` | Todas |
| Enlace de salto | `<a>` | `.salto` | Todas las que tienen menú |

## Modificadores de estado

| Clase | Para qué |
|---|---|
| `.marca-ok` | Venta activa, usuario activo, proveedor activo |
| `.marca-alerta` | Lote próximo a vencer, stock por debajo del mínimo |
| `.marca-mal` | Venta anulada, lote vencido, cuenta inactiva |
| `.aviso-info` | Mensaje informativo |
| `.aviso-exito` | Operación realizada correctamente |
| `.aviso-peligro` | Advertencia antes de una acción irreversible |
| `.campo.con-error input` | Campo con validación fallida: borde y mensaje visibles |

## Reglas de uso

- Toda pantalla parte de `plantilla.html`: copia el encabezado, el menú, el
  `main` y el pie, y solo reemplaza el contenido del `main`.
- Si una pantalla necesita algo que no está en esta tabla, primero se agrega a
  `styles.css` y a `componentes.html`, y después se usa.
- Los mensajes de error van dentro del `.campo`, debajo del control, nunca en
  una alerta del navegador.
- Las tablas van envueltas en `.tabla-scroll` para que en celular se desplacen
  en horizontal sin romper la página.

## Correcciones del aprendiz

Se llena con lo que Daniel detecte al revisar.

| # | Qué estaba mal o faltaba | Qué se pidió cambiar y por qué |
|---|---|---|
| | | |
