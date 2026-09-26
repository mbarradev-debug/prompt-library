---
title: Auditar con skills y registrar los hallazgos en pocas issues de Linear
tool: Claude Code con el MCP de Linear conectado
use-when: Antes de un trabajo grande quieres auditar el estado actual y dejar trazabilidad en Linear sin llenarlo de issues pequeñas
requires: MCP de Linear, las skills con las que quieres auditar
tags: [linear, audit, planning, traceability]
---

Quiero trazabilidad en Linear del trabajo de [AREA_TRABAJO, por ejemplo animaciones y micro interacciones] de este proyecto. Son dos fases. No modifiques código en ninguna de las dos.

## Fase 1: Auditoría (solo lectura)
Audita el estado actual del proyecto con estas skills, en este orden:
1. /[SKILL_1]: [QUÉ_REVISAR_CON_ELLA]
2. /[SKILL_2]: [QUÉ_REVISAR_CON_ELLA] (solo en modo crítica, sin aplicar cambios)
3. /[SKILL_3]: [QUÉ_REVISAR_CON_ELLA]

Para cada hallazgo indica el archivo afectado, el problema en una línea y la solución propuesta. Incluye también estos vacíos conocidos que ninguna skill cubre: [VACIOS_CONOCIDOS, o borra esta línea].

Al terminar, muéstrame un resumen de los hallazgos agrupados en máximo [MAX_ISSUES, por ejemplo 3] temas y espera mi OK antes de tocar Linear.

## Fase 2: Linear
Con mi OK, usa el MCP de Linear directamente. No uses skills de planificación que generan muchas issues.

1. Busca el proyecto "[PROYECTO_LINEAR]". Si no existe, créalo con una descripción corta en inglés.
2. Crea como máximo [MAX_ISSUES] issues, agrupando los hallazgos en vez de hacer una issue por cada uno. Usa los temas del resumen de la auditoría que aprobé.
3. Cada issue va en inglés, con esta estructura en la descripción:
   - Context: una o dos líneas
   - Findings: lista de hallazgos con su archivo
   - Scope: qué se va a hacer
   - Acceptance criteria: checklist verificable
   - Skill to use: cuál aplicar al implementarla
   - Suggested branch: nombre de rama
4. Si hay decisiones que me corresponden a mí (por ejemplo dos skills o referencias que recomiendan valores en conflicto), déjalas registradas en la issue que corresponda como decisión pendiente. No las resuelvas.
5. Agrega labels simples y prioridad, y marca las dependencias entre issues en el orden en que deben hacerse.

Al terminar, dame la lista de issues creadas con su identificador y título. No empieces a implementar ninguna.
