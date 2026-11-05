# Design System — Proposed Systems Console

**Status:** Approved by owner on 2026-11-05 as the Phase 4 implementation baseline.

## Color system

**Theme decision:** Dark mode only. A light mode is not required.

| Token | HEX | Use |
| --- | --- | --- |
| `--bg` | `#0B1020` | Primary page background. |
| `--surface` | `#141C33` | Cards and primary panels. |
| `--surface-raised` | `#1B2745` | Hovered cards and layered windows. |
| `--border` | `#4B638E` | Panel borders, dividers, inactive controls. |
| `--text` | `#F1F5F9` | Main body text. |
| `--text-muted` | `#B6C2D9` | Supporting metadata. |
| `--cyan` | `#62D9FF` | Links, focus rings, primary CTA. |
| `--amber` | `#FFC857` | Featured credential and highlights. |
| `--green` | `#73E2A7` | Completed/available state with a text label. |
| `--rose` | `#FF879D` | Error/destructive state with a text label. |

Contrast must be verified with the final font sizes. Color never carries meaning alone: status badges include plain text such as “Completed” or “Ongoing / In Development.”

## Typography

| Role | Family and fallback | Size / leading |
| --- | --- | --- |
| Display heading | `Pixelify Sans`, system-ui, sans-serif | `clamp(2rem, 5vw, 4.5rem)` / 1.05 |
| Section heading | `Pixelify Sans`, system-ui, sans-serif | `clamp(1.5rem, 3vw, 2.4rem)` / 1.15 |
| Body | Inter, system-ui, -apple-system, Segoe UI, sans-serif | 1rem / 1.6 |
| Metadata / nav | Inter, system-ui, sans-serif | .875–1rem / 1.4 |
| Tiny pixel label | `Press Start 2P`, monospace | .625–.75rem / 1.6, short labels only |

Do not use Press Start 2P for paragraphs, long navigation labels, form-like controls, project descriptions, or mobile body copy.

## Pixel-art rules

- Base UI pixel unit: 4 CSS px. Use multiples of 4 for spacing, offsets, borders, and sprite display sizes where practical.
- Use stepped corners via CSS pseudo-elements or clipped shapes; do not combine rounded, glassmorphism, and pixel borders in the same component.
- Border treatment: 2px solid `--border` plus a 2px offset shadow in `--bg` or `--cyan` only for emphasized controls.
- Decorative pixels must be grid-aligned and sparse; no full-page scanline overlay.
- Raster sprites, if approved, use integer scaling where possible and `image-rendering: pixelated`; do not apply it globally.
- Never pixelate profile photography or readable text.
- Decorative sprite dimensions: start with 16×16 or 32×32 source cells; document each asset’s source and license.

## Spacing and layout

| Token | Value |
| --- | --- |
| Page max width | 72rem (1152px) |
| Reading max width | 65ch |
| Desktop gutter | 2rem minimum |
| Mobile gutter | 1rem |
| Section space | `clamp(4rem, 10vw, 7rem)` |
| Card gap | 1rem mobile; 1.5rem desktop |
| Control height | 44px minimum touch target; 48px preferred |

Grid: one column by default; two columns only where parallel content remains understandable; project cards use 1 / 2 / 3 columns at increasing widths but never force narrow text columns.

## Component system

| Component | Appearance | Behavior |
| --- | --- | --- |
| Header/navigation | Solid surface bar with pixel divider. | Sticky after initial load; anchors scroll to sections; mobile menu is a normal button/menu. |
| Primary button | Cyan fill, dark text, 2px border, 2px pressed offset. | Hover brightens; active shifts down/right; visible keyboard focus. |
| Secondary button | Surface fill, cyan border. | Same accessible focus/pressed behavior. |
| Panel/card | Surface with stepped corners, thin border, small pixel corner marker. | Static by default; focusable only when it contains a link/control. |
| Project card | Status badge, concise description, technology tags, repository link. | Opens only through an explicit link/button; no hidden hover-only content. |
| Skill category | Text-first panel with compact icon slot. | No numeric ratings or animated bars. |
| Status badge | Compact, text plus color. | Meaning remains clear without color. |
| Featured credential | Amber-accent panel with provider, date, summary, verification link. | Prominent but visually consistent with other panels. |
| Timeline entry | Left marker and readable text. | Converts to simple stacked list on mobile. |
| Footer | Quiet surface with links and update note if needed. | No decorative motion required. |

## Interaction states

- Hover: color/outline shift and a maximum 2px offset, 150–180ms.
- Focus-visible: 3px cyan outer ring with 3px dark separation; never remove browser focus without replacement.
- Active: visual 2px press offset; must not move surrounding content.
- Disabled: muted contrast but still distinguishable; only use when a real disabled action exists.
- Reduced motion: disable nonessential transitions, pulses, sprite bobbing, and smooth scrolling using `prefers-reduced-motion`.

## Breakpoints

| Range | Intended behavior |
| --- | --- |
| Under 480px | Single column; text-first hero; menu collapsed; tags wrap; sprite decoration optional/hidden. |
| 480–767px | Single column with slightly larger gutters; projects remain stacked. |
| 768–1023px | Two-column supporting content; projects may use two columns. |
| 1024px and above | Full navigation; project grid up to three columns if text remains readable. |

## Asset usage guidelines

- Build borders, dots, gradients, shadows, dividers, and simple indicators in CSS.
- Use a licensed raster asset only when it communicates something CSS cannot: a small approved avatar, project screenshot, or limited decorative sprite.
- Optimize raster files, include alt text for meaningful images, and use empty alt text for purely decorative imagery.
- Font loading must use a system fallback, `font-display: swap`, and no more than two external font families.

