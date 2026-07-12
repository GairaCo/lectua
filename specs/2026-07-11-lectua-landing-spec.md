# SPEC · Landing LECTUA
`2026-07-11-lectua-landing-spec.md` · Define **qué** se quiere lograr y para quién — no el cómo.

## Overview

Landing page pública de **LECTUA**, comunidad de lectura que conecta lectores, cafés de
especialidad (*Leederos*) y librerías independientes. El producto central es el
**Pasaporte LECTUA**: un documento físico coleccionable que sella cada experiencia.
La página debe presentar la propuesta de valor, explicar el funcionamiento y convertir
visitantes en interesados en el Pasaporte. Nace de un rebrand: el mockup original era
LECTOPUS y la marca final es LECTUA.

## Usuarios objetivo

- **Lectores** que buscan comunidad, experiencias y beneficios en cafés y librerías.
- **Dueños de Leederos (cafés)** que evalúan aliarse para atraer clientes lectores.
- **Librerías independientes** que buscan visibilidad y eventos con lectores.

## Alcance v1

**Incluye:**
- Página única en español con: nav fijo, hero con pasaporte animado, ¿qué es?,
  cómo funciona (5 pasos), los 4 ciclos de lectura (metodología Borges), beneficios
  por audiencia (3 pestañas), CTA del Pasaporte, manifiesto y footer.
- Rebrand total: cero menciones de LECTOPUS; enlaces a `lectua.com` y `@somoslectua`.
- Responsive: escritorio, tablet (≤900px) y móvil (≤600px).
- Publicada en Vercel (plan gratuito) con repo público en GitHub.

**Queda fuera:**
- Registro real de usuarios, login o pagos.
- Backend, base de datos o CMS.
- Múltiples páginas/rutas o versión en otros idiomas.

## Comportamiento

- La navegación interna usa anclas con scroll suave; el CTA "Obtén tu Pasaporte" está
  siempre visible en el nav fijo.
- Las pestañas de beneficios alternan lectores / Leederos / librerías sin recargar.
- Tarjetas, pasos y beneficios aparecen con animación al entrar en el viewport.
- La tarjeta del pasaporte flota con animación continua en el hero.

## Errores y seguridad

- Sin JavaScript la página degrada con gracia: todo el contenido es visible; solo se
  pierden pestañas y animaciones (la primera pestaña queda activa por defecto).
- Sin formularios ni datos de usuario: no se captura información personal.
- Enlaces externos con `target="_blank"`; únicas dependencias externas: Google Fonts.

## Futuro (v2+)

- Formulario real de registro al Pasaporte.
- Mapa interactivo de Leederos y librerías aliadas por ciudad.
- Dominio propio `lectua.com` apuntando al despliegue de Vercel.
- Analítica de visitas y SEO (metadatos Open Graph, sitemap).
