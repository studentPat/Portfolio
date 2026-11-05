# UI/UX Specification — Proposed Systems Console

**Status:** Approved by owner on 2026-11-05 as the Phase 4 UI/UX baseline. No implementation is authorized until the next phase is planned and approved.

## Overall experience

The experience is a professional single-page portfolio with an optional pixel-art systems-console layer. A visitor should identify John Patrick Asuncion, his direction, and the strongest project/credential evidence in the first screenful; every section is reachable through standard navigation without game mechanics.

## Global navigation

- Desktop: persistent header links to Home, About, Skills, Projects, Education, Certifications, and Contact.
- Mobile: labelled menu button; expanded links are large enough for touch, keyboard reachable, and close on navigation.
- Current section: visible text/outline state; do not depend on color alone.
- Skip link: first keyboard-focusable item, jumping to main content.
- Anchor navigation works with JavaScript disabled; JavaScript may only enhance active-section indication.

## Section specifications

| Section | Purpose and priority | Layout / components | Pixel treatment and responsive behavior | Interaction |
| --- | --- | --- | --- | --- |
| Home | Establish identity, student status, career direction, and two paths forward. | Identity block, short introduction, primary/secondary CTA, 3 verified highlights. | Small console status label and sparse 16px decorative blocks. On mobile, stack CTAs full width. | CTA anchors scroll to Projects and Certifications. |
| About | Explain education, practical learning path, interests, and goal without repeating project detail. | Reading-width copy with compact fact list. | One quiet panel and divider, no busy background. Mobile stays single column. | No required animation. |
| Skills | Separate demonstrated skills from current learning. | Categorized cards/lists with evidence-oriented wording. | Small category glyph slot only if an approved asset/CSS icon exists. Cards stack on mobile. | No ratings, progress bars, or hover-only information. |
| Projects | Primary proof of work; prioritize LibraSys, RW PC Trading, EventFlow, Networking 2. | Consistent project cards: status, short description, technologies, GitHub link; optional expandable detail area. | Project cards share panel system; no mandatory screenshots. Grid becomes one column on small screens. | Explicit “View source” links; optional disclosure uses button semantics and works without animation. |
| Education | Confirm academic context concisely. | Single timeline/list entry. | Tiny pixel timeline marker, text remains conventional. | Static. |
| Certifications | Give the Google IT Support Professional Certificate prominent but accurate treatment; list supporting courses. | Featured credential panel plus supporting-course list/table. | Amber accent reserved for featured credential. On mobile supporting list becomes stacked rows. | Verification links open clearly labelled destinations. |
| Contact | Make professional channels effortless to locate. | Email, GitHub, LinkedIn as labelled links and a short invitation. | Minimal footer-like panel; no animated email envelope or custom cursor. | Normal links, keyboard focus, visible external-link context where needed. |

## Project detail model

Each project card must show: project name, approved short description, status, technology list, and GitHub repository. Expanded content may show the approved detailed description and implementation notes. No live-demo button for RW PC Trading; no inferred team role, metrics, or unapproved images.

## Original content wireframe

```text
Header / skip link
  Home identity + CTAs
  About narrative + education facts
  Skills: demonstrated | currently learning
  Projects: ordered cards
  Education: one concise entry
  Certifications: featured credential + supporting list
  Contact: email | GitHub | LinkedIn
Footer
```

## Interaction and animation plan

| Interaction | Trigger and result | Purpose | Essential? | Technology |
| --- | --- | --- | --- | --- |
| Pixel button press | Pointer/keyboard activation; 2px press offset. | Affordance. | No. | CSS. |
| Panel hover | Pointer hover; minor border/accent shift. | Clarify linked cards. | No. | CSS. |
| Active navigation | Scroll/anchor change; current-section marker updates. | Orientation. | No; all links work without it. | Optional vanilla JS. |
| Project disclosure | Explicit button; details expand/collapse. | Keeps project grid scannable. | No; details may be visible initially if JS absent. | HTML/CSS plus optional JS. |
| Decorative status pulse | Low-frequency pulse in hero only. | Adds pixel identity. | No. | CSS; disabled for reduced motion. |
| Sound | None by default. | Avoid distraction and accessibility risk. | N/A. | N/A. |

## Responsive requirements

- Never require horizontal scrolling at 320px viewport width.
- Use content order, not visual position alone, to convey hierarchy.
- Maintain 44px minimum interactive targets and 16px minimum readable body text.
- Let technology tags wrap rather than shrink to unreadable text.
- Hide decorative-only sprites before hiding content or controls.
- Preserve explicit labels beside icons on all viewport sizes.

## Accessibility requirements

- Semantic landmarks: header, nav, main, section, footer.
- One logical H1; nested headings follow order.
- All controls operable by keyboard; no mouse-only or hover-only information.
- High-contrast text/background pairings; status names supplement color.
- Meaningful images receive specific alt text; decorative pixels receive empty alt text or CSS rendering.
- Respect `prefers-reduced-motion`; no flash, autoplay sound, or animation-dependent content.
- Use direct text links for GitHub, LinkedIn, email, and certificates.

## Technical compatibility

| Concern | Proposed implementation boundary |
| --- | --- |
| Shared document frame | Reusable PHP includes for header, footer, and optional project-card data/view structure. |
| Layout and design | CSS custom properties, grid, flexbox, media queries, pseudo-elements; no framework. |
| Enhancement | Vanilla JavaScript for menu state, optional active navigation, and optional project disclosures. |
| Content baseline | Semantic HTML links and sections work without JavaScript. |
| Assets | `assets/images/`, `assets/sprites/`, `assets/fonts/` only after approval, with per-asset license record. |

## Acceptance criteria for a future implementation plan

- The seven approved sections and approved copy are all present.
- Direction A visual rules are applied consistently without external assets being required.
- Navigation, keyboard focus, responsive layout, reduced motion, and link labels pass manual checks.
- No unapproved live demo, project claim, personal detail, visual asset, or animation is introduced.

