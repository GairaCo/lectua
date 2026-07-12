# PLAN · Login LECTUA (v1 demo)
`2026-07-11-lectua-login-plan.md` · Traduce la spec en **pasos ejecutables y verificables**.

## Encabezado · El rumbo

| | |
|---|---|
| **Objetivo** | Login demo funcional en la landing publicada, en <5 min y costo $0. |
| **Stack** | JavaScript vanilla + Web Crypto API (SHA-256) + localStorage. Sin dependencias nuevas. |
| **Arquitectura** | Todo dentro de `index.html` (CSS del modal + HTML del modal + JS de auth). Deploy automático GitHub → Vercel. |
| **Spec** | → `2026-07-11-lectua-login-spec.md` |

## Tareas · El ritmo

Cada tarea: **ejecutar → verificar contra la spec → cumple ✓ / no cumple → fix → commit**.

### Tarea 1 · UI del modal
- CSS del modal (overlay, tarjeta, pestañas, campos, mensajes) con la paleta LECTUA.
- HTML: enlace "Entrar" en el nav + modal con formularios de registro e inicio.
- **Verificación**: el modal abre/cierra y respeta la identidad visual (constitución III).

### Tarea 2 · Lógica de registro
- Validar nombre, formato de correo y contraseña ≥6; rechazar correo duplicado.
- Guardar usuario con hash SHA-256 de la contraseña en `localStorage['lectua_users']`.
- **Verificación**: registro duplicado y contraseña corta muestran error; éxito muestra confirmación.

### Tarea 3 · Lógica de sesión
- Login compara hash; guarda `lectua_session`; nav muestra "Hola, {nombre}" + "Salir".
- Nombre escapado antes de insertar en el DOM; sesión persiste al recargar.
- **Verificación**: credenciales malas → error; buenas → saludo en nav; "Salir" restaura "Entrar".

### Tarea 4 · Publicar y verificar en producción
- Commit de specs + `index.html` a `main`; Vercel autodespliega.
- **Verificación**: lectua.vercel.app muestra "Entrar" y el flujo completo funciona.

## Criterio de salida (Publicar)

El login demo funciona en producción con todas las validaciones de la spec y los
documentos spec/plan quedan versionados en `specs/`.
