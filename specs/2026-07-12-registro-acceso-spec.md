# SPEC · Acceso por registro a la zona de eventos
`2026-07-12-registro-acceso-spec.md` · Define **qué** se quiere lograr y para quién — no el cómo.

## Overview

La agenda de eventos de Lectua (freemium y premium) solo es visible para usuarios
registrados en el sitio. El registro gratuito es la puerta de entrada al embudo:
convierte visitantes anónimos en miembros identificados de la comunidad, que luego
reciben la oferta premium. Se reutiliza el login demo existente (v1, localStorage).

## Usuarios objetivo

- **Visitantes nuevos**: ven un aviso claro de que la agenda existe y se desbloquea gratis.
- **Miembros registrados**: ven la agenda completa con ambas categorías.
- **El equipo Lectua**: cada registro es un lead para validar la propuesta de valor.

## Alcance v1

**Incluye:**
- Sección "Eventos" en la landing con dos estados: bloqueado (teaser + botón
  "Registrarme gratis" que abre el modal de registro) y desbloqueado (agenda completa).
- El estado responde a la sesión existente: al iniciar sesión se revela la agenda al
  instante y al cerrar sesión se vuelve a bloquear.
- Enlace "Eventos" en la navegación.

**Queda fuera:**
- Verificación de correo, backend o protección real del contenido (v1 es validación).
- Sincronización de registros con una base de datos externa.

## Comportamiento

- Sin sesión: la sección muestra el teaser; ningún evento es visible.
- Con sesión (registro o login): el teaser desaparece y aparece la agenda.
- Recargar la página conserva el estado según la sesión guardada.

## Errores y seguridad

- v1 protege la visibilidad, no el contenido (está en el HTML): suficiente para
  validar el embudo, documentado como limitación.
- Los mensajes de error del registro/login existentes no cambian.

## Futuro (v2+)

- Autenticación real (Supabase/Firebase) y lista de miembros exportable.
- Sincronización del registro web con el CRM/email marketing.

## Métricas de éxito

- ME-A1: sin sesión, ningún nombre de evento aparece en pantalla.
- ME-A2: tras registrarse, la agenda se ve sin recargar la página.
