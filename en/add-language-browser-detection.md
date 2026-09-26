---
title: Add a second language with browser language detection
tool: Claude Code
use-when: A site needs a second language, chosen automatically from the visitor's browser, with a manual switcher and proper SEO
requires: Next.js App Router (adapt the routing part for other frameworks), content kept in typed files rather than hardcoded in components
tags: [i18n, nextjs, seo, middleware]
---

I want to add [NEW_LANGUAGE] support to this site, automatically detecting the browser language. [PRIMARY_LANGUAGE] remains the main language.

## Expected behavior
- Locale-prefixed routes: `/[PRIMARY_CODE]/...` and `/[NEW_CODE]/...`.
- On a route without a prefix, the server redirects based on the `Accept-Language` header: if the browser prefers [NEW_LANGUAGE], to `/[NEW_CODE]`; otherwise, to `/[PRIMARY_CODE]`. Detection happens in the middleware (or `proxy.ts`, depending on the Next.js version in the repo), not in client-side JavaScript, so there is no language flash.
- A language switcher in the navbar that matches the existing design. Switching keeps the same page, and the choice is saved in a cookie that takes priority over `Accept-Language` on later visits.
- Correct `<html lang>` for each language.

## Content
- Split the content by language (for example `content/[PRIMARY_CODE].ts` and `content/[NEW_CODE].ts`) with a shared type, so TypeScript fails if a language is missing a string. UI strings (navigation, buttons, labels, image alt text, footer) are also per language, not hardcoded in components.
- Translate with a natural, professional tone, not literally. Keep the same narrative and hierarchy as the original.
- For terms without a clear equivalent (job titles, degrees, local concepts), propose 2 or 3 options and wait for me to choose.
- Do not translate proper names, brand names or product names.
- Images that contain text in the original language stay as they are; only translate their alt text.
- Downloadable files (for example a CV or a PDF) point to the version for each language. If one is missing, leave a placeholder and tell me.

## SEO
- Metadata (title, description, Open Graph) per language.
- `alternates` with `hreflang` ([PRIMARY_CODE], [NEW_CODE] and x-default pointing to [PRIMARY_CODE]) on every page.
- A sitemap with both versions of each route.

## Constraints
- Do not change the design, colors, animations or any other visual behavior.
- Choose the simplest, most maintainable solution: next-intl, or the dictionary pattern from the official Next.js docs. Justify the choice in one line.
- No runtime machine translation and no external services.

## Workflow
1. Before touching code, show me a short plan: chosen library, folder structure, how the middleware works and the translation options for ambiguous terms. Wait for my OK.
2. If the project uses an issue tracker, create a single issue for this work with acceptance criteria.
3. Implement and verify:
   - `/` with a browser in [NEW_LANGUAGE] redirects to `/[NEW_CODE]`, and with a browser in [PRIMARY_LANGUAGE] to `/[PRIMARY_CODE]`
   - the switcher cookie wins over the browser setting
   - no untranslated strings on any page
   - build and lint pass with no errors
4. Update AGENTS.md (or CLAUDE.md) with the rule that every new string must be added in both languages.
