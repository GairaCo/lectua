# SPEC · Login LECTUA (v1 demo)
`2026-07-11-lectua-login-spec.md` · Define **qué** se quiere lograr y para quién — no el cómo.

## Overview

Añadir inicio de sesión a la landing LECTUA para que los visitantes puedan crear una
cuenta y entrar con su nombre visible en la navegación. En v1 es una **demo funcional
del lado del cliente**: los datos se guardan únicamente en el navegador del usuario
(localStorage), sin backend y sin costo. Sirve para validar el flujo y la interfaz
antes de invertir en autenticación real (v2).

## Usuarios objetivo

- **Lectores interesados** que quieren "unirse" a LECTUA desde la landing.
- **El equipo LECTUA**, que necesita validar la experiencia de registro/login sin pagar
  infraestructura todavía.

## Alcance v1

**Incluye:**
- Enlace "Entrar" en la barra de navegación.
- Modal con dos pestañas: **Crear cuenta** (nombre, correo, contraseña) e
  **Iniciar sesión** (correo, contraseña).
- Sesión persistente en el navegador: al entrar, el nav muestra "Hola, {nombre}" y
  la opción "Salir".
- Validaciones: correo con formato válido, contraseña mínima de 6 caracteres,
  correo no duplicado al registrarse, credenciales correctas al entrar.
- Aviso visible de que es una demo local.

**Queda fuera:**
- Backend, base de datos o API de autenticación.
- Recuperación de contraseña, verificación de correo, OAuth (Google).
- Compartir sesión entre dispositivos o navegadores.

## Comportamiento

- "Entrar" abre el modal; la X, el fondo oscuro o registrarse con éxito lo cierran/cambian.
- Registro exitoso muestra confirmación y lleva a la pestaña de inicio de sesión.
- Login correcto cierra el modal y actualiza el nav con el saludo y "Salir".
- "Salir" borra la sesión y restaura el enlace "Entrar".
- La sesión sobrevive a recargas de página (mismo navegador).

## Errores y seguridad

- Mensajes de error claros en el modal: correo inválido, contraseña corta, correo ya
  registrado, credenciales incorrectas. Nunca fallos silenciosos.
- La contraseña **no se guarda en texto plano**: se almacena un hash SHA-256.
- El nombre del usuario se escapa antes de insertarse en el DOM (previene XSS).
- Limitación explícita v1: localStorage no es un mecanismo seguro de producción;
  cualquier dato es local al navegador y se pierde al limpiar datos del sitio.

## Futuro (v2+)

- Autenticación real con proveedor gratuito (p. ej. Supabase Auth o Firebase Auth).
- Inicio de sesión con Google.
- Perfil del lector: ciudad, ciclo favorito, sellos del Pasaporte digital.
