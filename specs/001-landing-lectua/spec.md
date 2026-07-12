# Especificación: Landing page LECTUA

**Rama**: `001-landing-lectua` · **Estado**: Implementada · **Fecha**: 2026-07-11

## Resumen

Landing page pública de LECTUA, comunidad de lectura que conecta lectores, cafés de
especialidad ("Leederos") y librerías independientes alrededor de un producto central:
el **Pasaporte LECTUA**, un documento físico coleccionable que sella cada experiencia.

## Historias de usuario

### HU-1 · Visitante conoce LECTUA (prioridad P1)
Como visitante que llega por primera vez, quiero entender en menos de 10 segundos qué
es LECTUA y qué gano al unirme, para decidir si obtengo mi Pasaporte.

**Criterios de aceptación**
1. Al cargar la página, el hero muestra la marca, el lema "Lee. Conecta. Viaja.
   Transfórmate." y un CTA visible "Obtén tu Pasaporte".
2. La sección "¿Qué es?" explica los 4 pilares: comunidad, Leederos, librerías y experiencias.

### HU-2 · Visitante entiende el funcionamiento (P1)
Como lector interesado, quiero ver los pasos concretos para participar, para saber qué
esperar antes de registrarme.

**Criterios de aceptación**
1. La sección "Cómo funciona" presenta 5 pasos numerados en orden.
2. La sección "Los 4 ciclos" presenta la metodología (El Asedio, El Viaje, La Búsqueda,
   El Sacrificio) basada en las cuatro tramas de Borges.

### HU-3 · Cada audiencia ve sus beneficios (P2)
Como lector, dueño de café o librero, quiero ver los beneficios específicos para mí,
para evaluar si me conviene aliarme.

**Criterios de aceptación**
1. La sección "Beneficios" tiene 3 pestañas: lectores, Leederos y librerías.
2. Al pulsar una pestaña se muestran solo sus 6 beneficios, sin recargar la página.

### HU-4 · Visitante convertido actúa (P1)
Como visitante convencido, quiero un llamado a la acción claro, para obtener mi
Pasaporte o seguir a la comunidad.

**Criterios de aceptación**
1. La sección CTA lista lo que incluye el Pasaporte (6 ítems) y enlaza a lectua.com
   y al Instagram @somoslectua.
2. El nav fijo mantiene el CTA visible durante todo el scroll.

## Requisitos funcionales

- **RF-01**: Página única con nav fijo, hero, ¿qué es?, cómo funciona, 4 ciclos, beneficios, CTA pasaporte, manifiesto y footer.
- **RF-02**: Navegación interna por anclas con scroll suave.
- **RF-03**: Pestañas de beneficios interactivas sin recarga.
- **RF-04**: Animaciones de entrada al hacer scroll (aparición progresiva de tarjetas y pasos).
- **RF-05**: Tarjeta de Pasaporte animada (flotación) en el hero con sellos de ejemplo.
- **RF-06**: Diseño responsive: escritorio, tablet (≤900px) y móvil (≤600px).
- **RF-07**: Todo el contenido en español y bajo la marca LECTUA (cero menciones a LECTOPUS).

## Fuera de alcance

- Registro real de usuarios, autenticación o pasarela de pago.
- Backend, base de datos o CMS.
- Múltiples páginas o rutas.

## Métricas de éxito

- **ME-01**: La página carga y es interactiva sin errores de consola.
- **ME-02**: 100% de las secciones visibles y funcionales en móvil de 360px de ancho.
- **ME-03**: Búsqueda de "lectopus" (sin distinción de mayúsculas) devuelve 0 resultados.
