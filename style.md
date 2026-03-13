# Portfolio Style Guide

## Brand Direction
Warm editorial + modern product feel: light textured background, earthy accent color, rounded surfaces, and soft motion.

## Color System
Use these CSS variables as the base theme:

```css
:root {
  --bg: #f6f3ea;
  --surface: rgba(255, 255, 255, 0.72);
  --text: #1f1f1f;
  --muted: #5a5a5a;
  --line: rgba(31, 31, 31, 0.14);
  --brand: #c4562c;
  --brand-strong: #922f0b;
}
```

Additional background accents:
- Warm radial accent: `#f8ddb1`
- Green radial accent: `#d8efdf`
- Decorative blob 1: `#e0b86f`
- Decorative blob 2: `#8bc3a1`

## Typography
Google Fonts:
- Headings: `Fraunces` (`opsz,wght@9..144,600`)
- Body/UI text: `Space Grotesk` (`400,500,700`)

Type usage:
- `h1`, `h2`, `h3`: `Fraunces`, line-height `1.1`
- Body text and controls: `Space Grotesk`, line-height `1.6`
- Hero title size: `clamp(2.3rem, 6vw, 4.3rem)`
- Eyebrow/meta labels: uppercase + letter-spacing (`0.08em` to `0.12em`)

## Layout
Container:
- Width: `min(980px, calc(100% - 2.5rem))`
- Mobile width (<560px): `min(980px, calc(100% - 1.4rem))`

Section rhythm:
- Main stack gap: `1.2rem`
- Panel padding: `1.35rem`
- Panel radius: `20px` (mobile `14px`)

## Surfaces & Borders
Panel pattern:
- Background: `var(--surface)`
- Border: `1px solid var(--line)`
- Radius: `20px`
- Backdrop blur: `blur(4px)`

Card pattern:
- Background: `#fff`
- Border: `1px solid var(--line)`
- Radius: `16px`
- Padding: `1rem`

## Buttons & Links
Buttons:
- Pill shape: `border-radius: 999px`
- Padding: `0.72rem 1.15rem`
- Hover motion: `transform: translateY(-2px)`

Primary button:
- Background: `var(--brand)`
- Text: `#fff`
- Hover: `var(--brand-strong)`

Ghost button:
- Background: `#fff4`
- Text: `var(--text)`

Links:
- Default color: `var(--brand-strong)`
- Utility text link weight: `500`

## Motion
Entrance animation (`rise`):
- Duration: `750ms` to `920ms`
- Easing: `ease-out`
- Effect: fade in + `translateY(16px -> 0)`

Hover motion:
- Cards: lift `-4px`, shadow `0 12px 30px rgba(0, 0, 0, 0.08)`
- Buttons: lift `-2px`

## Background Style
Layered background formula:
1. Radial gradient at top-left (`#f8ddb1`)
2. Radial gradient at top-right (`#d8efdf`)
3. Base fill `var(--bg)`

Decorative fixed blurred shapes:
- One warm blob near upper-right
- One green blob near lower-left
- High blur (`35px`) and low opacity (`0.36`)

## Responsive Rules
Breakpoints:
- `@media (max-width: 860px)`: convert multi-column grids to 1 column
- `@media (max-width: 560px)`: tighten layout and allow button wrapping

Mobile behavior:
- Hero top padding reduced
- Grid content stacked
- Section headers can switch to vertical alignment

## Reuse Checklist
For a new project, copy this baseline first:
1. Root color variables
2. Font imports (`Fraunces` + `Space Grotesk`)
3. Container + panel + card primitives
4. Button system (`btn`, `btn-primary`, `btn-ghost`)
5. `rise` animation and hover transitions
6. Two breakpoints (`860px`, `560px`)
