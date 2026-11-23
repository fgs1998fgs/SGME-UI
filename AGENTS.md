# Proyecto SGME — Sistema de Gestión Minimarket Express

Sistema web para la gestión de inventario y ventas de un minimarket de barrio.
Lo usan dos perfiles: el cajero, que vende, y el administrador, que además
gestiona productos, lotes, proveedores, usuarios y anulaciones.

El contexto completo del negocio está en `caso.md`. Léelo antes de proponer
cualquier pantalla.

## Reglas

- Solo HTML5, CSS3 y JavaScript puro. No usar frameworks ni librerías: nada de
  React, Vue, Tailwind, Bootstrap ni enlaces a CDN.
- Toda la interfaz en español. Ningún texto visible en inglés, incluidos los
  botones y los mensajes de error.
- HTML semántico: `header`, `nav`, `main`, `section`, `form`, `table`, `footer`.
  Cada campo de formulario lleva su `<label>` asociado con `for` e `id`.
- Un solo `styles.css` con las variables de color en `:root`. Ninguna pantalla
  define estilos propios ni usa atributos `style` en línea.
- Toda pantalla parte de `plantilla.html` y usa solo las clases de `styles.css`.
  Si falta un componente, se agrega primero a `styles.css` y a
  `componentes.html`, y después se usa.
- Diseño responsivo: debe verse bien en celular, a 375 px de ancho, sin
  desbordamiento horizontal.
- Accesibilidad: contraste suficiente, foco visible al navegar con teclado,
  mensajes de error junto al campo y no en una alerta del navegador.
- Sin IDs duplicados en una misma página.
- Solo datos ficticios. Nunca nombres reales, documentos reales ni contraseñas.
- Antes de crear o modificar archivos, muestra el plan y espera mi confirmación.

## Alcance

Esta entrega cubre únicamente la interfaz gráfica. No hay conexión a base de
datos, no hay backend y no se implementan pagos en línea, facturación
electrónica ni aplicación móvil nativa. Si una pantalla necesita datos, se usan
datos ficticios escritos directamente en el HTML.

## Trazabilidad

Cada pantalla debe declarar bajo su título el código del requisito funcional
que cumple, tomado de `docs/requisitos.md`. No inventes requisitos: si algo no
está en `docs/historias.md` o `docs/requisitos.md`, pregúntame antes.

## Estructura del proyecto

```
sgme-ui/
├── AGENTS.md
├── caso.md
├── docs/
│   ├── historias.md
│   ├── requisitos.md
│   └── componentes.md
├── prototipo/          mockups de baja fidelidad en escala de grises
├── styles.css          variables y componentes
├── plantilla.html      estructura común
├── componentes.html    guía de estilos
└── index.html y demás pantallas
```
