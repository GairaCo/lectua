# PLAN · Migración a Supabase Auth
`2026-07-12-auth-supabase-plan.md` · Traduce la spec en **pasos ejecutables y verificables**.

## Encabezado · El rumbo

| | |
|---|---|
| **Objetivo** | Registros reales en base de datos consultable, costo $0, sin romper la experiencia actual. |
| **Stack** | supabase-js v2 (CDN) + Supabase Auth (proyecto `lectua`, plan gratuito). |
| **Arquitectura** | El sitio estático conversa directo con Supabase Auth usando la publishable key. Sin servidor propio. |
| **Spec** | → `2026-07-12-auth-supabase-spec.md` |

## Tareas · El ritmo

### Tarea 1 · Infraestructura (hecha en el panel)
- Organización y proyecto `lectua` creados (plan Free, región América).
- "Confirm email" desactivado; registro de usuarios habilitado.
- **Verificación**: panel muestra proyecto activo y ajustes guardados. ✓

### Tarea 2 · Migrar el código de auth
- Cargar supabase-js por CDN; crear cliente con URL + publishable key.
- `doRegister` → `signUp` (nombre como metadato); `doLogin` → `signInWithPassword`;
  `logout` → `signOut`; `renderSession` → `getSession` + `onAuthStateChange`.
- Conservar validaciones y mensajes en español; traducir errores del proveedor.
- **Verificación**: sintaxis válida y flujo completo en local.

### Tarea 3 · Gobernanza
- Enmendar `memory/constitution.md` a v1.1.0 (segunda dependencia permitida).
- **Verificación**: constitución actualizada con fecha y justificación.

### Tarea 4 · Publicar y probar en producción
- Commits docs + feat; deploy automático de Vercel.
- Registrar usuario de prueba en lectua.vercel.app y comprobar ME-S1..S3,
  incluida su aparición en Authentication → Users del panel.

## Criterio de salida (Publicar)

Un registro hecho por cualquier visitante queda en la base de datos de Supabase y
el equipo puede verlo/exportarlo desde el panel.
