---
version: alpha
name: selba website
description: Website foundations, components, patterns, and combinations documented from the selba Figma library.
---

# selba website design system

## Overview

selba makes room for “I can do it myself.” The website combines expressive Selba display titles, clear Figtree text, family photography, playful drawn icons, and generous spacing. It addresses parents and caregivers in German-speaking DACH while keeping children’s participation at the center. Apply the intent, evidence boundaries, and naming rules in [BRAND.md](../../BRAND.md).

**Documented:** 2 November 2026. **Owner:** Max Pinkert. **Scope:** the supplied [Atoms page](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=0-1) and [Web page](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=1-2). 

### How to use this document

- Figma defines the visual designs. Preserve its combinations, colors, sizing, and state differences as intentional. This document records them; it does not redesign them.
- [digital.md](../../assets/colors/digital.md) owns palette names and exact values. Map Figma’s legacy names by value, as described below, without changing the appearance.
- Measurements describe the supplied reference frames and components. They do not establish breakpoints, maximum page widths, or fixed content heights at every viewport.
- YAML keys for typography and component recipes below are document identifiers for observed Figma styles and combinations, not a claim that identically named variables already exist in Figma. Numeric spacing and radius keys retain the existing variable names.
- “To be defined” means the supplied sources do not establish a decision. Do not fill these gaps with assumed behavior.

### Source and asset references

| Source | Role |
| --- | --- |
| [Brand foundation](../../BRAND.md) | Audience, purpose, promises, brand name, core message, and evidence boundaries |
| [Digital palette](../../assets/colors/digital.md) | Canonical color tokens |
| [Fonts](../../assets/fonts/) | Supplied Selba and Figtree font files |
| [Logo](../../assets/logo/) · [Icons](../../assets/icons/) | Reusable SVG artwork |
| [Imagery](../imagery.md) · [Image assets](../../assets/imagery/) | Photography direction and supplied images |
| [Illustrations](../illustrations.md) · [Illustration assets](../../assets/illustrations/) | Supporting editable overlays and preview composites |
| [Tone and voice](../tone-and-voice/tone-and-voice.md) | Public-facing copy guidance |

The foundation’s reference-map statements that asset folders are empty and digital/print files are placeholders predate the current asset inventory. Use the actual files linked here. This website document does not infer product capabilities from imagery, filenames, price samples, or placeholder text.

## Colors

Use the existing palette without introducing replacement hues:
[digital.md](../../assets/colors/digital.md)

Changes originate in digital.md.

### Designed combinations

| Pattern | Surface | Text / foreground |
| --- | --- | --- |
| Neutral hero, product section, FAQ | `screen` | `ink` |
| Morning hero | `morning` | `screen` |
| Day hero | `day` | `screen` |
| Night hero | `night` | `screen` |
| Brand hero | Photography and the source gradient treatment | `screen` title and logo |
| CTA band | `night-sand` | `screen` heading/body; white filled button with `ink` label |
| Steps | `night-sand`, `night-sage`, `night-lavender`, `night` panels | `screen` |
| Testimonial cards | `day`, `morning`, `night` | `screen` |
| Footer | `ink` | `screen` |

These are the intended combinations in the supplied Figma designs. Palette groups do not imply automatic light/dark themes or status colors. The three-color testimonial row is a specific website combination; it does not change the separate palette restrictions for illustration overlays.

## Typography

**Selba Bold** carries expressive display titles. **Figtree** carries the Heading 1–6 styles, body copy, navigation, button labels, captions, and supporting information. This division is the owner-confirmed brand direction. Figtree also remains the fallback when Selba is unavailable.

Use the supplied [Selba Bold WOFF2](../../assets/fonts/Selba/Selba-Bold.woff2) and [Figtree Latin variable WOFF2](../../assets/fonts/Figtree/figtree-latin-wght-normal.woff2), [Latin extended](../../assets/fonts/Figtree/figtree-latin-ext-wght-normal.woff2) and [italic](../../assets/fonts/Figtree/figtree-latin-wght-italic.woff2) files are also available. Their availability does not add italic roles to the current website style inventory.

### Observed type scale

Source: [Typography](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=7-150). All listed styles have zero percent letter spacing. Line heights below convert Figma percentages to unitless multipliers.

| Figma style | Document token | Family / weight | Size | Line height |
| --- | --- | --- | --- | --- |
| Title | `title` | Selba / 700 | 96px | 1.1 |
| Title (S) | `title-s` | Selba / 700 | 64px | 1.1 |
| Title (XS) | `title-xs` | Selba / 700 | 40px | 1.1 |
| Heading 1 | `heading-1` | Figtree / 400 | 96px | 1.2 |
| Heading 2 | `heading-2` | Figtree / 400 | 64px | 1.2 |
| Heading 3 | `heading-3` | Figtree / 400 | 40px | 1.2 |
| Heading 4 | `heading-4` | Figtree / 400 | 32px | 1.2 |
| Heading 5 | `heading-5` | Figtree / 400 | 24px | 1.2 |
| Heading 6 | `heading-6` | Figtree / 400 | 20px | 1.2 |
| Body - Tall | `body-tall` | Figtree / 400 | 20px | 1.4 |
| Body - Bold | `body-bold` | Figtree / 900 | 16px | 1.2 |
| Body | `body` | Figtree / 400 | 16px | 1.4 |
| Body Small | `body-small` | Figtree / 400 | 12px | 1.2 |
| Captions | `captions` | Figtree / 400 | 8px | 1.2 |

```yaml
typography:
  title:
    fontFamily: Selba
    fontSize: 96px
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: 0em
  title-s:
    fontFamily: Selba
    fontSize: 64px
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: 0em
  title-xs:
    fontFamily: Selba
    fontSize: 40px
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: 0em
  heading-1:
    fontFamily: Figtree
    fontSize: 96px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0em
  heading-2:
    fontFamily: Figtree
    fontSize: 64px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0em
  heading-3:
    fontFamily: Figtree
    fontSize: 40px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0em
  heading-4:
    fontFamily: Figtree
    fontSize: 32px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0em
  heading-5:
    fontFamily: Figtree
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0em
  heading-6:
    fontFamily: Figtree
    fontSize: 20px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0em
  body-tall:
    fontFamily: Figtree
    fontSize: 20px
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 0em
  body-bold:
    fontFamily: Figtree
    fontSize: 16px
    fontWeight: 900
    lineHeight: 1.2
    letterSpacing: 0em
  body:
    fontFamily: Figtree
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 0em
  body-small:
    fontFamily: Figtree
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0em
  captions:
    fontFamily: Figtree
    fontSize: 8px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0em
```

Desktop heroes use `title`; the mobile Brand hero and A patterns use `title-s`; mobile B patterns, the product name, and CTA title use `title-xs`. Buttons use `body-tall`, `body`, and `body-small` for Large, Default, and Small respectively. FAQ questions use `heading-6` and answers use `body`. Match these roles rather than treating every visually prominent heading as Selba.

## Layout

### Reference grids

Source: [Layouts](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=7-236).

| Reference | Frame width | Columns | Outer margin | Gutter | Inner width |
| --- | --- | --- | --- | --- | --- |
| Web | 1280px | 12 stretch columns | 96px | 24px | 1088px |
| Mobile | 375px | 6 stretch columns | 24px | 12px | 327px |

Website hero specimens are 1280 × 720px on desktop and 375 × 800px on mobile. No tablet breakpoint, desktop maximum width, fluid interpolation rule, or viewport-height rule is supplied.

### Spacing

Source: [Spacing](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=7-171). Preserve the actual scale: 4, 8, 12, 16, 24, 40, 64, 96, and 144px. Do not replace it with a generic 8px scale or add 32/48px spacing tokens merely because those numbers occur elsewhere as text sizes or component dimensions.

```yaml
spacing:
  "4": 4px
  "8": 8px
  "12": 12px
  "16": 16px
  "24": 24px
  "40": 40px
  "64": 64px
  "96": 96px
  "144": 144px
```

Product, FAQ, Video, and Steps desktop sections have 96px outer padding. Testimonials use 96px horizontally and 64px vertically. The footer uses 96px horizontally and 40px vertically. Navigation uses 24px padding. These are distinct patterns, not a single universal section-padding rule.

Auto-layout groups preserve related content: title/body/action stacks; horizontal button groups; gallery/thumbnail stacks; FAQ lists; and card rows. Source-specific dimensions and distributed alignment remain local to their components. Values such as the 210px gap between the two product columns are composition measurements, not additions to the shared spacing scale.

## Elevation & Depth

The inspected website patterns use flat surfaces, whitespace, image crops, outlines, and color blocks. No shadow scale is established. Preserve the existing 1px secondary-button borders, 1px FAQ dividers, and 4px outside hover strokes on filled buttons.

Brand hero nodes contain a photograph and an `ink` radial gradient at 50% paint opacity, with stops from opaque `ink` to 20%-opacity `ink`. Mobile B heroes contain a photograph and a linear gradient with the reverse stop order, also at 50% paint opacity. Preserve each source node’s paint order, gradient transform, crop, and resulting appearance; do not substitute a generic CSS overlay from this abbreviated description.

UI gradient and hover-opacity treatments do not extend to illustration overlays. The [illustration guideline](../illustrations.md) specifies flat, opaque drawing layers with transparent unused space.

## Shapes

Source: [Radius](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=7-166).

```yaml
rounded:
  "4": 4px
  "8": 8px
  "16": 16px
  full: 9999px
```

- **4px:** action buttons, main product-gallery image, and the image window inside the expanded Steps panel.
- **8px:** available foundation radius; no additional website role is assigned here.
- **16px:** mobile A image window, dropdown container and image window, Steps panels, and testimonial cards.
- **Full:** feature pills beneath the product gallery.
- **Square:** full-width section surfaces and navigation-link containers retain their observed zero radius. Zero is an observed property, not an additional Figma radius variable.

Logo and icon outlines come from supplied SVG artwork. Preserve their proportions and hand-drawn character; do not replace them with text approximations or another icon family.

## Components

### Component inventory

| Figma set | Source | Available variants |
| --- | --- | --- |
| Button | [16:2891](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=16-2891) | 32 variants: filled, outlined, and navigation patterns |
| Hero | [28:3928](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=28-3928) | 14 variants: 5 Web, 1 Mobile Brand, 4 Mobile A, 4 Mobile B |
| Navbar | [44:9823](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=44-9823) | Default and Dropdown |
| FAQ | [49:9915](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-9915) | Question-only and question-with-answer appearances |
| Sections | [49:10114](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10114) | Product, FAQ, Video, CTA, Steps, Testimonial, Footer |
| Logo | [2:84](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=2-84) | default / 1:1 / 1:2 × ink / screen / color × Large / Default / Small |
| Icons | [36:8227](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=36-8227) | Supplied artwork in screen, ink, and primary |

### Buttons

The property axes are `Type`, `Color`, `Size`, and `State`. The set also exposes `IconLeft`, `IconRight`, `Text`, `Subtext`, a text `Label`, and an `Icon` instance swap. Use the actual available combinations, not an assumed full Cartesian product:

| Type | Colors | Sizes | States |
| --- | --- | --- | --- |
| Primary (filled) | Primary, Screen, Ink | Large, Default, Small | Default, Hover |
| Secondary (outlined) | Screen, Ink | Large, Default, Small | Default, Hover |
| Navigation | Screen | Default | Default, Hover |

Primary color buttons use `primary` with `screen` text. Screen filled buttons use `screen` with `ink` text; Ink filled buttons use `ink` with `screen` text. Secondary Screen and Ink buttons have transparent default fills and matching 1px borders and text. Primary hover adds a 4px outside stroke in the fill color at 20% opacity. Secondary hover adds a 20%-opacity fill in its border color while retaining the 1px border.

| Size | Text | Filled padding, vertical / horizontal | Outlined padding, vertical / horizontal | Gap | Icon size in source |
| --- | --- | --- | --- | --- | --- |
| Large | 20px / 1.4 | 20 / 40px | 19 / 40px | 12px | Filled 24px; outlined 16px |
| Default | 16px / 1.4 | 16 / 24px | 15 / 24px | 8px | 16px |
| Small | 12px / 1.2 | 12 / 16px | 11 / 16px | 8px | 12px |

With both icons visible, filled specimens measure 64, 48, and 36px high; outlined specimens measure 56, 48, and 36px. The **Large Primary-color hover** specimen intentionally uses 16px icons and measures **56px** high versus **64px** in Default. Preserve this difference. Large Screen and Ink filled hover specimens remain 64px high.

Height depends on the visible children in the source: text-only instances are smaller, including the 32px-high Small navigation CTA, 43px-high Default hero buttons, and 54px-high Large product CTA. Do not impose one fixed height across all instances or use text-layer ink bounds as CSS line-height values.

Navigation is a separate text-and-description pattern with a 12px label, directional icon, optional 8px subtext, and 8px internal gap. Its outer padding is 12px vertically and 16px horizontally. Hover changes the label to weight 900 and changes its measured width. The `Color=Screen` variant name does not mean all nested text is white: the standalone sample uses `ink`; footer instances supply the light treatment shown in the composition.

Pressed, focus, disabled, loading, and icon-only interaction specifications are **to be defined**. The presence of a Hover variant does not establish its animation timing.

### Hero patterns and combinations

All hero recipes reuse the Button and typography foundations. The Brand hero combines full-bleed family photography, a centered Selba title, two actions, and the horizontal white logo near the bottom. Its desktop title group is 738px wide, with 64px between title and actions. The mobile Brand composition has a 327px-wide content group, 64px top padding, and a 125 × 40px logo.

The Web Neutral/Morning/Day/Night pattern is a text-and-image split: a 439px-wide text column at x=96, and a 535px-wide portrait image at x=745 extending to the right edge. The source portrait is 803px high and cropped by the 720px hero. The text column uses 96px top/bottom padding, a 64px title-to-content gap, and a 40px body-to-actions gap. Neutral shows a filled primary action plus an outlined Ink action; the range-colored desktop variants show one filled primary action.

| Type | Web | Mobile A | Mobile B | Surface token |
| --- | --- | --- | --- | --- |
| Brand | `28:3927` | Mobile Default `28:3922`; no A/B pair | — | Photograph |
| Neutral | `28:3926` | `28:3916` | `28:3919` | `screen` |
| Morning | `28:3924` | `28:3915` | `28:3920` | `morning-blue` |
| Day | `28:3923` | `28:3914` | `28:3918` | `day-coral` |
| Night | `28:3925` | `28:3921` | `28:3917` | `night` |

Each ID resolves in the [Hero set](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=28-3928). Preserve the differences between these compositions:

- **Mobile A:** 24px side inset; a 327 × 327px image window with 16px radius; a 64px Selba title; body copy and a Small primary action beneath. Morning/Day/Night use 24px configured spacing and 40px bottom padding; Neutral has its own 66px configured spacing and 24px bottom padding. Preserve the source distribution rather than forcing identical vertical positions across variants.
- **Mobile B:** full-width photographic background with a small action at the lower-right edge of the image area; a full-width colored text panel begins at y=525 in the 800px specimen. The panel is 275px high, with 40px vertical and 24px horizontal padding, a 40px Selba title, and body text. The action sits above the panel, not below the description.

**A/B test requirement:** retain both A and B for Neutral, Morning, Day, and Night. Run an A/B test before choosing a winning mobile pattern. No winner is established. Test objective, primary metric, eligible traffic, allocation, tracking, duration/sample requirements, and decision rule are **to be defined**. The supplied variants differ in imagery treatment, title size, and action placement; document the tested combination so results are not attributed to a single isolated change.

### Navigation

Default (`44:9822`) is 1280 × 88px on `screen`, with 24px padding, a 32 × 32px color 1:1 logo at left, and “Produkte”, “Über uns”, and a Small Primary action at right. Navigation spacing is 24px between the link group and CTA.

Dropdown (`44:9821`) combines the same top bar with a 24px gap and a 1280 × 280px white panel with 16px radius. The panel has 96px horizontal and 40px vertical padding. It combines three range destinations, short descriptions, and a 200px square rounded image. The groups are labeled “morgens”, “tagsüber”, and “abends”, using the Morning blue, Day coral, and Night colors respectively.

Opening/closing triggers, keyboard behavior, sticky positioning, overlay behavior, destinations, and mobile navigation are **to be defined**. The displayed labels establish the pattern, not published routes or product availability.

### Product section

Source: [Type=Product, 49:9884](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-9884). Reference size: 1280 × 814px; white surface, 96px padding, two 439px columns separated by 210px.

The left column combines a gallery and three feature pills, separated by 40px. The main image is 439 × 300px with 4px radius. Five 69 × 47px thumbnails sit below with an 8px gallery-to-thumbnail gap and 24px thumbnail gaps. The source repeats the same photograph; do not invent a completed five-image product set. Feature pills are 439 × 65px, `night-sand`, full radius, 16px vertical / 24px horizontal padding, 16px icon-to-text spacing, and an Ink asterisk icon. Pills are separated by 16px.

The right column combines a range label, 40px Selba product name, description, price, and a full-column-width Large Primary purchase button aligned near the bottom. “Schlafsteine”, “abends”, “39,90 €”, and “Jetzt kaufen” are visible sample content. The price and product facts require a current verified product source before publication; this design document does not establish them.

Gallery selection behavior, thumbnail active states, checkout destination, stock behavior, and mobile composition are **to be defined**.

### FAQ item and section

[FAQ items](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-9915) retain the source names `Property 1=Frame 48` (`49:9914`, question-only) and `Property 1=Frame 49` (`49:9913`, question and answer). They visually represent collapsed and expanded content; these descriptions are not renamed Figma properties.

Items use a 20px question, 16px body answer, a 24px question-to-answer gap, and a 16px Ink chevrons icon separated from the text column by 64px. Standalone specimens are 745px wide; the question-only specimen is 16px high and the answer specimen 71px with its current copy. Content determines height.

[Type=FAQ, 49:10113](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10113) is a 1280 × 669px white section with 96px padding. It contains a centered 718px-wide list of five items, four closed and one open, with 1px Ink dividers and 40px gaps between list children. Single-open versus multiple-open behavior, animation, keyboard interaction, final questions/answers, and mobile layout are **to be defined**.

### Video / full-width media

[Type=Video, 53:10756](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=53-10756) is 1280 × 669px and currently contains a photographic fill with no child controls. Document this visual media pattern as supplied. A video file, playback controls, autoplay/mute/loop rules, captions, poster behavior, and mobile treatment are **to be defined**. The component name alone does not specify a working player.

### CTA band

[Type=CTA, 49:10157](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10157) combines a `night-sand` surface, white copy, a white filled button with Ink text/chevrons, and a large cropped product image on the right. Reference size: 1280 × 307px. The left inset is 96px; the 625px copy column has 40px top/bottom padding, 24px between title and body, and 40px to the button. The 559px right image window crops the larger product artwork. Preserve this crop rather than shrinking the entire image to fit.

The displayed title is “Schritt für Schritt / Block für Block.” Use `title-xs`, `body-tall`, and the Default Screen filled button. Final copy, action destination, and mobile arrangement are **to be defined**.

### Steps panels

[Type=Steps, 49:10301](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10301) is a 1280 × 745px section with 96px padding and 24px gaps. It combines four 553px-high, 16px-radius panels: three narrow 161px panels and one expanded 532px panel. Preserve the source widths and placement, including their local rounding, rather than recalculating the entire component from a generic grid.

The sequence uses `night-sand`, `night-sage`, `night-lavender`, and `night`; the lavender panel is expanded in the supplied composition. Narrow panels combine a 32px Screen alarm-clock icon with a rotated 32px title. The expanded panel has 40px padding, a small icon/label row, 32px heading, 16px body, a Small outlined Screen “Mehr erfahren” action, and a cropped 452 × 144px photograph with 4px radius. The source photo extends beyond its clipped window.

This is a designed combination of compact and expanded panels. Switching behavior, trigger, animation, alternate expanded states, and mobile arrangement are **to be defined**; no working accordion is implied by the screenshot alone.

### Testimonials

[Type=Testimonial, 49:10302](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10302) combines three 347 × 175px cards with 24px gaps in a 1280 × 303px white section. Each card has a 16px radius, 24px vertical / 40px horizontal padding, and 16px spacing between rating, quote, and attribution. Card colors are Day coral, Morning blue, and Night, with white content.

Use the supplied outlined star and person artwork. Preserve the source’s differing star counts; they are sample rating layouts, not evidence of customer ratings. Quotes and “Mama einer Tochter” attribution are placeholder examples. Real quotes, attribution, rating provenance, and mobile layout are **to be defined**. Do not populate this pattern with persona simulations or invented testimonials.

### Footer

[Type=Footer, 49:10755](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10755) is 1280 × 320px on Ink, with 96px horizontal / 40px vertical padding. It combines:

- A white horizontal logo, a short 12px brand paragraph, and an 8px legal-link row with 12px gaps.
- Product and resource link groups using the Navigation label/description pattern and directional icons, with 24px between groups.
- Social marks above a rounded portrait crop.

The source legal labels are Impressum, Datenschutz, AGBs, and Sicherheit; resource labels are Über uns, Blog, and Hilfe. Preserve the displayed hierarchy. Legal copy, routes, social profile destinations, exported social-mark assets, and mobile composition are **to be defined**.

### Reuse and asset mapping

Paths below are relative to this document. Match the source frame’s crop and logo variant; filenames alone do not authorize a different composition.

| Designed use | Existing asset |
| --- | --- |
| Brand desktop hero / full-width media scene | [01-family-a-building-landscape.png](../../assets/imagery/brand/01-family-a-building-landscape.png), visually matched to the family/building scene |
| Mobile Brand/B, dropdown, footer portrait scene | [02-family-a-drawing-portrait.png](../../assets/imagery/brand/02-family-a-drawing-portrait.png); footer layer explicitly uses this filename; preserve each crop |
| Split desktop hero and Mobile A portrait | [04-family-a-rabbit-portrait.png](../../assets/imagery/brand/04-family-a-rabbit-portrait.png), named in the Figma layers |
| Product gallery | [07-final-stone-detail-landscape.png](../../assets/imagery/products/night/07-final-stone-detail-landscape.png), named in the Figma layers |
| CTA product artwork | [schlafsteine.png](../../assets/imagery/products/night/schlafsteine.png), named in the Figma layer |
| Expanded Steps image | [04-shared-story-landscape.png](../../assets/imagery/products/night/04-shared-story-landscape.png), named in the Figma layer |
| Navigation logo | [1:1 color Small SVG](<../../assets/logo/Format=1_1, Color=color, Size=Small.svg>) |
| Brand hero horizontal white logo | [default Screen Small SVG](<../../assets/logo/Format=default, Color=screen, Size=Small.svg>) |
| Other logo placements | [Logo assets](../../assets/logo/); match format, color, and size to the instance |
| FAQ/navigation direction | [Ink chevrons](../../assets/icons/ink/chevrons.svg) · [Screen chevrons](../../assets/icons/screen/chevrons.svg) |
| Product feature pills | [Ink asterisk](../../assets/icons/ink/asterisk.svg) |
| Steps | [Screen alarm-clock](../../assets/icons/screen/alarm-clock.svg) |
| Ratings / attribution | [Screen star](../../assets/icons/screen/star.svg) · [Screen person](../../assets/icons/screen/person.svg) |
| Other button icons | [Existing SVG icon families](../../assets/icons/), matched to the actual selected instance |
| Optional illustration layers | [Brand overlays](../../assets/illustrations/brand/) · [Night overlays](../../assets/illustrations/product/night/), with their corresponding mockups |

Image-fill matches without explicit layer filenames are visual matches, not verified byte-identical Figma exports. Do not replace a source crop with an unrelated image. Illustration overlays are available assets but are not added to the inspected website patterns by this specification. If a later design uses one, pair it with its documented source photograph and preserve the overlay’s coordinate frame. Do not apply it to a different crop without checking alignment.

Logo format colons are represented by underscores in local filenames. The folder includes duplicate-suffixed 1_2 Screen exports; those filenames do not prove which is a color variant. Exact selection for an unused 1:2 color instance is **to be defined**. Social marks visible in the footer have no identified matching files in the supplied icon families.

### Component tokens

These recipes encode observed combinations using the foundations above. They are intentionally partial: complex image crops, layout trees, gradient transforms, and state-specific sizing remain in the prose and linked Figma nodes. No unspecified interaction is encoded as an established standard.

```yaml
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.screen}"
    rounded: "{rounded.4}"
  button-screen:
    backgroundColor: "{colors.screen}"
    textColor: "{colors.ink}"
    rounded: "{rounded.4}"
  button-ink:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.screen}"
    rounded: "{rounded.4}"
  button-secondary-screen:
    backgroundColor: transparent
    textColor: "{colors.screen}"
    rounded: "{rounded.4}"
  button-secondary-ink:
    backgroundColor: transparent
    textColor: "{colors.ink}"
    rounded: "{rounded.4}"
  button-large:
    typography: "{typography.body-tall}"
  button-default:
    typography: "{typography.body}"
  button-small:
    typography: "{typography.body-small}"
  hero-neutral:
    backgroundColor: "{colors.screen}"
    textColor: "{colors.ink}"
  hero-morning:
    backgroundColor: "{colors.morning}"
    textColor: "{colors.screen}"
  hero-day:
    backgroundColor: "{colors.day}"
    textColor: "{colors.screen}"
  hero-night:
    backgroundColor: "{colors.night}"
    textColor: "{colors.screen}"
  product-feature-pill:
    backgroundColor: "{colors.night-sand}"
    textColor: "{colors.ink}"
    rounded: "{rounded.full}"
    typography: "{typography.body}"
  dropdown:
    backgroundColor: "{colors.screen}"
    rounded: "{rounded.16}"
  cta-band:
    backgroundColor: "{colors.night-sand}"
    textColor: "{colors.screen}"
  testimonial-day:
    backgroundColor: "{colors.day}"
    textColor: "{colors.screen}"
    rounded: "{rounded.16}"
    typography: "{typography.body}"
  testimonial-morning:
    backgroundColor: "{colors.morning}"
    textColor: "{colors.screen}"
    rounded: "{rounded.16}"
    typography: "{typography.body}"
  testimonial-night:
    backgroundColor: "{colors.night}"
    textColor: "{colors.screen}"
    rounded: "{rounded.16}"
    typography: "{typography.body}"
  footer:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.screen}"
```

### Combining the patterns

Reuse the combinations designed inside each component: photo + title + action(s) + logo in Brand Hero; gallery + feature pills + product information + purchase action in Product; question/answer items + dividers in FAQ; compact/expanded panels in Steps; rating + quote + attribution in Testimonial; and logo + brand paragraph + navigation + portrait in Footer.

The Web page presents separate reusable component sets. Their canvas order is not an approved website sitemap or page sequence. Final page inventory, section order, navigation destinations, and rules for combining sections into complete pages are **to be defined**. Do not treat repeated sample actions as separate confirmed user journeys.

## Do's and Don'ts

- **Do** preserve the supplied Figma design choices, including the exact color combinations, mobile alternatives, component-specific spacing, icon visibility, and intentional hover-size change.
- **Do** reuse canonical palette tokens and supplied assets; map legacy Figma names by value.
- **Do** use Selba for display titles and Figtree for the documented text and control roles.
- **Do** retain mobile A and B and run the required A/B test once its specification is defined.
- **Do** keep children active in the story and preserve the photograph’s meaningful gestures and product details when matching crops.
- **Do** follow the brand’s factual boundaries: use verified product information and traceable real testimonials.
- **Don’t** import the generic template’s fonts, palette, components, or example rules into selba.
- **Don’t** infer missing breakpoints, mobile sections, form patterns, animation timing, navigation behavior, or routes from a static frame.
- **Don’t** invent inputs, checkboxes, radio buttons, chips, tooltips, or validation states merely because the generic format mentions them. These are not supplied website components.
- **Don’t** turn sample copy, prices, star counts, or persona stories into claims of verified product or customer facts.
- **Don’t** add illustrations to existing compositions simply because overlays are available.