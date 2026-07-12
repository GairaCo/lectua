# Plan de implementación: Landing page LECTUA

**Especificación**: `spec.md` · **Constitución**: v1.0.0

## Contexto técnico

| Aspecto | Decisión |
|---|---|
| Lenguaje | HTML5 + CSS3 + JavaScript vanilla (ES6) |
| Estructura | Un solo archivo `index.html` (estilos y scripts embebidos) |
| Dependencias | Solo Google Fonts (Playfair Display, Lato) |
| Hosting | Vercel, sitio estático sin build |
| Repositorio | GitHub `lectua`, rama `main` |
| Pruebas | Verificación manual + revisión responsive |

## Verificación contra la constitución

- ✅ I. Simplicidad: un solo archivo, sin frameworks ni build.
- ✅ II. Español: contenido, docs y commits en español.
- ✅ III. Marca: variables CSS con la paleta oficial; rebrand completo a LECTUA.
- ✅ IV. Responsive: media queries a 900px y 600px; HTML semántico (nav/section/footer).
- ✅ V. Despliegue: Vercel conectado a `main` en GitHub.

## Diseño técnico

### Estructura del documento
1. `<nav>` fijo — logo SVG (pulpo + libro), enlaces ancla, CTA.
2. `.hero` — grid 2 columnas: texto + tarjeta pasaporte animada (`@keyframes float`).
3. `.que-es` — grid 2x2 de tarjetas + bloque de cita.
4. `.como-funciona` — 5 pasos con línea de tiempo vertical (pseudo-elemento `::after`).
5. `.ciclos` — grid de 4 tarjetas sobre fondo verde.
6. `.beneficios` — pestañas con `showTab()` que alterna clases `.active`.
7. `.pasaporte-cta` — lista de inclusiones + botones a lectua.com e Instagram.
8. `.por-que` + `<footer>` — manifiesto y cierre.

### Interactividad (JS)
- `showTab(tab)`: alterna visibilidad de los 3 paneles de beneficios.
- `IntersectionObserver` (threshold 0.1): revela `.feature-card`, `.ciclo-card`, `.step`
  y `.benefit-item` con transición de opacidad y translateY.
- Scroll suave nativo vía `scroll-behavior: smooth`.

### Theming
Variables CSS en `:root` (verde, verde-medio, verde-claro, crema, crema-oscura, dorado,
café, texto, blanco) — cualquier ajuste de marca se hace en un solo lugar.

## Despliegue

1. Repo GitHub `lectua` con `index.html` en la raíz.
2. Importar en Vercel como proyecto estático (framework preset: *Other*, sin build command).
3. Cada push a `main` genera despliegue automático de producción.
