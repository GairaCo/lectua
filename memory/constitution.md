# Constitución del proyecto LECTUA

> Documento fundacional del desarrollo dirigido por especificaciones (Spec-Driven Development).
> Toda especificación, plan y tarea de este proyecto debe respetar estos principios.

## Principios

### I. Simplicidad primero
El sitio es HTML5, CSS y JavaScript vanilla en un solo archivo (`index.html`). No se
introducen frameworks, bundlers ni dependencias de build mientras la landing no lo exija.
La única dependencia externa permitida son las fuentes de Google Fonts.

### II. Contenido en español
Todo el contenido visible al usuario, la documentación y los mensajes de commit se
escriben en español. El atributo `lang="es"` es obligatorio en el documento.

### III. Identidad de marca LECTUA
La marca es **LECTUA** (antes LECTOPUS). Paleta oficial en variables CSS: verde bosque
`#1e3a2f`, crema `#f5f0e8`, dorado `#c8a855`. Tipografías: Playfair Display (títulos)
y Lato (cuerpo). Ninguna referencia a la marca anterior puede llegar a producción.

### IV. Responsive y accesible
Todo cambio debe funcionar en móvil (breakpoints 900px y 600px), usar HTML semántico
y mantener contraste legible sobre los fondos verde y crema.

### V. Despliegue continuo y reproducible
La rama `main` en GitHub es la fuente de verdad. Cada push a `main` despliega
automáticamente a Vercel como sitio estático. No hay pasos manuales de build.

## Flujo de trabajo

1. **Especificar** (`specs/NNN-nombre/spec.md`): qué se construye y por qué — sin detalles técnicos.
2. **Planificar** (`plan.md`): cómo se construye — decisiones técnicas alineadas con esta constitución.
3. **Desglosar** (`tasks.md`): tareas pequeñas, verificables y ordenadas.
4. **Implementar**: cada tarea se completa y verifica antes de pasar a la siguiente.

## Gobernanza

Esta constitución prevalece sobre cualquier otra práctica. Cualquier cambio a estos
principios debe documentarse aquí con fecha y justificación.

**Versión**: 1.0.0 · **Ratificada**: 2026-07-11
