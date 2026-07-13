# PLAN · Fase "Eventos freemium → premium"
`2026-07-12-fase-eventos-plan.md` · Integra las 3 specs de la fase en **pasos ejecutables y verificables**.

## Encabezado · El rumbo

| | |
|---|---|
| **Objetivo** | Validar la propuesta de valor en 2-3 meses: qué eventos y qué beneficios debe tener el Pasaporte, cobrando eventos premium a la mayor brevedad. Costo $0. |
| **Stack** | Mismo stack (HTML/CSS/JS en `index.html`) + Luma como operador de eventos. |
| **Arquitectura** | Zona de eventos con gate por sesión (login demo) → catálogo freemium/premium → inscripción y cobro en Luma / link de pago. Deploy GitHub → Vercel. |
| **Specs** | → `2026-07-12-registro-acceso-spec.md` · `2026-07-12-eventos-catalogo-spec.md` · `2026-07-12-identidad-limpia-spec.md` |

## Tareas · El ritmo

### Tarea 1 · Identidad limpia (spec C)
- Reemplazar logo pulpo por libro abierto; eliminar todos los 🐙.
- **Verificación**: ME-C1 y ME-C2.

### Tarea 2 · Gate de registro (spec A)
- Sección "Eventos" con teaser bloqueado + botón que abre el registro; revelar/ocultar
  según sesión sin recargar; enlace en el nav.
- **Verificación**: ME-A1 y ME-A2.

### Tarea 3 · Catálogo de eventos (spec B)
- 3 eventos freemium + 3 premium con fechas, lugares, precios orientativos y CTAs a Luma.
- **Verificación**: ME-B1 y ME-B2.

### Tarea 4 · Publicar y probar
- Commits docs + feat a `main`; prueba en producción del flujo completo:
  visitante → no ve agenda → se registra → ve agenda → clic en evento.
- **Verificación**: todas las ME de las 3 specs en lectua.vercel.app.

### Tarea 5 · Operación (fuera del código)
- Crear los 6 eventos en Luma y reemplazar los enlaces marcadores.
- Conectar link de pago (Bold/Wompi/Mercado Pago) a los eventos premium.
- En cada evento freemium: encuesta de salida + oferta premium (instrumento de validación).

## Criterio de salida (Publicar)

La fase queda publicada cuando un visitante puede registrarse, ver ambas categorías,
e inscribirse a un evento; y el equipo puede medir registro → inscripción → asistencia
→ compra premium.
