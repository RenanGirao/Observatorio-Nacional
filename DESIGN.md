---
version: beta
name: Observatório da Participação Digital
description: >
  Plataforma de dados abertos sobre participação social digital no Brasil —
  indicadores, processos, documentos e um padrão de dados público. Inclui
  a home (página única com navegação por âncoras) e a página de Pesquisas
  e publicações (/pesquisas).
memorable: >
  Confiança institucional — "Isso é sério. Isso é oficial. Posso confiar
  nesses dados." Toda decisão de design serve essa percepção.
colors:
  # === Monochromatic / Polite (variações do azul cobalto) ===
  primary-95: "#d2e0f7"
  primary-80: "#729de5"
  primary-60: "#396bbf"
  primary: "#18499b"
  primary-40: "#163972"
  primary-20: "#0b234c"
  primary-10: "#031026"

  # === Complementary (terracota — oposto ao azul) ===
  # Máximo 5% da interface. CTAs secundários e tags de destaque.
  comp-95: "#f2d6a9"
  comp-80: "#e5b15b"
  comp-60: "#cc8e28"
  comp: "#b27c23"
  comp-40: "#7f5613"
  comp-20: "#4c3207"

  # === Analogous — apenas para dados, gráficos, categorização ===
  ana-left-80: "#2fadbf"
  ana-left-60: "#19727f"
  ana-left-40: "#09393f"
  ana-right-80: "#4939bf"
  ana-right-60: "#2b1f7f"
  ana-right-40: "#1a124f"

  # === Split Complementary — apenas para estados semânticos ===
  split-left-80: "#d84a36"
  split-left-60: "#992d1e"
  split-left-40: "#4c130b"
  split-right-80: "#bacc3d"
  split-right-60: "#737f1f"
  split-right-40: "#3a4010"

  # === Triadic — apenas para dashboards, indicadores, categorias ===
  tri-left-80: "#d83673"
  tri-left-60: "#991e4c"
  tri-left-40: "#4c0b23"
  tri-right-80: "#72cc3d"
  tri-right-60: "#437f1f"
  tri-right-40: "#224010"

  # === Neutros ===
  background: "#f7f8fa"
  surface: "#ffffff"
  foreground: "#111827"
  muted: "#6b7280"
  border: "#e5e7eb"
  on-primary: "#ffffff"
  on-comp: "#ffffff"

  # === Semânticos ===
  success: "#17a34a"
  warning: "#eab308"
  danger: "#dc2626"
  info: "#18499b"

typography:
  display:
    fontFamily: "Inter, -apple-system, system-ui, sans-serif"
    fontSize: 48px
    fontWeight: 600
    lineHeight: 1.1
    letterSpacing: "-0.02em"
  h1:
    fontFamily: "Inter, -apple-system, system-ui, sans-serif"
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "-0.01em"
  h2:
    fontFamily: "Inter, -apple-system, system-ui, sans-serif"
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "-0.01em"
  h3:
    fontFamily: "Inter, -apple-system, system-ui, sans-serif"
    fontSize: 20px
    fontWeight: 600
    lineHeight: 1.3
  body-lg:
    fontFamily: "Inter, -apple-system, system-ui, sans-serif"
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.6
  body-md:
    fontFamily: "Inter, -apple-system, system-ui, sans-serif"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: "Inter, -apple-system, system-ui, sans-serif"
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  label-md:
    fontFamily: "Inter, -apple-system, system-ui, sans-serif"
    fontSize: 14px
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: "0.01em"
  label-sm:
    fontFamily: "Inter, -apple-system, system-ui, sans-serif"
    fontSize: 12px
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: "0.02em"
  mono-md:
    fontFamily: "ui-monospace, 'JetBrains Mono', monospace"
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "0"
  mono-sm:
    fontFamily: "ui-monospace, 'JetBrains Mono', monospace"
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: "0"

rounded:
  none: 0px
  sm: 4px
  md: 8px
  lg: 12px
  xl: 16px
  full: 9999px

spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
  4xl: 80px
  gutter: 24px
  margin: 32px

components:
  # === Botões ===
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: "12px 24px"
  button-primary-hover:
    backgroundColor: "{colors.primary-40}"
    textColor: "{colors.on-primary}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: "12px 24px"
    border: "1px solid {colors.primary}"
  button-secondary-hover:
    backgroundColor: "{colors.primary-95}"
    textColor: "{colors.primary}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.muted}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: "10px 14px"
    border: "1px solid {colors.border}"
  button-ghost-hover:
    textColor: "{colors.danger}"
    borderColor: "{colors.danger}"
  button-dark-primary:
    backgroundColor: "{colors.primary-60}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: "12px 24px"
  button-dark-primary-hover:
    backgroundColor: "{colors.primary}"
  button-dark-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.md}"
    padding: "12px 24px"
    border: "1px solid {colors.on-primary}"
  button-dark-secondary-hover:
    backgroundColor: "rgba(255, 255, 255, 0.1)"

  # === Cards base ===
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.lg}"
    padding: "20px"
    border: "1px solid {colors.border}"
  card-hover:
    borderColor: "{colors.primary-80}"
  card-indicator:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.lg}"
    padding: "24px"
    border: "1px solid {colors.border}"

  # === Inputs ===
  input:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.md}"
    padding: "10px 14px"
    border: "1px solid {colors.border}"
    typography: "{typography.body-md}"
    minHeight: "44px"
  input-focus:
    borderColor: "{colors.primary}"
    outline: "2px solid {colors.primary-60}"
    outlineOffset: "2px"
  input-error:
    borderColor: "{colors.danger}"
  input-search:
    backgroundImage: "lupa SVG inline"
    backgroundPosition: "left 12px center"
    paddingLeft: "40px"

  # === Navegação ===
  nav-link:
    textColor: "{colors.foreground}"
    typography: "{typography.label-md}"
  nav-link-active:
    textColor: "{colors.primary}"
  nav-link-hover:
    textColor: "{colors.primary}"

  # === Tags e Badges ===
  tag:
    backgroundColor: "{colors.primary-95}"
    textColor: "{colors.primary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: "4px 12px"
  tag-accent:
    backgroundColor: "{colors.comp-95}"
    textColor: "{colors.comp}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: "4px 12px"
  tag-dark-section:
    backgroundColor: "rgba(255, 255, 255, 0.1)"
    textColor: "{colors.primary-95}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: "4px 12px"
    textTransform: "uppercase"
  tag-doc-type:
    backgroundColor: "{type-color}18"
    textColor: "{type-color}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: "2px 10px"
    border: "1px solid {type-color}30"
  tag-count:
    backgroundColor: "{colors.primary-95}"
    textColor: "{colors.primary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: "2px 10px"

  # === Seções ===
  section-light:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    padding: "80px 24px"
  section-dark:
    backgroundColor: "{colors.primary-10}"
    textColor: "{colors.on-primary}"
    padding: "80px 24px"

  # === Banner de página interna ===
  page-banner:
    backgroundColor: "{colors.primary-10}"
    textColor: "{colors.on-primary}"
    padding: "64px 24px"

  # === Document card (/pesquisas) ===
  document-card:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.lg}"
    padding: "16px"
    border: "1px solid {colors.border}"
    layout: "flex row"
  document-card-hover:
    borderColor: "{colors.primary-80}"
  document-card-checkbox:
    width: "20px"
    height: "20px"
    accentColor: "{colors.primary}"

  # === Filter bar (/pesquisas) ===
  filter-bar:
    layout: "flex row wrap"
    gap: "{spacing.md}"
  filter-group:
    layout: "flex column"
    gap: "{spacing.xs}"
    minWidth: "140px"
    flex: "1 1 160px"
  filter-search:
    flex: "1 1 260px"
    minWidth: "200px"

  # === Process group (/pesquisas) ===
  process-group:
    element: "<details>/<summary> nativo"
    backgroundColor: "{colors.surface}"
    border: "1px solid {colors.border}"
    rounded: "{rounded.lg}"
  process-group-open:
    borderColor: "{colors.primary-80}"
  process-summary:
    padding: "{spacing.lg}"
    layout: "flex row space-between"
    cursor: "pointer"
    listStyle: "none"
  process-summary-hover:
    backgroundColor: "{colors.primary-95}"
  process-chevron:
    transition: "transform 200ms ease"
    openTransform: "rotate(180deg)"
    openColor: "{colors.primary}"

  # === Floating download bar (/pesquisas) ===
  download-bar:
    position: "sticky"
    bottom: "0"
    zIndex: "90"
    backgroundColor: "{colors.surface}"
    borderTop: "1px solid {colors.border}"
    boxShadow: "0 -4px 24px rgba(3, 16, 38, 0.15)"
    padding: "{spacing.md} {spacing.gutter}"

  # === Catalog card (/pesquisas) ===
  catalog-card:
    backgroundColor: "{colors.surface}"
    border: "1px solid {colors.border}"
    rounded: "{rounded.lg}"
    padding: "{spacing.lg}"
    layout: "flex column"
  catalog-card-hover:
    borderColor: "{colors.primary-80}"

  # === Data entity card (/#padrao-dados) ===
  data-entity-card:
    backgroundColor: "{colors.primary-20}"
    border: "1px solid rgba(255, 255, 255, 0.08)"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
  data-entity-card-hover:
    borderColor: "rgba(255, 255, 255, 0.2)"

  # === Submission callout (/#padrao-dados) ===
  submission-callout:
    backgroundColor: "rgba(255, 255, 255, 0.05)"
    border: "1px solid rgba(255, 255, 255, 0.1)"
    rounded: "{rounded.lg}"
    padding: "{spacing.lg}"

  # === Timeline ===
  timeline-dot:
    backgroundColor: "{colors.primary}"
    size: "16px"
    rounded: "{rounded.full}"
  timeline-line:
    backgroundColor: "{colors.border}"
    width: "2px"

  # === Hero (exclusivo da home) ===
  hero-gradient:
    background: "linear-gradient(135deg, #031026 0%, #163972 50%, #18499b 100%)"

  # === Footer ===
  footer:
    backgroundColor: "{colors.primary-10}"
    textColor: "{colors.primary-95}"
    padding: "48px 32px"
---

# Observatório da Participação Digital — DESIGN.md

## Overview

**Confiança institucional com calor humano.** O Observatório da Participação Digital é uma plataforma de dados abertos sobre participação social no Brasil. O design evoca seriedade, oficialidade e transparência — sem ser frio ou distante.

A identidade é construída sobre um **azul cobalto profundo** (#18499b) que domina o hero, a navegação e os botões primários. O tom é equilibrado por superfícies claras (#f7f8fa) que evitam o branco puro e por um **terracota complementar** (#b27c23) usado como acento quente em no máximo 5% da interface.

**Arquitetura:** homepage de página única com navegação por âncoras + página dedicada `/pesquisas` para documentos e publicações. Densidade média-alta em desktop, respirável em mobile.

**Público-alvo:** gestores públicos, pesquisadores, organizações da sociedade civil, cidadãos interessados e equipes técnicas.

**Diferenciador memorável:** a combinação do azul institucional dominante com o terracota complementar usado com parcimônia extrema. O azul diz "isso é oficial"; o terracota diz "isso é humano". Juntos, constroem confiança sem frieza.

## Colors

A paleta é ancorada no azul cobalto extraído da imagem de referência `Home.png`. Variações monochromáticas constroem hierarquia; as paletas análoga, split-complementary e triádica são **exclusivas para dados, gráficos e categorização** — nunca para UI estrutural.

### Paleta Principal (Monochromatic)

- **Primary-95 (#d2e0f7):** Fundo de tags, badges, hover states sutis.
- **Primary-80 (#729de5):** Ícones secundários, gráficos de suporte, estados desabilitados.
- **Primary-60 (#396bbf):** Links secundários, bordas de foco, CTAs em seções escuras.
- **Primary (#18499b):** Cor principal. Botões primários, links ativos, header, timeline dots.
- **Primary-40 (#163972):** Hover de botões primários, fundo de seções escuras.
- **Primary-20 (#0b234c):** Fundo de cards em seções escuras (data entity cards).
- **Primary-10 (#031026):** Fundo mais profundo do hero, footer, banner de página interna.

### Paleta Complementar

O terracota é o oposto cromático do azul. Uso máximo: 5% da interface.

- **Comp-95 (#f2d6a9):** Fundo de tags de alerta leve.
- **Comp-80 (#e5b15b):** Ícones de aviso, destaques em gráficos, badges de "Apresentação".
- **Comp (#b27c23):** Acento principal. Exclusivo para CTAs secundários e tags de destaque.
- **Comp-40 (#7f5613):** Texto sobre fundos claros quando o comp precisa ser legível.

### Paletas de Dados (uso exclusivo para gráficos e categorização)

**Análoga** (ciano e azul-violeta) — categorias de dados:
- ana-left-80 (#2fadbf): categoria "Relatório"
- ana-right-80 (#4939bf): categoria "Documento técnico"

**Split-Complementary** — estados semânticos:
- split-left-80 (#d84a36): erro, "Documento normativo"
- split-right-80 (#bacc3d): atenção, "Material de apoio"

**Triádica** — indicadores de status:
- tri-left-80 (#d83673): status crítico
- tri-right-80 (#72cc3d): sucesso, "Dataset"

### Tipos de Documento (mapeamento de cores)

| Tipo | Cor | Paleta |
|---|---|---|
| Relatório | `ana-left-80` (#2fadbf) | Análoga |
| Dataset | `tri-right-80` (#72cc3d) | Triádica |
| Documento técnico | `ana-right-80` (#4939bf) | Análoga |
| Documento normativo | `split-left-80` (#d84a36) | Split-comp |
| Apresentação | `comp-80` (#e5b15b) | Complementar |
| Ata/Registro | `primary-60` (#396bbf) | Principal |
| Material de apoio | `split-right-80` (#bacc3d) | Split-comp |
| Anexo | `primary-80` (#729de5) | Principal |

### Neutros

- **Background (#f7f8fa):** Fundo de página. Nunca use #ffffff como fundo de página.
- **Surface (#ffffff):** Cards, header, inputs, modais. Branco puro apenas para elementos flutuantes.
- **Foreground (#111827):** Texto principal — quase preto com toque de azul.
- **Muted (#6b7280):** Texto secundário, captions, metadados, placeholders.
- **Border (#e5e7eb):** Divisores, bordas de cards, bordas de inputs inativos.
- **On-Primary (#ffffff):** Texto e ícones sobre fundos azuis.
- **On-Comp (#ffffff):** Texto e ícones sobre fundos terracota.

## Typography

**Inter** em todos os níveis. Sem fontes decorativas ou serifadas. Hierarquia por peso, tamanho e espaçamento — nunca por itálico.

- **Display (48px / 600 / -0.02em):** Números de indicadores no hero. Uso exclusivo para dados estatísticos.
- **H1 (32px / 600 / -0.01em):** Títulos de página e seção.
- **H2 (24px / 600 / -0.01em):** Subtítulos de seção, títulos de cards de timeline.
- **H3 (20px / 600):** Títulos de cards, títulos de documentos, nomes de entidade.
- **Body-lg (18px / 400 / 1.6):** Parágrafos introdutórios. Máximo 60 caracteres por linha.
- **Body-md (16px / 400 / 1.6):** Texto corrido padrão.
- **Body-sm (14px / 400 / 1.5):** Metadados, descrições de card, timestamps, corpo de entidade.
- **Label-md (14px / 500 / 0.01em):** Botões, links de navegação.
- **Label-sm (12px / 500 / 0.02em):** Badges, tags, contadores, labels de filtro. Caixa alta para tags semânticas ("PADRÃO DE DADOS").
- **Mono-md (14px / JetBrains Mono):** Código, endpoints, paths de API.
- **Mono-sm (12px / JetBrains Mono):** Código inline, nomes de campo técnico em callouts.

**Regras:**
- Nunca mais de 3 tamanhos de fonte em uma única tela.
- Sentence-case para títulos e labels. Title-case apenas para nomes próprios.
- Nunca use itálico para ênfase — use peso 600 ou cor primary.
- Texto sobre primary-10 ou primary-20 deve usar on-primary (#ffffff) e atender WCAG AA (4.5:1).

## Layout

Grid de 12 colunas com largura máxima de 1200px e gutters de 24px. Tablet (640–1023px): 8 colunas, gutters 16px. Mobile (<640px): 4 colunas, gutters 12px.

**Espaçamento vertical:**
- Seções principais: 80px padding-top e padding-bottom em desktop, 48px em tablet, 32px em mobile.
- Banner de página interna: 64px vertical em desktop.
- Cards internos: padding de 16px a 24px dependendo da densidade.
- Entre elementos relacionados: 16px. Entre grupos: 32px. Entre seções: 80px.

**Grids específicos:**
- Indicadores: 5 col (desktop) → 3 col (tablet) → 2 col (mobile)
- Pilares: 4 col → 2 col → 1 col
- Parceiros: 3 col → 2 col → 1 col
- Catálogos: 2 col → 1 col → 1 col
- Documentos por processo: 1 col sempre
- Filtros: flex-wrap row → column em mobile

**Whitespace:** o espaço em branco é o principal separador. Bordas visíveis apenas entre seções de natureza distinta.

## Elevation & Depth

Design **predominantemente flat**. Sem sombras em cards, inputs ou botões padrão. Hierarquia construída por:

1. **Contraste de cor:** fundos escuros (hero, banner, footer, padrão de dados) vs. fundos claros.
2. **Bordas sutis:** 1px solid border (#e5e7eb) em cards e inputs.
3. **Espaçamento:** seções bem separadas criam camadas naturais.

**Elevação aplicada apenas em:**
- **Header sticky:** `background: rgba(255,255,255,0.95)` + `backdrop-filter: blur(8px)` + `border-bottom: 1px solid #e5e7eb`. Sombra: `0 1px 3px rgba(3,16,38,0.08)`.
- **Menu mobile:** `box-shadow: 0 4px 16px rgba(3,16,38,0.12)`.
- **Download bar (flutuante):** `box-shadow: 0 -4px 24px rgba(3,16,38,0.15)` — fixa na base da viewport.

**Hero gradient** (exclusivo da home): `linear-gradient(135deg, #031026 0%, #163972 50%, #18499b 100%)`.

## Shapes

- **Border-radius padrão:** 8px (md) para botões, inputs, selects, data entity cards.
- **Cards:** 12px (lg) — cards de indicador, documento, catálogo, processo.
- **Badges e tags:** 9999px (full) — pill-shaped. Inclui tags de tipo de documento.
- **Timeline dots:** 9999px (full) — círculos de 16px.
- **Callout boxes:** 12px (lg) — consistente com cards.
- **Nunca misture** border-radius diferentes na mesma seção.

## Components

### Buttons

**Primary:**
- Fundo: primary (#18499b). Texto: branco. Fonte: label-md.
- Padding: 12px 24px. Border-radius: 8px. Mínimo 44x44px.
- Hover: primary-40 (#163972). Transição: 200ms ease.
- Focus: outline 2px solid primary-60, offset 2px.

**Secondary:**
- Fundo: transparente. Borda: 1px solid primary. Texto: primary.
- Hover: fundo primary-95. Texto: primary.

**Dark section buttons (usados no padrão de dados, banner):**
- Primary-dark: fundo primary-60, hover primary.
- Secondary-dark: transparente + borda branca, hover rgba(255,255,255,0.1).

**Ghost (download bar):**
- Fundo: transparente. Borda: 1px solid border. Texto: muted.
- Hover: texto danger, borda danger. Usado para "Limpar seleção".

### Cards

**Card de indicador:**
- Fundo: surface. Borda: 1px solid border. Border-radius: 12px. Padding: 24px.
- Número: display (48px / 600 / primary). Label: body-sm (muted).
- Hover: borda primary-80, sem sombra.

**Card de documento (`/pesquisas`):**
- Fundo: background (#f7f8fa). Borda: 1px solid border. Border-radius: 12px. Padding: 16px.
- Layout: flex row (checkbox + corpo + ações).
- Checkbox: 20x20px, accent-color primary, alinhado ao topo.
- Título: body-md / 600 / foreground.
- Badge de tipo: tag-doc-type com cor da paleta de dados correspondente.
- Descrição: body-sm / muted, 1-2 linhas.
- Metadata row: body-sm / muted, ícones 14px inline.
- Ações: download (button-primary, height 36px) + copiar link (button-ghost, 36x36px).
- Mobile: flex-wrap, ações ocupam 100% da largura, download expandido.
- Hover: borda primary-80.

**Card de catálogo (`/pesquisas`):**
- Fundo: surface. Borda: 1px solid border. Border-radius: 12px. Padding: 24px.
- Header: nome (h3) + badge de tipo (tag).
- Descrição: body-md / muted.
- Footer: contagem de datasets (body-sm / muted) + link externo (label-md / primary).
- Separador entre corpo e footer: 1px solid border.

**Card de entidade de dados (`/#padrao-dados`):**
- Fundo: primary-20. Borda: 1px solid rgba(255,255,255,0.08). Border-radius: 8px. Padding: 24px.
- Nome: h3 / on-primary.
- Descrição: body-sm / primary-80, sem campos técnicos.
- Hover: borda rgba(255,255,255,0.2).

**Card de processo — `<details>/<summary>` (`/pesquisas`):**
- Elemento HTML nativo. Funciona sem JS.
- Fundo: surface. Borda: 1px solid border. Border-radius: 12px.
- Aberto: borda primary-80.
- Summary: padding 24px, flex row space-between, cursor pointer, list-style none.
- Summary hover: background primary-95.
- Chevron SVG: 20x20px, rotated 180° quando aberto, cor primary quando aberto.
- Meta: período + tema (body-sm / muted) + contagem de docs (tag-count).
- Conteúdo: padding 16px, border-top 1px solid border.

### Filter Bar (`/pesquisas`)

- Container: flex-wrap row, gap 16px, align-items flex-end.
- Campo de busca: flex 1 1 260px, input com ícone de lupa à esquerda (SVG inline no background-image, padding-left 40px).
- Grupo de filtro: flex column, gap 4px, flex 1 1 160px, min-width 140px.
- Label do filtro: label-sm / muted / uppercase.
- Select/input: padrão input do sistema.
- Mobile: flex-direction column, todos 100% width.
- JS progressivo: filtros aplicados com `input`/`change`, resultados anunciados via `aria-live`.
- Sem JS: todos os documentos visíveis, formulário submete normalmente.

### Floating Download Bar (`/pesquisas`)

- Sticky na base (bottom: 0, z-index: 90).
- Fundo: surface. Border-top: 1px solid border. Sombra: 0 -4px 24px rgba(3,16,38,0.15).
- Inner: max-width 1200px, flex row space-between.
- Contagem: body-md / 500 / foreground.
- Ações: "Limpar seleção" (button-ghost) + "Baixar selecionados (ZIP)" (button-primary).
- Hidden por padrão (atributo `hidden`). JS mostra/esconde conforme checkboxes.
- Mobile: flex-direction column, botões em coluna.

### Submission Callout (`/#padrao-dados`)

- Fundo: rgba(255,255,255,0.05). Borda: 1px solid rgba(255,255,255,0.1). Border-radius: 12px. Padding: 24px.
- Título: h3 / on-primary.
- Texto: body-sm / primary-80. `<strong>` em primary-95. `<code>` em mono-sm com fundo rgba(255,255,255,0.1).
- CTAs alinhados abaixo do texto, mesmo estilo dos dark section buttons.

### Tags & Badges

- **Tag padrão:** primary-95 / primary / label-sm / full rounded / 4px 12px.
- **Tag de destaque:** comp-95 / comp / label-sm / full rounded / 4px 12px.
- **Tag de seção escura:** rgba(255,255,255,0.1) / primary-95 / label-sm / full rounded / uppercase.
- **Badge de tipo de documento:** cor da paleta de dados a 10% opacity no fundo, cor sólida no texto, borda sutil da mesma cor a 20% opacity.
- **Badge de contagem:** primary-95 / primary / label-sm / full rounded / 2px 10px.

### Navigation

**Header sticky (presente em todas as páginas):**
- Fundo: surface 95% opacity + blur(8px). Altura: 64px desktop, 56px mobile.
- Links: Sobre (#sobre), Indicadores (#indicadores), Linha do Tempo (#linha-do-tempo), Dados (#padrao-dados), Parceiros (#parceiros), Pesquisas e publicações (/pesquisas).
- Links âncora (#) navegam na home. O link /pesquisas é uma rota de página.
- Link ativo: primary. Hover: primary.
- Mobile: hamburger menu (44x44px), overlay full-screen, fundo primary-10, texto branco, links altura 48px mínima.
- Skip-to-content: primeiro elemento focável, visível apenas no focus.

**Footer:**
- Fundo: primary-10. Texto: primary-95.
- 4 colunas em desktop, 2 em tablet, 1 em mobile.
- Links: hover primary-80 com underline.
- Logos institucionais (Dataprev, UnB, Secretaria-Geral, gov.br) + Creative Commons.

### Timeline

- Desktop: linha vertical central, cards alternando esquerda/direita, largura máxima 480px.
- Mobile: linha à esquerda (24px do edge), cards à direita.
- Dots: 16px, primary, full rounded. Linha: 2px, border color.
- Ano: label-sm, primary.
- Card: surface, 12px radius, 20px padding.

### Hero (exclusivo da home)

- Background: gradient linear 135deg primary-10 → primary-40 → primary.
- Altura: 40-60vh. Conteúdo alinhado ao topo com padding generoso (64px).
- Números de indicadores em display (48px/600).
- CTA principal em comp (#b27c23).

## Páginas

### Home (`/`)

Página única com navegação por âncoras: Hero → Sobre → Indicadores → Linha do Tempo → Padrão de Dados → Parceiros → Footer.

### Pesquisas e publicações (`/pesquisas`)

Página dedicada com banner primary-10, barra de filtros, documentos organizados por processo (blocos `<details>` expansíveis), barra de download flutuante e seção de fontes de dados abertos.

## Seção Padrão de Dados (`/#padrao-dados`)

Substituiu a antiga seção "API". Seção dark (primary-10) com:
- Tag "PADRÃO DE DADOS" (uppercase).
- Título e introdução explicando que um padrão aberto está sendo construído.
- 5 cards de entidade (Processo, Participação, Indicador, Publicação, Estado) — cada um com nome + descrição conceitual, sem listagem de campos técnicos.
- Callout explicando o fluxo de submissão: CLI `hub-participacao enviar` → mTLS → validação → scoring → persistência.
- CTAs: "Solicitar cadastro de órgão" + "Documentação do padrão".

## Do's and Don'ts

- **Do** usar o azul primary (#18499b) como cor dominante.
- **Don't** usar o terracota comp (#b27c23) em mais de 5% da interface.
- **Do** manter o fundo de página como background (#f7f8fa).
- **Don't** usar gradientes fora do hero da home. Banner de página usa primary-10 sólido.
- **Do** usar `<details>/<summary>` nativo para blocos expansíveis — funciona sem JS.
- **Don't** usar sombras em cards padrão. A hierarquia é por borda e espaçamento.
- **Do** usar `aria-live` para anúncios dinâmicos (resultados de filtro, contagem de seleção).
- **Don't** usar cores das paletas análoga, split-complementary ou triádica para UI estrutural. São exclusivas para dados, gráficos e badges de tipo.
- **Do** manter a página funcional sem JavaScript. Conteúdo estático, `<details>` nativo, downloads individuais e formulário de filtro funcionam sem JS.
- **Don't** criar animações auto-play. Respeitar `prefers-reduced-motion`.
- **Do** garantir que todo elemento interativo tenha no mínimo 44x44px de área de toque.
- **Don't** usar mais de 3 tamanhos de fonte em uma única tela.
- **Do** usar sentence-case para títulos e labels da UI.
- **Don't** usar floating labels em formulários. Labels sempre visíveis acima do campo.
- **Do** usar mono (JetBrains Mono) apenas para código, paths e dados técnicos em callouts.
- **Don't** misturar border-radius diferentes na mesma seção.
- **Do** usar a cor de link (primary) com underline no hover — links nunca dependem apenas de cor.
- **Don't** esquecer o `aria-label` ou `<label>` associado em todos os inputs.
- **Do** comunicar o fluxo de dados real: Hub de Participação Digital → validação → Observatório.
- **Don't** inventar endpoints fictícios ou catálogos que não existem.

## Decisions Log

| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-06-16 | Design system inicial | Criado por /design-consultation baseado na imagem Home.png |
| 2026-06-17 | Página /pesquisas adicionada | Centralizar documentos e publicações, comunicar fontes de dados |
| 2026-06-17 | Seção API substituída por Padrão de Dados | Comunicar o modelo de dados real (Hub), não endpoints fictícios |
| 2026-06-17 | Header: "API" → "Dados", link #padrao-dados | Consistência com a nova seção |
| 2026-06-17 | Catálogos DKAN/CKAN substituídos por Hub + dados.gov.br | Alinhamento com a infraestrutura real (poc-tls) |
| 2026-06-17 | Componentes inline em vez de arquivos separados | Componentes single-use não justificam indireção de arquivo |
| 2026-06-17 | Refresh completo do DESIGN.md | Sincronizar com o estado atual do código após múltiplas features |
