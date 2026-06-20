# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Observatório da Participação Digital** — a single-page hot site for displaying data, indicators, and evidence about digital participation processes in Brazil. Built with Astro 6.

## Commands

```bash
npm install              # Install dependencies
npm run dev              # Start dev server at localhost:4321
npm run build            # Production build to ./dist/
npm run preview          # Preview production build locally
npm run astro -- [cmd]   # Run Astro CLI (e.g., astro check, astro add)
```

Node version: `>=22.12.0` (see `.nvmrc` — currently `22.21.0`).

## Architecture

This is an **Astro 6** static site with the standard Astro directory structure:

```
src/
├── assets/          # Static assets (SVGs, images) imported by components
├── components/      # Reusable .astro components
├── layouts/         # Page layout wrappers (Layout.astro)
└── pages/           # File-based routing — each .astro becomes a page
public/              # Static files copied verbatim to build output
```

**Key architectural decisions:**
- **Single-page design** by intent — the entire site is one page with smooth anchor navigation between sections (hero, indicators, timeline, data panels, API, partners, footer).
- **Zero JavaScript required for static content** — anchor navigation works via native `href`. Progressive enhancement only.
- **Sticky header** with backdrop blur, skip-to-content link as the first focusable element.
- **No shadows on standard cards** — hierarchy is built through color contrast, subtle borders, and whitespace, not elevation.

## Design System

The full design system is documented in `DESIGN.md` — **read it before writing any UI code**. All font choices, colors, spacing, and aesthetic direction are defined there. Do not deviate without explicit user approval. In QA mode, flag any code that doesn't match DESIGN.md.

**Memorable thing:** Confiança institucional — "Isso é sério. Isso é oficial. Posso confiar nesses dados."

Critical rules:

- **Primary color**: cobalt blue `#18499b` — the dominant institutional color. Use for buttons, active links, header, hero gradient.
- **Complementary accent**: terracotta `#b27c23` — used sparingly (max 5% of interface) for secondary CTAs and highlight tags only.
- **Typography**: Inter only. No decorative/serif fonts. Hierarchy via weight and size, never italic. Max 3 font sizes per screen.
- **Page background**: `#f7f8fa` (off-white with blue tint) — never pure white for the full page. Reserve `#ffffff` for cards/modals.
- **Border radius**: 8px for buttons/inputs, 12px for cards, 9999px for badges/tags. Never mix values in the same section.
- **Dark sections** (hero, banner, padrão de dados, footer): use `primary-10` (#031026) background with white text. The hero has an exclusive gradient.
- **Analogous, split-complementary, and triadic palettes** are for data visualization, charts, and document type badges only — never for UI structure.
- **`<details>/<summary>` nativo** para blocos expansíveis — funciona sem JS, estilo consistente com cards.
- **JS progressivo**: tudo funciona sem JS (filtros mostram todos os docs, downloads individuais, `<details>` nativo). JS adiciona filtro em tempo real, seleção múltipla e ZIP.
- **Dados reais**: comunicar o Hub de Participação Digital e o pipeline de ingestão real (poc-tls). Não inventar endpoints ou catálogos fictícios.
- **Accessibility**: WCAG AA compliance, 44px minimum tap targets, `prefers-reduced-motion` respected, skip-to-content link required, `aria-live` for dynamic announcements.

The `DESIGN.md` also specifies every component with exact colors, sizes, padding, typography tokens, hover/focus states, and responsive behavior.

## Deployment

Multi-stage Docker build (`Dockerfile`):
1. **Build stage**: Node LTS, `npm install`, `npm run build`
2. **Runtime stage**: Nginx Alpine serving `./dist` on port 8080, with gzip enabled

The `nginx.conf` handles SPA-style routing with `try_files $uri $uri/index.html =404`.

## TypeScript

Astro's strict TS config is extended from `astro/tsconfigs/strict`. Type-check with `npm run astro check` (needs `@astrojs/check` if not already installed).

## VS Code

The recommended extension is `astro-build.astro-vscode` (see `.vscode/extensions.json`).
