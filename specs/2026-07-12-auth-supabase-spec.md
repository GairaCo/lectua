# SPEC · Autenticación real con Supabase
`2026-07-12-auth-supabase-spec.md` · Define **qué** se quiere lograr y para quién — no el cómo.

## Overview

Migrar el login demo (localStorage) a **autenticación real con Supabase** (plan
gratuito). A partir de esta fase, cada registro queda guardado en una base de datos
que el equipo Lectua puede consultar: los registros dejan de vivir solo en el
navegador del visitante y se convierten en la lista real de miembros de la comunidad.
El gate de eventos pasa a apoyarse en sesiones verificadas por servidor.

## Usuarios objetivo

- **Visitantes** que se registran para ver la agenda: su cuenta ahora existe de verdad
  y funciona desde cualquier navegador.
- **El equipo Lectua**: ve y exporta la lista de miembros desde el panel de Supabase
  (Authentication → Users) para hacer seguimiento y marketing.

## Alcance v1

**Incluye:**
- Registro con nombre, correo y contraseña → usuario creado en Supabase Auth
  (el nombre viaja como metadato del usuario).
- Inicio de sesión con correo/contraseña contra Supabase; cierre de sesión.
- Sesión persistente entre recargas y días (token gestionado por supabase-js).
- Confirmación por correo desactivada en esta fase: el registro es inmediato.
- El mismo modal y los mismos mensajes de error en español.
- El gate de eventos responde a la sesión de Supabase.

**Queda fuera:**
- Recuperación de contraseña y login con Google (siguiente iteración).
- Verificación de correo (se activará cuando haya plantillas en español).
- Tablas adicionales (perfiles, inscripciones): esta fase cubre solo identidad.

## Comportamiento

- Registro exitoso → confirmación y paso a "Iniciar sesión".
- Correo ya registrado → error claro "Ese correo ya tiene cuenta".
- Login correcto → saludo con el nombre en el nav + agenda visible.
- La cuenta funciona en cualquier navegador/dispositivo (ya no es local).

## Errores y seguridad

- La clave usada en el sitio es la **publishable key** de Supabase: pública por
  diseño, solo permite lo que las políticas del proyecto autorizan.
- Las contraseñas las gestiona Supabase (hash bcrypt en servidor); el sitio nunca
  las almacena.
- Los mensajes de error del proveedor se traducen a español antes de mostrarse.
- Nota de gobernanza: la constitución se enmienda (v1.1.0) para permitir
  supabase-js como segunda dependencia externa.

## Futuro (v2+)

- Login con Google · recuperación de contraseña · verificación de correo.
- Tabla `perfiles` (ciudad, ciclo favorito) y tabla `inscripciones` a eventos.
- Emails de bienvenida automáticos.

## Métricas de éxito

- ME-S1: un registro hecho en producción aparece en Supabase → Authentication → Users.
- ME-S2: login/logout funcionan y el gate de eventos responde a la sesión real.
- ME-S3: la sesión sobrevive a recargar la página.
