# love12xfuture Design System

> STARTER DRAFT — validate colors, fonts, and tone before treating as source of truth.
> Generated from brand signals: name, content focus (YouTube/LinkedIn/newsletter),
> Physical AI engineering context, and Isaiah 35 ethos (barren → generative).

---

## 1. Product Context

love12xfuture is a content brand for builders, engineers, and founders who want to think
12x further than the present moment. It lives across YouTube, LinkedIn, and a newsletter.
The audience is technically literate, action-oriented, and suspicious of hype — but
hungry for genuine signal about what's coming and how to build toward it. The tone is
warm, precise, and a little dangerous. Isaiah 35 energy: things that look barren are seeds.

---

## 2. Visual Theme & Mood

**Archetype:** "Warm Futurist" — not cold tech, not soft lifestyle. The intersection.
Think: a desert at golden hour, right before something blooms unexpectedly.

**Mood signals:**
- Generative, not declarative — things in motion, not finished
- Warmth without softness (warmth IS precision with a heartbeat)
- Dense ideas made navigable — complexity respected, not avoided
- Physical presence — grounded in atoms, not just bits

**Aesthetic:** Clean dark substrate with intentional warmth. Restrained palette that
earns its moments of color. Typography that carries intellectual weight without feeling
academic. Never sterile. Never shouty.

---

## 3. Color System

### Primary Palette

| Role         | Name        | Hex                       | Usage                        |
|--------------|-------------|---------------------------|------------------------------|
| Background   | Deep Slate  | `#0d0f12`                 | Page/canvas background       |
| Surface      | Slate       | `#141618`                 | Cards, panels                |
| Elevated     | Raised      | `#1c1f23`                 | Modals, tooltips             |
| Border       | Subtle      | `rgba(255,255,255,0.06)`  | Dividers, outlines           |
| Border Active| Medium      | `rgba(255,255,255,0.12)`  | Focused states               |

### Text

| Role      | Hex        | Usage                              |
|-----------|------------|------------------------------------|
| Primary   | `#f0ede8`  | Headlines, body — warm white       |
| Secondary | `#b8b4ae`  | Subheads, captions                 |
| Tertiary  | `#6b6762`  | Metadata, placeholder              |
| Inverse   | `#0d0f12`  | Text on light backgrounds          |

### Brand Accents

| Role              | Name              | Hex        | Usage                                    |
|-------------------|-------------------|------------|------------------------------------------|
| Primary Accent    | Desert Bloom      | `#e8956d`  | CTAs, links, highlights                  |
| Secondary Accent  | Signal Indigo     | `#6c7fff`  | Code, data, technical callouts           |
| Tertiary Accent   | Generative Green  | `#4ecb71`  | Success, growth, positive states         |
| Warning           | Amber             | `#f5a623`  | Caution states                           |
| Destructive       | Crimson           | `#e0534a`  | Error states                             |

**Desert Bloom (`#e8956d`):** Primary action color. One bloom per screen — don't dilute.
**Signal Indigo (`#6c7fff`):** For code blocks, data displays, technical terms.
Reserve white for text only. Never as background.

---

## 4. Typography

### Font Stack

**Display/Headlines:** `"Cabinet Grotesk"` — geometric, confident, slightly wide.
Fallback: `"Inter Variable"`, `system-ui`, sans-serif.
(Available free at fontshare.com)

**Body:** `"Inter Variable"` with `cv01`, `ss03` OpenType features enabled.

**Monospace:** `"Berkeley Mono"` or `"JetBrains Mono"`.

### Type Scale

| Token       | Size  | Weight | Line Height | Tracking | Usage             |
|-------------|-------|--------|-------------|----------|-------------------|
| display-xl  | 72px  | 700    | 1.05        | -2.5px   | Hero headlines    |
| display-lg  | 56px  | 700    | 1.08        | -1.8px   | Section heroes    |
| display-md  | 40px  | 700    | 1.1         | -1.2px   | Page titles       |
| heading-xl  | 32px  | 600    | 1.2         | -0.6px   | Major sections    |
| heading-lg  | 24px  | 600    | 1.25        | -0.3px   | Card titles       |
| heading-md  | 20px  | 600    | 1.3         | -0.2px   | Sub-sections      |
| body-lg     | 18px  | 400    | 1.65        | 0        | Long-form body    |
| body-md     | 16px  | 400    | 1.6         | 0        | Standard body     |
| body-sm     | 14px  | 400    | 1.5         | 0.1px    | Captions, meta    |
| label       | 12px  | 500    | 1.4         | 0.4px    | Tags, labels      |
| code        | 14px  | 400    | 1.6         | 0        | Code blocks       |

**Rules:** Display always Cabinet Grotesk, negative tracking, weight 700.
Never pure white `#ffffff` for text. Body: 16–18px, weight 400, line-height 1.6–1.65.

---

## 5. Layout & Spacing

### Grid
- Max content width: 1200px (marketing), 960px (editorial/newsletter)
- Columns: 12 desktop, 4 mobile
- Gutter: 24px desktop, 16px mobile
- Margin: 80px desktop, 24px mobile

### Spacing Scale (8px base)
```
4px   — micro
8px   — xs
12px  — sm
16px  — md
24px  — lg
32px  — xl
48px  — 2xl
64px  — 3xl
96px  — 4xl
128px — 5xl
```

---

## 6. Shadow & Elevation

Philosophy: depth through darkness, not drop shadows. Elevation = background lightness stepping.

| Level   | Background  | Shadow                              |
|---------|-------------|-------------------------------------|
| Ground  | `#0d0f12`   | none                                |
| Raised  | `#141618`   | none                                |
| Float   | `#1c1f23`   | `0 4px 16px rgba(0,0,0,0.4)`        |
| Overlay | `#23272d`   | `0 8px 32px rgba(0,0,0,0.6)`        |

---

## 7. Component Signatures

### Buttons
```css
/* Primary */
background: #e8956d; color: #0d0f12;
border-radius: 6px; padding: 10px 20px;
font-weight: 500; font-size: 15px; letter-spacing: 0.1px;

/* Secondary */
background: rgba(255,255,255,0.05);
border: 1px solid rgba(255,255,255,0.10);
color: #f0ede8; border-radius: 6px;

/* Ghost */
background: transparent; color: #e8956d;
border: 1px solid rgba(232,149,109,0.3);
```

### Cards
```css
background: #141618;
border: 1px solid rgba(255,255,255,0.06);
border-radius: 10px; padding: 24px;
/* Hover: */ border-color: rgba(255,255,255,0.12); background: #1c1f23;
```

### Border Radius Scale
```
4px  — inputs, small chips
6px  — buttons (default)
8px  — code blocks, small cards
10px — cards
16px — feature panels
24px — tags/badges ONLY
```

---

## 8. Design Guidelines

### Do
- Use Desert Bloom (`#e8956d`) sparingly — one dominant action per screen
- Let dark backgrounds breathe — whitespace signals confidence
- Use weight contrast (700 display vs 400 body) as primary hierarchy tool
- Use Signal Indigo on technical content to signal precision
- Prefer luminance stepping for depth

### Don't
- No pure white `#ffffff` — always warm white `#f0ede8`
- No more than 2 accent colors per screen
- No drop shadows on dark surfaces — luminance stepping only
- No positive letter-spacing on headlines
- No rounded pills on structural elements
- No generic SaaS blue (`#3b82f6`) — this is a Desert Bloom brand
- No light mode default without explicit decision (dark-native system)

---

## 9. Responsive Behavior

| Breakpoint | Width      | Notes                                         |
|------------|------------|-----------------------------------------------|
| Mobile     | < 640px    | Single column, 24px margins, stacked nav      |
| Tablet     | 640–1024px | 2-column grid, 32px margins                   |
| Desktop    | > 1024px   | Full 12-column, 80px margins, max 1200px      |

Typography scales down ~15–20% at mobile. Display caps at 40px mobile.

---

## 10. Agent Prompt Guide

### Quick prompt (copy-paste):
> "Build this UI using the love12xfuture design system. Dark background `#0d0f12`,
> surface `#141618`. Primary accent `#e8956d` (Desert Bloom). Font: Cabinet Grotesk
> for headlines (weight 700, negative tracking), Inter Variable for body. 6px radius
> on buttons, 10px on cards. Depth through background luminance stepping, not shadows.
> Warm and precise — never sterile, never shouty."

### For content graphics / thumbnails:
> "love12xfuture visual: dark `#0d0f12`, warm white `#f0ede8`, Desert Bloom accent
> `#e8956d`. Bold Cabinet Grotesk headlines. Dense but breathable. Desert at golden
> hour — calm and charged simultaneously."

### Anti-patterns to flag in review:
- Pure white backgrounds or text (cold, clinical)
- Multiple competing accent colors per screen
- Pill shapes on non-tag elements
- Drop shadows on dark-on-dark surfaces (use luminance stepping)
- Generic Tailwind blue-500 (`#3b82f6`) anywhere
- Light mode without explicit opt-in decision

---

## 11. Reference Influences

Studied: Linear (dark-mode architecture, luminance stepping, Inter Variable), Stripe
(typographic confidence, negative tracking at display sizes), Notion (editorial
spaciousness, content-first hierarchy). Differentiated: warmer accent palette (Desert
Bloom vs. indigo-first), larger body copy for long-form content, physicality that pure
SaaS lacks.
