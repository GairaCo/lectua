# PLAN · Reposicionamiento "Lee y Actúa"
`2026-07-12-lectua-pilares-plan.md` · Traduce la spec en **pasos ejecutables y verificables**.

## Encabezado · El rumbo

| | |
|---|---|
| **Objetivo** | Landing reposicionada al nuevo modelo (5 pilares + Lectuamigos) publicada en Vercel, costo $0. |
| **Stack** | Mismo stack: HTML/CSS/JS vanilla en `index.html`; sin dependencias nuevas. |
| **Arquitectura** | Reescritura de secciones de contenido reutilizando la estructura y CSS existentes (la línea de tiempo de "Cómo funciona" ahora presenta los 5 pilares). Deploy automático GitHub → Vercel. |
| **Spec** | → `2026-07-12-lectua-pilares-spec.md` |

## Tareas · El ritmo

### Tarea 1 · Nav y hero
- Título "Lectua — Lee y Actúa"; nav con Pilares y CTA "Hazte Lectuamigo".
- Hero: nuevo titular, los dos problemas, tagline y tarjeta Lectuamigos.
- **Verificación**: hero comunica lectura+escritura y la tarjeta dice LECTUAMIGOS.

### Tarea 2 · ¿Qué es? y 5 pilares
- Reescribir "¿Qué es?" (soledad del lector, salto a la escritura, red de apoyo).
- Reemplazar "Cómo funciona" por "Los 5 pilares" con los textos del documento.
- **Verificación**: los 5 nombres exactos aparecen en orden (ME-01).

### Tarea 3 · Beneficios, Lectuamigos y cierre
- Pestañas: lectores / escritores / aliados (ids y JS actualizados).
- CTA "Hazte Lectuamigo" con inclusiones de la membresía; footer con Lectualidad.
- Cita de Alberto Manguel en el manifiesto.
- **Verificación**: pestañas funcionan; cero "Pasaporte"/"Leederos" (ME-02).

### Tarea 4 · Publicar y verificar
- Commits: docs (spec+plan) y feat (index.html) a `main`; Vercel autodespliega.
- **Verificación**: producción cumple ME-01..03; login demo operativo (ME-03).

## Criterio de salida (Publicar)

lectua.vercel.app comunica el nuevo modelo completo y los documentos quedan
versionados en `specs/`.
