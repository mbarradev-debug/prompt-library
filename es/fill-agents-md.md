---
title: Llenar AGENTS.md y CLAUDE.md en un repo existente
tool: Claude Code (sirve con cualquier agente de código)
use-when: Un repo todavía no tiene instrucciones para agentes, o están vacías o desactualizadas
requires: Un repo con código
tags: [agents-md, claude-md, onboarding, conventions]
---

Mi proyecto no tiene contenido en AGENTS.md ni en CLAUDE.md. Quiero llenarlos para que cualquier agente que trabaje en este repo entienda el proyecto y siga mis reglas sin que tenga que repetirlas en cada prompt.

## Cómo hacerlo
1. Primero explora el repo (manifiesto de paquetes, estructura de carpetas, configuración de TypeScript, lint y formateo, dónde vive el contenido y los datos, carpetas de referencia o documentación, README) para sacar los datos reales: versiones, comandos y rutas. No inventes nada. Si algo no lo puedes confirmar, déjalo como pregunta al final.
2. Escribe todo el contenido en `AGENTS.md`, en inglés.
3. Deja `CLAUDE.md` solo con la línea `@AGENTS.md`, para que Claude Code lo importe sin duplicar contenido.
4. Muéstrame el borrador completo y espera mi OK antes de guardarlo.

## Qué debe incluir AGENTS.md
Solo lo que un agente no puede deducir leyendo el código. Nada que ya diga el README. Máximo unas 150 líneas, con secciones cortas y listas.

- **Project overview**: qué es el proyecto y para quién, en dos o tres líneas.
- **Stack y versiones reales**, más los comandos de desarrollo, build, lint y test.
- **Estructura**: qué va en cada carpeta principal y dónde viven el contenido, la configuración y los componentes compartidos.
- **Reglas de diseño**: qué decisiones visuales son fijas (colores, tipografía, espaciado, referencias) y dónde están definidos los tokens del tema. No se inventa contenido: los placeholders se mantienen hasta que yo entregue el material real.
- **Carpetas de solo lectura**: [CARPETAS_SOLO_LECTURA, por ejemplo references/, vendor/]. Nunca se modifican y quedan fuera del build, del chequeo de tipos y del lint.
- **Idiomas**: [IDIOMA_CONTENIDO] para el contenido del producto; inglés para código, comentarios, commits, README e issues.
- **Accesibilidad y movimiento**: contraste AA, áreas táctiles de al menos 44px, `aria-label` en botones de solo ícono, `prefers-reduced-motion` respetado y sin scroll horizontal en 360px. Ajusta a lo que aplique en este proyecto.
- **Forma de trabajo**:
  - Antes de editar, mostrar un plan corto y esperar mi OK.
  - El trabajo se rastrea en [GESTOR_ISSUES, por ejemplo el proyecto "[NOMBRE_PROYECTO]" de Linear], con una rama por issue.
  - Nunca hacer commit, push ni merge sin que yo lo pida.
  - Correr lint y build antes de dar una tarea por terminada.
- **Skills por tipo de tarea**: qué skill instalada usar para cada tipo de trabajo (por ejemplo reglas de UI/UX, pulido visual, auditoría de calidad, de issue a PR). Lista solo las skills que existen en este entorno.
- **Decisiones pendientes**: preguntas abiertas que el agente no debe resolver por su cuenta.

## Al final
Dame una lista breve de lo que no pudiste confirmar en el repo, para completarlo yo.
