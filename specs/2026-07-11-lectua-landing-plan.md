# PLAN · Landing LECTUA
`2026-07-11-lectua-landing-plan.md` · Traduce la spec en **pasos ejecutables y verificables**.

## Encabezado · El rumbo

| | |
|---|---|
| **Objetivo** | Publicar la landing LECTUA (rebrand de LECTOPUS) en Vercel con repo en GitHub, costo $0. |
| **Stack** | HTML5 · CSS3 · JavaScript vanilla · Google Fonts. Sin build ni dependencias. |
| **Arquitectura** | Un solo `index.html` estático · GitHub (repo público `lectua`) · Vercel Hobby (deploy automático desde `main`). |
| **Spec** | → `2026-07-11-lectua-landing-spec.md` |

## Tareas · El ritmo

Cada tarea sigue el ciclo: **ejecutar → verificar contra la spec → cumple ✓ / no cumple → volver con el fix → commit**.

### Tarea 1 · Rebrand LECTOPUS → LECTUA
- Reemplazo con preservación de mayúsculas (LECTUA / Lectua / lectua) en título, nav,
  hero, pasaporte, copy, manifiesto, footer y enlaces externos.
- **Verificación**: búsqueda case-insensitive de "lectopus" devuelve 0 resultados.

### Tarea 2 · Documentación SDD
- Generar spec y plan con la anatomía del curso + README que explica el flujo.
- **Verificación**: el repo contiene `specs/` con ambos artefactos fechados.

### Tarea 3 · Repositorio git
- `git init`, commits en español separando docs (spec/plan) de código (landing).
- **Verificación**: `git log` muestra historial limpio en rama `main`.

### Tarea 4 · Publicar repo en GitHub (gratis)
- Crear repo público `lectua` y subir archivos. Plan free de GitHub: $0.
- **Verificación**: `github.com/<usuario>/lectua` accesible con todos los archivos.

### Tarea 5 · Desplegar en Vercel (gratis)
- Importar el repo en Vercel, preset "Other", sin build command ni output directory.
  Plan Hobby: $0 para proyectos personales.
- **Verificación**: la URL `*.vercel.app` carga la landing.

### Tarea 6 · Verificación final en producción
- La página carga sin errores de consola; pestañas y animaciones funcionan;
  responsive correcto a 900px y 600px; ME: 0 menciones de la marca anterior.
- **Verificación**: revisión visual + búsqueda en el HTML servido en producción.

## Criterio de salida (Publicar)

El paso 7 del flujo se considera cumplido cuando la URL pública de Vercel muestra la
landing LECTUA completa y el repo GitHub queda como fuente de verdad conectada al deploy.
