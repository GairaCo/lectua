# LECTUA - Lee. Conecta. Comparte. Actúa.

Landing page de **LECTUA**, comunidad de lectura que conecta lectores, cafés de
especialidad (*Leederos*) y librerías independientes a través del **Pasaporte LECTUA**,
un documento físico coleccionable que sella cada experiencia vivida.

**Stack**: HTML5 + CSS3 + JavaScript vanilla · sin build · **Hosting**: Vercel (gratis) · **Repo**: GitHub (gratis)

## Metodología: Spec-Driven Development

> *Defines qué construir **antes** de ejecutar — y verificas contra ello.*

Este proyecto sigue el flujo de 7 pasos del desarrollo dirigido por especificaciones:

```
1 Feature → 2 Aclarar la idea → 3 Spec del usuario → 4 Plan → 5 Ejecutar → 6 Verificar → 7 Publicar
                                                                    ↑__ no cumple → vuelve con el fix __|
```

### Artefactos

| Artefacto | Archivo | Qué define |
|---|---|---|
| **SPEC** | [`specs/2026-07-11-lectua-landing-spec.md`](specs/2026-07-11-lectua-landing-spec.md) | **Qué** se quiere lograr y para quién — no el cómo. Overview, usuarios objetivo, alcance v1, comportamiento, errores y seguridad, futuro (v2+). |
| **PLAN** | [`specs/2026-07-11-lectua-landing-plan.md`](specs/2026-07-11-lectua-landing-plan.md) | Traduce la spec en pasos ejecutables y verificables: objetivo, stack, arquitectura y tareas con su ciclo ejecutar → verificar → commit. |

Además, `specs/001-landing-lectua/` y `memory/constitution.md` contienen la versión
extendida de la documentación (estilo GitHub Spec Kit): constitución del proyecto,
historias de usuario con criterios de aceptación y desglose de tareas.

## Ejecutar en local

No hay build ni dependencias:

```bash
open index.html        # o doble clic
npx serve .            # o con servidor local
```

## Despliegue (costo $0)

- **GitHub**: repo público en el plan free.
- **Vercel**: plan Hobby, preset "Other", sin build command. Cada push a `main`
  publica automáticamente a producción.

## Secciones de la landing

Nav fijo · Hero con pasaporte animado · ¿Qué es? · Cómo funciona (5 pasos) ·
Los 4 ciclos de lectura (metodología Borges) · Beneficios por audiencia (tabs) ·
CTA Pasaporte · Manifiesto · Footer.

---
© 2025 Lectua · Proyecto del reto Claude — Día 4
