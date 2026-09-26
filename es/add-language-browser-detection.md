---
title: Agregar un segundo idioma con detección del idioma del navegador
tool: Claude Code
use-when: Un sitio necesita un segundo idioma elegido automáticamente según el navegador del visitante, con selector manual y SEO correcto
requires: Next.js App Router (adapta la parte de rutas si es otro framework), contenido en archivos tipados y no escrito directo en los componentes
tags: [i18n, nextjs, seo, middleware]
---

Quiero agregar soporte para [IDIOMA_NUEVO] a este sitio, detectando automáticamente el idioma del navegador. [IDIOMA_PRINCIPAL] sigue siendo el idioma principal.

## Comportamiento esperado
- Rutas con prefijo de idioma: `/[CODIGO_PRINCIPAL]/...` y `/[CODIGO_NUEVO]/...`.
- Al entrar a una ruta sin prefijo, el servidor redirige según el encabezado `Accept-Language`: si el navegador prefiere [IDIOMA_NUEVO], a `/[CODIGO_NUEVO]`; en cualquier otro caso, a `/[CODIGO_PRINCIPAL]`. La detección se hace en el middleware (o `proxy.ts`, según la versión de Next.js del repo), no con JavaScript en el cliente, para que no haya parpadeo de idioma.
- Selector de idioma en la navbar, con el mismo estilo del diseño actual. Al cambiar de idioma se mantiene la misma página, y la elección se guarda en una cookie que tiene prioridad sobre `Accept-Language` en las visitas siguientes.
- `<html lang>` correcto en cada idioma.

## Contenido
- Separa el contenido por idioma (por ejemplo `content/[CODIGO_PRINCIPAL].ts` y `content/[CODIGO_NUEVO].ts`) con un tipo compartido, para que TypeScript falle si a un idioma le falta un texto. Los textos de interfaz (navegación, botones, etiquetas, texto alternativo de imágenes, footer) también van por idioma, no escritos directo en los componentes.
- Traduce con tono natural y profesional, no literal. Mantén la misma narrativa y jerarquía del original.
- Para términos sin equivalente claro (cargos, títulos universitarios, conceptos locales), propónme 2 o 3 opciones y espera que elija una.
- No traduzcas nombres propios, de marca ni de producto.
- Las imágenes que tienen texto en el idioma original se mantienen; solo se traduce su texto alternativo.
- Los archivos descargables (por ejemplo un CV o un PDF) apuntan a la versión de cada idioma. Si falta alguno, déjalo como placeholder y avísame.

## SEO
- Metadata (title, description, Open Graph) por idioma.
- `alternates` con `hreflang` ([CODIGO_PRINCIPAL], [CODIGO_NUEVO] y x-default apuntando a [CODIGO_PRINCIPAL]) en cada página.
- Sitemap con ambas versiones de cada ruta.

## Restricciones
- No cambies el diseño, los colores, las animaciones ni ningún otro comportamiento visual.
- Elige la solución más simple y mantenible: next-intl, o el patrón de diccionarios de la documentación oficial de Next.js. Justifica la elección en una línea.
- No uses traducción automática en tiempo de ejecución ni servicios externos.

## Forma de trabajo
1. Antes de tocar código, muéstrame un plan corto: librería elegida, estructura de carpetas, cómo funciona el middleware y las opciones de traducción para los términos ambiguos. Espera mi OK.
2. Si el proyecto usa un gestor de issues, crea una sola issue para este trabajo con criterios de aceptación.
3. Implementa y verifica:
   - `/` con el navegador en [IDIOMA_NUEVO] redirige a `/[CODIGO_NUEVO]`, y con el navegador en [IDIOMA_PRINCIPAL] a `/[CODIGO_PRINCIPAL]`
   - la cookie del selector gana sobre el idioma del navegador
   - no hay textos sin traducir en ninguna página
   - build y lint pasan sin errores
4. Actualiza AGENTS.md (o CLAUDE.md) con la regla de que todo texto nuevo debe agregarse en ambos idiomas.
