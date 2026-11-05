# Design Research

**Phase:** 4 — UI/UX and Design Planning  
**Status:** Research baseline supporting the approved Systems Console direction. No external reference or asset is copied, downloaded, or approved for direct use.

## Research methodology

Research focused on four questions: how pixel art can be recognizably intentional rather than decorative, how a portfolio remains easy for recruiters to scan, which assets have clear reusable licenses, and how the final site can remain accessible on mobile and with reduced motion. Sources were reviewed in November 2026. A reference is inspiration, not a template to copy.

## Website references

| Reference | Type and observable approach | Useful lesson | Do not adopt |
| --- | --- | --- | --- |
| [Pixel / 8-bit Web Design Showcase](https://design-styles.enlighten-media.net/pages/pixel-art/) | Design-style gallery; identifies grid-constrained images, limited palettes, sprite composition, and chunky type as core characteristics. | Establish one grid, one palette, and a deliberate pixel scale before adding decorative sprites. | A fully 8-bit treatment of every paragraph or control; this would reduce readability. |
| [YN10, via the showcase](https://design-styles.enlighten-media.net/pages/pixel-art/) | Personal portfolio rendered as a pixel-art environment, including navigation and illustrations. | A personal portfolio can use a consistent world metaphor. | Requiring exploration before visitors can find projects, contact information, or credentials. |
| [Youssef Ahmedy Pixel Portfolio](https://github.com/YoussefAhmedy/The_Pixel_Portfolio) | Developer portfolio with pixel borders, dithering, a pixel cursor, responsive layouts, project details, and light/dark modes. | Let standard portfolio hierarchy lead; apply pixel borders and texture as a layer over it. | A custom cursor as a usability requirement, or copying its visual system. |
| [Peter Oravec](https://peteroravec.com/) | Interactive developer portfolio that uses a pixel-art world and project paths. | An interactive world can create memorable context when there is also direct access to conventional portfolio content. | A game engine or a map-first experience; it adds complexity beyond this PHP/vanilla stack. |
| [Fatima Zehra Shakeel portfolio analysis](https://geekchamp.com/a-developer-portfolio-you-can-explore-fatima-zehra-shakeels-pixel-art-world/) | Island-map portfolio where locations represent career areas. | A spatial metaphor can organize a journey, but content must stay directly reachable. | Making navigation a puzzle or hiding a résumé-like summary behind interactions. |

### Research conclusion

The professional pattern is **content first, pixel art second**: ordinary navigation, semantic sections, clear status labels, readable body text, and optional visual flavor. Pixel elements should signal technical craft and learning, not imply that the portfolio is a game-development portfolio.

## Asset-kit research

| Asset / source | Includes and technical format | License / cost | Potential use | Selection |
| --- | --- | --- | --- | --- |
| [Kenney UI Pack](https://kenney.nl/assets/ui-pack) | 430 UI assets: panels, buttons, sliders and interface elements; PNG/spritesheet-style assets. | CC0; free; attribution not required. [License policy](https://kenney.nl/support) | Optional small decorative icons, dividers, or a single panel motif. | Recommended only after visual compatibility review. |
| [Kenney Pixel UI Pack on OpenGameArt](https://opengameart.org/content/pixel-ui-pack-750-assets) | 750 UI tiles: panels, buttons, pointers, bars, checks, scrollers; 9-slice PNGs and spritesheets. | CC0; free; attribution optional. | Strong technical fallback if CSS-only panel treatment proves insufficient. | Recommended fallback. |
| [Retro UI Kit Lite — Willosuna](https://willosuna.itch.io/retro-ui-kit-lite) | 30 free pieces: CRT panel, dialog, buttons, cursor, slots, keys, speech bubble; ZIP/PNG. | Name-your-price; page states free for commercial use. Keep its included license file with the download. | Optional prototype/reference for button-state and panel ideas. | Needs verification before download/use. |
| [Minimalist Game GUI](https://opengameart.org/content/minimalist-game-gui) | Minimal pixel UI; PSD source. | CC0; free; credit not required. | Reference for restrained green/grey UI treatment. | Optional; PSD adds workflow friction. |
| [Pixel UI Kit — barkino](https://opengameart.org/content/pixel-ui-kit) | Green/grey pixel UI elements; ZIP. | CC0; free. | Potential icons or prototype-only UI details. | Optional. |

### Asset license rules

- No asset may be downloaded or committed during Phase 4.
- Prefer CSS-made borders, blocks, and states where possible; this avoids stylistic mismatch and attribution overhead.
- If any asset is selected later, retain its original URL and license text in the repository.
- Recheck the original download page and included license at download time. Search snippets are not a substitute for the packaged license.
- Do not use unverified preview images, character sprites, sound effects, or third-party logos.

## Typography, color, and technical resources

| Resource | Research finding | Design application |
| --- | --- | --- |
| [Google Fonts: Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P) | Strong pixel display typeface; compact and difficult at paragraph sizes. | Optional display-only font for very short labels, badges, and section markers; not body copy. |
| [Google Fonts: Pixelify Sans](https://fonts.google.com/specimen/Pixelify+Sans) | Pixel-inspired display face with more flexible sizes. | Preferred display heading candidate; verify final rendering and license/loading details at implementation. |
| [Google Fonts: Inter](https://fonts.google.com/specimen/Inter) | Conventional UI/body family with strong screen readability. | Recommended body, navigation, metadata, and long-form project copy. |
| [Lospec Palette List](https://lospec.com/palette-list/) | Downloadable pixel-art palettes in HEX and multiple formats. | Reference for constrained palettes; the proposed colors below are original selections, not copied palette assets. |
| [MDN: image-rendering](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/image-rendering) | `image-rendering: pixelated` preserves hard edges for scaled pixel art; non-integer scaling can look uneven. | Apply only to actual raster sprites at integer-oriented sizes, never to photos, icons intended to be smooth, or text. |
| [MDN: reduced motion](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/%40media/prefers-reduced-motion) | `prefers-reduced-motion` supports minimizing non-essential animation. | All planned motion must have a reduced-motion alternative. |

## Recommended research outcome

Use a CSS-first design with a small number of optional, CC0-compatible pixel assets. The baseline must look complete with no external asset pack. This creates a professional site that is fast, maintainable, and legally simple.

## Rejected approaches

- A mandatory canvas/game-world navigation system: harms direct access and accessibility.
- Full CRT scanlines over body text: harms readability and can cause visual fatigue.
- Pixel fonts for all text: poor mobile and paragraph readability.
- A custom cursor: inaccessible/awkward on touch devices and unnecessary.
- Autoplay sound or music: not appropriate for a professional portfolio.

