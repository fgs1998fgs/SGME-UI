# SGME · Interfaz gráfica

Interfaz del **Sistema de Gestión Minimarket Express**, el proyecto formativo
de la ficha 3389057.

- **Evidencia:** GA6-220501096 · AA3 y AA4
- **Aprendiz:** Daniel Felipe González Sabogal
- **Programa:** Tecnología en Análisis y Desarrollo de Software · SENA
- **Agente de codificación:** Claude Code

## Cómo verlo

No hace falta instalar nada: se abre `index.html` con doble clic en cualquier
navegador. Desde ahí se entra al sistema con el documento `1024595068` y la
contraseña `sgme2026`.

Si prefiere servirlo, desde esta carpeta:

```
python -m http.server 8788
```

y abrir `http://localhost:8788`.

## Qué hay aquí

| Ruta | Qué es |
|---|---|
| `AGENTS.md` | Reglas que el agente de codificación lee en cada sesión |
| `caso.md` | El caso de estudio del minimarket |
| `docs/historias.md` | 14 historias de usuario con criterios y prioridad MoSCoW |
| `docs/requisitos.md` | 44 requisitos funcionales con trazabilidad a su historia |
| `docs/componentes.md` | Los componentes reutilizables y dónde aparece cada uno |
| `docs/navegacion.md` | Mapa de navegación en Mermaid |
| `prototipo/` | Mockups de baja fidelidad en escala de grises, navegables |
| `styles.css` | Única hoja de estilos, con las variables en `:root` |
| `plantilla.html` | Estructura común de la que parte toda pantalla |
| `componentes.html` | Guía de estilos: cada componente con sus estados |
| Las demás `.html` | Las 18 interfaces del sistema |

## Alcance

Esta entrega cubre **solo la interfaz gráfica**. No hay conexión a base de
datos ni backend: los datos que aparecen en las pantallas son ficticios y
están escritos en el propio HTML.

El modelo de datos está construido aparte, en la evidencia de AA1 y AA2: nueve
tablas en PostgreSQL sobre Supabase.

## Restricciones cumplidas

- Solo HTML5, CSS3 y JavaScript puro. Sin frameworks, sin librerías y sin
  enlaces a CDN.
- Toda la interfaz en español.
- Una sola hoja de estilos; ninguna pantalla define estilos propios ni usa el
  atributo `style` en línea.
- Cada campo de formulario con su `<label>` asociado, foco visible al navegar
  con teclado y mensajes de error junto al campo.
- Responsivo: se ve correctamente a 375 px de ancho, sin desbordamiento
  horizontal.
