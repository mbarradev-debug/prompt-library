---
title: Reescribir el borrador de un período de la historia de un juego narrativo, listo para llevarlo a Ink
tool: Claude o cualquier asistente de escritura
use-when: Escribes la historia de un juego narrativo por períodos (un año, capítulo o etapa por chat) y quieres pulir el borrador de uno sin que se mezcle con los demás
requires: El borrador del período adjunto, con el período y la edad del protagonista indicados en el archivo
tags: [writing, narrative, game-design, ink]
---

Te adjunto el borrador de un período específico de la historia de mi videojuego. El período ([UNIDAD, por ejemplo año, capítulo o etapa]) y la edad del protagonista están indicados en el archivo.

## Contexto del juego
- Género y estilo: [GENERO_Y_ESTILO, por ejemplo RPG en pixel art de 16 bits inspirado en Undertale y Stardew Valley].
- Premisa: [PREMISA, por ejemplo un chico que a los 15 años sufre una convulsión y recibe un diagnóstico de epilepsia].
- Lo que abarca la historia: [ARCO_GENERAL, por ejemplo año a año hasta los 30: colegio, universidad, amistades, relaciones amorosas].
- Fuente principal: [FUENTE, por ejemplo el borrador se basa en mi experiencia real con la condición y es la referencia principal, o borra esta línea].

## Qué hacer
Reescribe solo este período, mejorando la redacción y la estructura, con un estilo a medio camino entre una novela y un guion: narración en prosa, escenas bien delimitadas y diálogos claros, pensando en que después los voy a llevar a Ink.

## Reglas
- Trabaja únicamente con lo que ocurre en este período. No adelantes ni inventes hechos de otros períodos.
- Si el borrador menciona algo de períodos anteriores que no está explicado, no lo completes: márcalo con un comentario `<!-- así -->`.
- Respeta los hechos y los personajes. No agregues eventos importantes ni elimines los que escribí.
- [REGLA_DE_TONO, por ejemplo muestra la condición con precisión, sin dramatizarla ni usarla para generar lástima; es una historia de valentía, crecimiento y fortaleza, no centrada solo en la enfermedad].
- Usa el mismo tipo de comentario para cualquier cosa ambigua, contradictoria o [IMPRECISION_A_VIGILAR, por ejemplo médicamente imprecisa].

## Entregable
- Un archivo .md con el período y la edad como título (`#`) y un subtítulo por escena (`##`).
- Al final, una lista corta con los comentarios `<!-- -->` que dejaste, para revisarlos de una vez.
