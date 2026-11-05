# Design Direction Options

**Status:** Approved by owner on 2026-11-05. Direction A — Systems Console and its accompanying design decisions are the approved Phase 4 design baseline.

## Shared constraints

All directions retain the approved seven sections and use ordinary, keyboard-accessible page navigation. Pixel art supports the portfolio; it never hides content or replaces semantic controls.

## Direction A — Systems Console

**Concept:** A restrained technical console: dark workspace, compact pixel heading labels, modular information panels, and small status indicators. The feeling is a well-organized IT workstation rather than a game screen.

| Dimension | Proposal |
| --- | --- |
| Atmosphere | Calm, capable, technical, and professional. |
| Palette | Midnight navy, slate panels, electric cyan focus, amber highlight, off-white text. |
| Type | Pixelify Sans for display labels; Inter for all reading text. |
| Navigation | Standard sticky top navigation; compact “system menu” label on mobile. |
| Layout | Conventional one-page portfolio sections in a centered content column; projects receive the largest visual area. |
| Pixel treatment | 2px stepped corners, grid dots, tiny terminal-style metadata markers, pixel dividers. |
| Motion | Small button-press offset, status-light pulse only when motion is allowed. |
| Assets | CSS first; optional CC0 icon or panel accent only. |
| Strength | Most aligned with IT Support/Network Engineering direction and recruiter scanning. |
| Risk | Must avoid becoming a generic terminal imitation. |

**Reference lessons:** structured pixel UI from [Kenney UI Pack](https://kenney.nl/assets/ui-pack), content-first pixel portfolio from [The Pixel Portfolio](https://github.com/YoussefAhmedy/The_Pixel_Portfolio).

## Direction B — Network Operations Map

**Concept:** A light narrative layer built around a network topology: each section is a named node, connected by lines. The actual content remains in normal sections below or beside the map.

| Dimension | Proposal |
| --- | --- |
| Atmosphere | Exploratory, technical, network-focused. |
| Palette | Deep blue, monitor green, muted teal, signal amber, neutral white. |
| Type | Pixelify Sans headings; Inter body. |
| Navigation | Standard navigation plus optional “map” shortcut links. |
| Layout | Compact topology overview near Home; normal section layout thereafter. |
| Pixel treatment | Small network-device sprites, square node connectors, packet-like hover indicators. |
| Motion | Optional, slow packet dots along one decorative connection; never essential. |
| Assets | Could use CSS shapes; any device sprites require license review. |
| Strength | Directly connects Networking 2, IT Support, and Network Engineer goals. |
| Risk | Can misrepresent the portfolio as a networking-only site and complicate responsive layouts. |

**Reference lesson:** use exploration only as optional context, as in [pixel-world portfolio analysis](https://geekchamp.com/a-developer-portfolio-you-can-explore-fatima-zehra-shakeels-pixel-art-world/).

## Direction C — Pixel Field Journal

**Concept:** A brighter, warm “project journal” with notebook-like project entries, pixel stamps, and a small avatar/mascot space. It frames the portfolio as a student’s documented learning journey.

| Dimension | Proposal |
| --- | --- |
| Atmosphere | Friendly, personal, and handcrafted. |
| Palette | Warm parchment, deep ink, forest green, rust orange, muted blue. |
| Type | Press Start 2P for tiny labels only; Inter body and headings. |
| Navigation | Standard top navigation with section labels resembling tabs. |
| Layout | Editorial cards and short timelines; credential as a stamped featured card. |
| Pixel treatment | Stamps, small badge icons, stitched/stepped borders, sparse dithering. |
| Motion | Optional stamp-in reveal and hover lift. |
| Assets | More illustration-dependent; a custom avatar would need explicit approval. |
| Strength | Makes student status approachable and highlights ongoing learning. |
| Risk | Least aligned with the desired technical/IT professional impression if over-decorated. |

## Comparison

| Criterion | A: Systems Console | B: Network Operations Map | C: Pixel Field Journal |
| --- | --- | --- | --- |
| Recruiter scanability | High | Medium | High |
| IT Support / Network Engineer alignment | High | Very high | Medium |
| Project detail support | High | Medium | High |
| Mobile complexity | Low | High | Medium |
| Asset dependence | Low | Medium | Medium/high |
| Accessibility risk | Low | Medium | Medium |

## Selected direction — Direction A: Systems Console

Direction A best balances professional clarity and pixel-art identity. It supports the approved content hierarchy, emphasizes technical projects and credentials, works naturally on small screens, and can be implemented with PHP, CSS, and small vanilla-JavaScript enhancements. It also avoids implying game-development experience or requiring game-like navigation. **The owner approved this direction on 2026-11-05.**

Direction B can be reconsidered as an optional Home illustration later, but should not control navigation. Direction C is a valid alternate if the owner wants a warmer, less technical tone.

## Original low-fidelity concept board — Direction A

```text
DESKTOP
┌───────────────────────────────────────────────────────────────────┐
│ JP ASUNCION  [ABOUT] [SKILLS] [PROJECTS] [EDU] [CERTS] [CONTACT] │
├───────────────────────────────────────────────────────────────────┤
│  [SYSTEM STATUS: LEARNING / BUILDING]                              │
│  JOHN PATRICK ASUNCION                                             │
│  BSIT STUDENT | SOFTWARE DEVELOPMENT | NETWORKING & AI            │
│  [ VIEW PROJECTS ]  [ VIEW CREDENTIALS ]      ▣ pixel motif        │
├───────────────────────────────────────────────────────────────────┤
│  ABOUT                         SKILLS / CURRENT LEARNING          │
│  concise copy                  categorized, no ratings             │
├───────────────────────────────────────────────────────────────────┤
│  FEATURED WORK                                                    │
│  [ LIBRASYS ] [ RW PC TRADING ] [ EVENTFLOW ] [ NETWORKING 2 ]   │
├───────────────────────────────────────────────────────────────────┤
│  EDUCATION                  [ FEATURED: GOOGLE IT SUPPORT ]       │
├───────────────────────────────────────────────────────────────────┤
│  CONTACT: email · GitHub · LinkedIn                                │
└───────────────────────────────────────────────────────────────────┘

MOBILE: menu → hero → quick highlights → projects → about → skills →
education → credentials → contact. Cards stack; no horizontal scrolling.
```

This is an original content/layout diagram, not a final visual mockup or implementation.

## Approved design decisions

1. The dark navy/cyan/amber Systems Console palette is approved.
2. Pixelify Sans for display headings and Inter for body text are approved.
3. No avatar or mascot is included by default.
4. CSS-first visuals with optional CC0 asset fallback are approved. No assets are selected or downloaded yet.
5. The website is dark-mode only; a light mode is not required.
6. No sound effects are included by default.

