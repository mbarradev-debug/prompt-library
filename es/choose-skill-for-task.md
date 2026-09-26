---
title: Elegir la mejor skill instalada para una tarea (solo lectura)
tool: Claude Code
use-when: Vas a empezar un tipo de trabajo y no sabes cuál de tus skills instaladas encaja mejor
requires: Skills instaladas a nivel de usuario, proyecto o plugin
tags: [skills, planning, read-only]
---

Tarea de solo lectura: no modifiques, crees ni borres ningún archivo, no instales nada y no ejecutes skills. Solo analiza y recomienda.

## Contexto
Estoy trabajando en [DESCRIPCION_PROYECTO, por ejemplo un sitio en Next.js con Chakra UI]. Voy a trabajar en [AREA_TAREA, por ejemplo micro interacciones y animaciones]. En concreto:
- [NECESIDAD_1]
- [NECESIDAD_2]
- [NECESIDAD_3]

## Qué necesito
1. Lista todas las skills disponibles: las de usuario (`~/.claude/skills`), las del proyecto (`.claude/skills`) y las de plugins instalados. Lee el SKILL.md de las que tengan relación con [AREA_TAREA], no solo su descripción.
2. Evalúa cuáles sirven realmente para este trabajo, según lo que cada skill cubre de verdad y no por su nombre.
3. Recomienda la mejor opción, o una combinación si ninguna cubre todo, y en qué orden usarlas.

## Formato de respuesta
- Tabla con las skills relevantes: nombre, qué cubre de esta tarea, qué no cubre y qué tan adecuada es para este caso (alta, media o baja).
- Recomendación final en 2 o 3 frases, con el motivo.
- Vacíos: qué necesidades de la lista no cubre ninguna skill.
- Cómo invocar la skill recomendada, con un ejemplo de prompt concreto para este proyecto.
