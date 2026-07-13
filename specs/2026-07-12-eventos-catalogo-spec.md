# SPEC · Catálogo de eventos freemium y premium
`2026-07-12-eventos-catalogo-spec.md` · Define **qué** se quiere lograr y para quién — no el cómo.

## Overview

Dentro de la zona registrada, la agenda presenta dos categorías claramente
diferenciadas: **Freemium** (eventos gratuitos que hacen vivir la experiencia Lectua)
y **Premium** (eventos pagos de cupo limitado). Los freemium alimentan el embudo y en
ellos se promueven los premium. La operación (inscripción, recordatorios, aforo) se
gestiona en **Luma**; cada tarjeta enlaza a su evento en Luma. El objetivo de los
próximos 2-3 meses es validar qué tipos de evento y qué beneficios debe tener el
Pasaporte para su venta.

## Usuarios objetivo

- **Miembros registrados** que quieren asistir a su primer evento gratuito.
- **Asistentes freemium** listos para dar el paso a un evento pago.

## Alcance v1

**Incluye:**
- Categoría **Freemium** con 3 eventos: Lectuante de estreno, Taller relámpago
  "Tu primera página" y Micrófono abierto Lectube.
- Categoría **Premium** con 3 eventos: Cena literaria con autor invitado, Ciclo
  completo "El Viaje" (4 sesiones) y Lectour de día completo.
- Cada tarjeta: fecha, nombre, descripción, lugar/cupo, precio (premium) y botón de
  inscripción hacia Luma. Los precios son orientativos y editables.
- Distinción visual: insignia verde (freemium) e insignia dorada (premium).

**Queda fuera:**
- Cobro dentro del sitio (el pago vive en Luma o en link de pago externo).
- Gestión dinámica de eventos (CMS); en v1 se editan en el HTML.

## Comportamiento

- Los botones freemium dicen "Reservar gratis"; los premium "Comprar mi cupo" y
  muestran precio.
- Los enlaces abren Luma en pestaña nueva. Mientras se crean los eventos reales en
  Luma, apuntan a la página de la comunidad (lu.ma/lectua) como marcador.

## Errores y seguridad

- Sin JavaScript la sección permanece bloqueada (no se filtra la agenda).
- Fechas y precios revisados antes de cada publicación (fuente de verdad: Luma).

## Futuro (v2+)

- Calendario embebido de Luma; sellos digitales por asistencia; paquetes de eventos
  dentro del Pasaporte según lo aprendido en la validación.

## Métricas de éxito

- ME-B1: las 2 categorías con 3 eventos cada una se muestran a usuarios con sesión.
- ME-B2: cada evento tiene fecha, lugar y CTA; los premium muestran precio.
