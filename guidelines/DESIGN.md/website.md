---
version: alpha
name: selba website
description: Website foundations, components, patterns, and combinations documented from the selba Figma library.
---

# selba website design system

## Overview

selba makes room for “I can do it myself.” The website combines expressive Selba display titles, clear Figtree text, family photography, playful drawn icons, and generous spacing. It addresses parents and caregivers in German-speaking DACH while keeping children’s participation at the center. Apply the intent, evidence boundaries, and naming rules in [BRAND.md](../../BRAND.md).

**Documented:** 3 November 2026. **Owner:** Max Pinkert. **Scope:** the current [Atoms page](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=0-1) and [Web page](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=1-2), including the four-step Shop set and the separate four-state Steps set. Measurements, style names, and the limited prototype wiring noted below come from a fresh read-only inspection of the live file.

### How to use this document

- Figma defines the visual designs. Preserve its observed combinations, colors, sizing, and state differences rather than silently redesigning them. An observed difference is not proof of intent; unresolved source inconsistencies are recorded below.
- [digital.md](../../assets/colors/digital.md) owns palette names and exact values. Map differing Figma names by value, as described below, without changing the appearance or silently renaming either source.
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

### Source naming and value conflicts

Use actual variable values and applied fills to identify the designed appearance; several visible Atoms swatch labels disagree with them.

| Figma source | Actual value / website mapping | Unresolved discrepancy |
| --- | --- | --- |
| `morning` | `#499ACD` → `morning` | Swatch `1:13` prints `#F5D91B` |
| `morning-sun` | `#F5D91B` → digital.md `morning-yellow` | Swatch `1:52` is named `morning-blue` and prints `#499ACD`; its visible name is `morning-sun` |
| `day` | `#FF7852` → `day` | Swatch `1:18` prints `#00CC99` |
| `day-torquoise` | `#00CC99` → digital.md table `day-torquoise` | Swatch `1:49` displays `day-torqouise` and `#FF7852`; digital.md YAML also spells the key `day-torqouise` |

These are naming/label conflicts, not permission to exchange the colors. Other palette values agree with digital.md. Figma additionally supplies `Transparent/screen`, `Transparent/ink`, and `Transparent/Primary` at 20% opacity. `Transparent/Day` is the turquoise `#00CC99` at 90%, `Transparent/Morning` is the yellow `#F5D91B` at 90%, and `Transparent/Night` is `#0B1946` at 90%; those names do not imply that the current main Day or Morning colors should replace their underlying values. Preserve the source treatment where used rather than inventing new palette aliases.

### Designed combinations

| Pattern | Surface | Text / foreground |
| --- | --- | --- |
| Neutral hero, Shop, FAQ | `screen` | `ink` |
| Morning hero | `morning` | `screen` |
| Day hero | `day` | `screen` |
| Night hero | `night` | `screen` |
| Brand hero | Photography and the source gradient treatment | `screen` title and logo |
| CTA band | `night-sand` | `screen` heading/body; white filled button with `ink` label |
| Steps | `night-sand`, `night-sage`, `night-lavender`, `night` panels | `screen` |
| Testimonial cards | `day`, `morning`, `night` | `screen` |
| Shop benefit pills | `night-sand` | `ink` |
| Shop confirmation panels | `night-sage` | `ink` |
| Footer | `ink` | `screen` |

These are the combinations in the supplied Figma designs, not a declaration that every combination passes accessibility requirements. Palette groups do not imply automatic light/dark themes or global status colors; the green Shop panels are a local confirmation treatment. The three-color testimonial row is a specific website combination; it does not change the separate palette restrictions for illustration overlays. See unresolved accessibility conflicts below.

## Typography

**Selba Bold** carries expressive display titles. **Figtree** carries the Heading 1–6 styles, body copy, navigation, button labels, captions, and supporting information. This division is the owner-confirmed brand direction. Figtree also remains the fallback when Selba is unavailable.

Use the supplied [Selba Bold WOFF2](../../assets/fonts/Selba/Selba-Bold.woff2) and [Figtree Latin variable WOFF2](../../assets/fonts/Figtree/figtree-latin-wght-normal.woff2), [Latin extended](../../assets/fonts/Figtree/figtree-latin-ext-wght-normal.woff2) and [italic](../../assets/fonts/Figtree/figtree-latin-wght-italic.woff2) files are also available. Their availability does not add italic roles to the current website style inventory.

### Observed type scale

Source: [Typography](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=7-150) and the live local text-style inventory. The table omits the shared `Typography/` prefix but preserves style names. All listed styles have zero percent letter spacing. Line heights below convert Figma percentages to unitless multipliers.

| Figma style | Document token | Family / weight | Size | Line height |
| --- | --- | --- | --- | --- |
| Title | `title` | Selba / 700 | 96px | 1.1 |
| Title (S) | `title-s` | Selba / 700 | 64px | 1.1 |
| Title (XS) | `title-xs` | Selba / 700 | 40px | 1.1 |
| H1 | `heading-1` | Figtree / 400 | 96px | 1.2 |
| H2 | `heading-2` | Figtree / 400 | 64px | 1.2 |
| H3 | `heading-3` | Figtree / 400 | 40px | 1.2 |
| H4 | `heading-4` | Figtree / 400 | 32px | 1.2 |
| H5 | `heading-5` | Figtree / 400 | 24px | 1.2 |
| H6 | `heading-6` | Figtree / 400 | 20px | 1.2 |
| Body-Tall | `body-tall` | Figtree / 400 | 20px | 1.4 |
| Body-Bold | `body-bold` | Figtree Black / 900 | 16px | 1.2 |
| Body | `body` | Figtree / 400 | 16px | 1.4 |
| Body-Small | `body-small` | Figtree / 400 | 12px | 1.4 |
| Body - Small - Bold | `body-small-bold` | Figtree Black / 900 | 12px | 1.2 |
| Captions | `captions` | Figtree / 400 | 8px | 1.4 |

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
    lineHeight: 1.4
    letterSpacing: 0em
  body-small-bold:
    fontFamily: Figtree
    fontSize: 12px
    fontWeight: 900
    lineHeight: 1.2
    letterSpacing: 0em
  captions:
    fontFamily: Figtree
    fontSize: 8px
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 0em
```

Desktop heroes use `title`; the mobile Brand hero and A patterns use `title-s`; mobile B patterns, the Shop product name, and CTA title use `title-xs`. Buttons use `body-tall`, `body`, and `body-small` for Large, Default, and Small respectively. The regular 12px `body-small` style now uses 1.4 line height, including Small buttons, default navigation labels, Shop field labels, testimonial attribution, and the footer paragraph. Navigation hover uses the distinct 12px/900 `body-small-bold` treatment at 1.2 line height. Shop field values and purchase/waitlist/community actions use `body-tall`. The 8px `captions` style uses 1.4 line height (11.2px), including navigation descriptions, Shop consent, and footer headings, newsletter copy, and legal links; consent privacy links are underlined. FAQ questions use `heading-6` and answers use `body`. Match these roles rather than treating every visually prominent heading as Selba. The styles named “Bold” actually use Figtree Black at weight 900; do not silently substitute 700.

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

Shop, FAQ, Video, and Steps desktop sections have 96px outer padding. Testimonials use 96px horizontally and 64px vertically. The footer uses 96px horizontally and 40px vertically. Navigation uses 24px padding. These are distinct patterns, not a single universal section-padding rule.

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

- **4px:** action buttons, Shop field presentations, main product-gallery image, and the image window inside the expanded Steps panel.
- **8px:** Shop gallery thumbnails and confirmation panels in Community and Success.
- **16px:** mobile A image window, dropdown container and image window, Steps panels, testimonial cards, and the footer portrait window.
- **Full:** feature pills beneath the product gallery.
- **Square:** full-width section surfaces and navigation-link containers retain their observed zero radius. Zero is an observed property, not an additional Figma radius variable.

Logo and icon outlines come from supplied SVG artwork. Preserve their proportions and hand-drawn character; do not replace them with text approximations or another icon family.

## Components

### Component inventory

| Figma library | Source | Available variants / artwork |
| --- | --- | --- |
| Button | [16:2891](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=16-2891) | 32 variants: filled, outlined, and navigation patterns |
| Hero | [28:3928](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=28-3928) | 14 variants: 5 Web, 1 Mobile Brand, 4 Mobile A, 4 Mobile B |
| Navbar | [44:9823](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=44-9823) | Default and Dropdown |
| FAQ | [49:9915](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-9915) | Question-only and question-with-answer appearances |
| Sections | [49:10114](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10114) | 5 variants: FAQ, Video, CTA, Testimonial, Footer |
| Shop | [68:926](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=68-926) | `Step=Product`, `Waitlist`, `Community`, `Success`; Product is the default |
| Steps | [72:1422](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=72-1422) | `Step=1`, `2`, `3`, `4`; Step 1 is the default |
| Logo | [2:84](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=2-84) | default / 1:1 / 1:2 × ink / screen / color × Large / Default / Small |
| Icons | [36:8227](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=36-8227) | Section containing 195 individual components: 65 each in screen, ink, and primary, including checked and unchecked boxes |

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
| Small | 12px / 1.4 | 12 / 16px | 11 / 16px | 8px | 12px |

With both icons visible, filled specimens measure 64, 48, and 36px high; outlined specimens measure 56, 48, and 36px. The **Large Primary-color hover** specimen (`16:2873`) uses 16px icons and measures **56px** high versus **64px** and 24px icons in Default (`16:2875`). Large Screen and Ink filled hover specimens remain 64px high; Large outlined variants remain 56px. Preserve these measured differences in source documentation, but treat their intended runtime behavior as an unresolved design inconsistency, not an approved hover-resize rule.

Height depends on the visible children in the source: text-only instances are smaller, including the 32px-high Small navigation CTA, 43px-high Default split-hero buttons, and 54px-high Large Shop actions. The desktop Brand action group is also 54px high. Do not impose one fixed height across all instances or use text-layer ink bounds as CSS line-height values.

Navigation is a separate text-and-description pattern with a 12px / 1.4 label, directional icon, optional 8px / 1.4 subtext, and 8px internal gap. Its outer padding is 12px vertically and 16px horizontally. Hover changes the label to weight 900 at 1.2 line height and changes its measured width; retain this distinction from the regular label. The `Color=Screen` variant name does not mean all nested text is white: the standalone sample uses `ink`; footer instances supply the light treatment shown in the composition.

Pressed, focus, disabled, loading, and icon-only interaction specifications are **to be defined**. The presence of a Hover variant does not establish its animation timing.

### Hero patterns and combinations

All hero recipes reuse the Button and typography foundations. The Brand hero combines full-bleed family photography, a centered Selba title, two actions, and the horizontal white logo near the bottom. Its desktop title group is 738px wide, with 64px between title and actions. The mobile Brand composition has a 327px-wide content group, 64px top padding, and a 125 × 40px logo.

The Web Neutral/Morning/Day/Night pattern is a text-and-image split: a 439px-wide text column at x=96, and a 535px-wide portrait image at x=745 extending to the right edge. The source portrait is 803px high and cropped by the 720px hero. The text column uses 96px top/bottom padding and `SPACE_BETWEEN` distribution between title and content; configured item spacing is 144px for Neutral and 64px for the range-colored variants, not a fixed rendered title-to-content gap. The body-to-actions gap is 40px. Neutral shows a filled primary action plus an outlined Ink action; the range-colored desktop variants show one filled primary action.

| Type | Web | Mobile A | Mobile B | Surface token |
| --- | --- | --- | --- | --- |
| Brand | `28:3927` | Mobile Default `28:3922`; no A/B pair | — | Photograph |
| Neutral | `28:3926` | `28:3916` | `28:3919` | `screen` |
| Morning | `28:3924` | `28:3915` | `28:3920` | `morning` |
| Day | `28:3923` | `28:3914` | `28:3918` | `day` |
| Night | `28:3925` | `28:3921` | `28:3917` | `night` |

Each ID resolves in the [Hero set](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=28-3928). Preserve the differences between these compositions:

- **Mobile A:** 24px side inset; a 327 × 327px image window with 16px radius; a 64px Selba title; body copy and a Small primary action beneath. Morning/Day/Night use 24px configured spacing and 40px bottom padding; Neutral has its own 66px configured spacing and 24px bottom padding. Preserve the source distribution rather than forcing identical vertical positions across variants.
- **Mobile B:** full-width photographic background with a small action at the lower-right edge of the image area; a full-width colored text panel begins at y=525 in the 800px specimen. The panel is 275px high, with 40px vertical and 24px horizontal padding, a 40px Selba title, and body text. The action sits above the panel, not below the description.

**A/B test requirement:** retain both A and B for Neutral, Morning, Day, and Night. Run an A/B test before choosing a winning mobile pattern. No winner is established. Test objective, primary metric, eligible traffic, allocation, tracking, duration/sample requirements, and decision rule are **to be defined**. The supplied variants differ in imagery treatment, title size, and action placement; document the tested combination so results are not attributed to a single isolated change.

### Navigation

Default (`44:9822`) is 1280 × 88px on `screen`, with 24px padding, a 32 × 32px color 1:1 logo at left, and “Produkte”, “Über uns”, and a Small Primary action at right. Navigation spacing is 24px between the link group and CTA.

Dropdown (`44:9821`) combines the same top bar with a 24px gap and a 1280 × 280px white panel with 16px radius. The panel has 96px horizontal and 40px vertical padding. It combines three range destinations, short descriptions, and a 200px square rounded image. The groups are labeled “morgens”, “tagsüber”, and “abends”, using the Morning blue, Day coral, and Night colors respectively. Their current link labels are “Zur Warteliste”, “Zur Warteliste”, and “Schlafsteine”; descriptions remain placeholder copy. The open composition uses the Hover treatment for the top-level “Produkte” link.

Opening/closing triggers, keyboard behavior, sticky positioning, overlay behavior, destinations, and mobile navigation are **to be defined**. The displayed labels establish the pattern, not published routes or product availability.

### Shop: Product, Waitlist, Community, Success

Source: [Shop, 68:926](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=68-926). Product is now part of this set, not a `Type=Product` variant of Sections. The property axis is `Step`; all four desktop specimens are **1280 × 814px**, on `screen`, with **96px padding**, **two 439px columns**, and a **210px column gap**. Their inner columns are 622px high. No Mobile Shop variant is supplied.

#### Shared gallery and benefits

All four steps retain the same left column: a gallery and three benefit pills, separated by 40px. The main image is 439 × 300px with 4px radius. Five 69 × 47px thumbnails with 8px radii form a left-aligned 377 × 47px row, with an 8px main-image-to-thumbnail gap and 8px gaps between thumbnails. In Product, Waitlist, Community, and Success alike, the first thumbnail's image fill is at 25% opacity and the other four are at 100%; all five layers remain at 100% node opacity and have no stroke. Preserve this visible distinction without treating it as a defined selected/disabled state or inferring gallery interactions. The main image and all thumbnails repeat the same photograph; do not invent a completed five-image product set. Benefit pills are 439 × 65px, `night-sand`, full radius, 16px vertical / 24px horizontal padding, 16px icon-to-text spacing, and a 24px Ink asterisk icon. Pills are separated by 16px and contain placeholder body copy.

#### Step inventory

| Step / source | Right-column composition | Visible action |
| --- | --- | --- |
| [Product, 49:9884](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-9884) | `abends` range label in Night, 40px Selba “Schlafsteine”, 16px description, 20px “39,90 €” price; purchase action near the bottom | Full-width Large Primary “Jetzt kaufen” |
| [Waitlist, 68:925](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=68-925) | Product heading with directional icon, description and price retained; 20px out-of-stock invitation, E-Mail field, separate email consent row | Full-width Large Primary “Auf Warteliste eintragen” |
| [Community, 68:924](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=68-924) | Product heading with directional icon, E-Mail confirmation presentation and green thank-you panel; invitation to the WhatsApp community, Telefonnummer field, separate phone consent row | Full-width Large Primary “Für Produkttests anmelden” |
| [Success, 68:923](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=68-923) | Product heading, Telefonnummer confirmation presentation and green community confirmation panel | Full-width Large outlined Ink “Zurück zur Website” |

The four compositions show a product/waitlist/community sequence, not a complete implemented state machine. One prototype reaction is present: clicking the **Waitlist component root** (`68:925`) changes to Community (`68:924`) with `ON_CLICK` → `CHANGE_TO` and no transition animation configured. This is not a reaction attached specifically to the submit button, and it does not establish validation, consent enforcement, or a successful real submission. No other Shop transition was found in the inspected variants and their descendants.

The Community invitation remains **optional**: email waitlist consent is not consent to WhatsApp participation or product-test contact. Do not make a phone number a prerequisite for the email waitlist. The source does not specify the optional skip control or its destination.

#### Fields, consent and confirmation treatment

- **Field presentation:** 439 × 70px label/control stack with an 8px gap; 12px / 1.4 label over a 439 × 54px control, 4px radius, 1px Ink border, 19px vertical / 24px horizontal padding, and 20px text. Waitlist shows “E-Mail” / “...”; Community shows “Telefonnummer” / “+49 ...”. These are sample values, not a phone-format validation specification.
- **Source implementation boundary:** the visible field shells are reused Large Secondary Ink **Button instances**, not a dedicated Input component set. Entry presentations have no fill. The Community email and Success phone presentations reuse `State=Hover`, giving them a 20%-opacity Ink fill. This records their appearance only; it does not establish disabled, read-only, valid, or focused field semantics.
- **Consent rows:** 439 × 28px, with a 24px `ink/box-unchecked` icon, 16px gap, and 399px-wide 8px / 1.4 copy. The email row describes storing/using the address for restock notification; the phone row separately describes storing/using the number for product-test contact. Both mention withdrawal and the underlined Datenschutzerklärung. The form stack uses 16px gaps between the labeled field, consent row, and action. Both box drawings exist in the icon library and local exports, but only the unchecked presentation is composed in Shop; a checked form-control state, focus behavior, and consent submission rules are not established by the artwork alone.
- **Confirmation panels:** Community (`68:804`) and Success (`68:845`) use `night-sage` with Ink content, 439 × 143px, 8px radius, 24px padding, and 16px between the 24px icon and 16px text. Community uses `ink/rocket` with a restock thank-you message. Success uses `ink/heart-fun` and a message about later community contact. This does not establish a global success-color token.
- **Actions:** the shown Shop actions are 439 × 54px, text-only, with 20px labels. Primary actions use 20px vertical / 40px horizontal padding; the outlined return action uses 19px vertical / 40px horizontal padding.

Visible copy includes an out-of-stock statement, a promise of restock notification, and future community contact. These are design examples, not evidence of current inventory, a working integration, approved legal consent, delivery timing, or verified product facts. Price, benefits, consent wording and destinations require current product/legal approval before publication; preserve the distinction from visual fidelity.

**To be defined:** gallery selection and active thumbnails; purchase/stock routing and the remaining step transitions beyond the observed Waitlist-root prototype click; back/return/optional-skip destinations; editable versus read-only field behavior; required fields and consent enforcement; focus, checked-control, error, validation, loading, and submission-failure states; keyboard/screen-reader behavior; email/phone processing and WhatsApp integration; and responsive/mobile Shop composition. Do not treat prototype navigation as a working form or fabricate a mobile Shop design.

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

Source: the standalone [Steps set, 72:1422](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=72-1422), no longer a `Type=Steps` variant of Sections. The property axis is `Step`, with **four supplied expanded appearances** and **Step 1 as the default**:

| Variant | Source | Expanded panel |
| --- | --- | --- |
| `Step=1` | [49:10301](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10301) | First — `night-sand` |
| `Step=2` | [72:1421](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=72-1421) | Second — `night-sage` |
| `Step=3` | [72:1420](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=72-1420) | Third — `night-lavender` |
| `Step=4` | [72:1419](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=72-1419) | Fourth — `night` |

Every reference variant is **1279 × 745px**, with 96px padding and 24px gaps. Each has four 553px-high, 16px-radius panels: one 532px expanded panel and three 161px compact panels. Their widths, gaps, and padding account for the 1279px specimen; do not silently normalize it to the 1280px section references or derive a new breakpoint from the difference. The panel order stays sand, sage, lavender, night across all four variants.

Compact panels have 40px vertical / 60px horizontal padding, a 32px Screen alarm-clock icon, and a 90°-rotated 32px Figtree heading. They use `SPACE_BETWEEN` distribution; the configured 200px item spacing is not a fixed rendered gap. Expanded panels have 40px padding and Screen content: a 32px icon with a 16px label, a 32px Figtree heading, 16px body copy, and a 130 × 36px Small outlined Screen “Mehr erfahren” action. The content stack uses 40px gaps, with 24px between heading and body; 64px separates that stack from the 452 × 144px, 4px-radius image window. The 467 × 311px source photograph extends beyond the clipped window.

All four expanded appearances currently reuse the same placeholder text, icon, action, and photograph; the variants establish which colored panel is expanded, not four approved content stories. No prototype reactions are assigned to the Steps variants or their descendants. Switching triggers, keyboard behavior, animation, action destinations, final copy, and mobile arrangement remain **to be defined**. The four designed states are available; an interactive accordion is not yet specified.

### Testimonials

[Type=Testimonial, 49:10302](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10302) combines three 347 × 175px cards with 24px gaps in a 1280 × 303px white section. Each card has a 16px radius, 24px vertical / 40px horizontal padding, and 16px spacing between rating, quote, and attribution. Card colors are Day coral, Morning blue, and Night, with white content.

Use the supplied outlined star and person artwork. Preserve the source’s differing star counts; they are sample rating layouts, not evidence of customer ratings. Quotes and “Mama einer Tochter” attribution are placeholder examples. Real quotes, attribution, rating provenance, and mobile layout are **to be defined**. Do not populate this pattern with persona simulations or invented testimonials.

### Footer

[Type=Footer, 49:10755](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10755) is now **1280 × 421.7px** (approximately 422px high) on Ink, with 96px horizontal / 40px vertical padding. Its horizontal auto-layout distributes two bottom-aligned main groups: 254px and 625px wide, both 341.7px high. It combines:

- A left column with an additional 40px top inset: a Small white horizontal logo measuring approximately 108.44 × 34.7px, followed after 24px by a 254px-wide 12px / 1.4 brand paragraph. The newsletter group follows the brand-information group after 40px.
- A 254 × 93px newsletter presentation with 8px vertical gaps: the 8px / 1.4 heading “zum newsletter anmelden”; a 200 × 32px “Deine E-Mail” field shell and 46 × 32px icon-only action separated by 8px; then a 16px white unchecked-box drawing, 16px gap, and 222px-wide 8px / 1.4 consent text. The field and action reuse Small Secondary Screen Button instances with 1px white outlines and 4px radii; the field label is 12px / 1.4 and the action contains a 12px chevron icon. These are visual presentations, not evidence of editable input or working newsletter submission.
- Product and resource columns, each 161px wide, using 8px / 1.4 headings (“Produkte”, “Ressourcen”), 12px / 1.4 Navigation labels, 8px / 1.4 descriptions, and 16px directional icons. Product labels are “Schlafsteine”, “Zur Warteliste”, and “Zur Warteliste”; resource labels are “Über uns”, “Blog”, and “Hilfe”. Descriptions remain placeholder copy. The footer instances remove the standard Navigation left padding; the last item in each column also removes bottom padding.
- Three approximately 24px social marks with 16px gaps, right-aligned above the 625 × 301.7px navigation/portrait row with 16px separation. That row has 24px gaps between the two link columns and a 255px-wide portrait/legal column. The portrait window is 255 × 271.7px with 16px radius, clipping the supplied drawing-family image. Legal links now sit 24px below the image, distributed with `SPACE_BETWEEN` across the full 255px width, rather than below the brand paragraph.

The current paragraph reads: “Manchmal braucht ein eigener Versuch etwas Zeit und jemanden, der den Reißverschluss festhält. Mit selba möchten wir solchen Versuchen mehr Platz im Familienalltag geben. Dafür entwickeln wir einfache, spielerische Werkzeuge, die zum Mitmachen einladen und Raum für euren eigenen Weg lassen.” Preserve its supplied hierarchy and regular Body-Small treatment.

The newsletter consent reads: “Ich bin damit einverstanden, dass selba meine E-Mail-Adresse speichert und nutzt, um miR den Newsletter zu schicken. Weitere Informationen finde ich in der Datenschutzerklärung.” The privacy reference is underlined; the source capitalization “miR” is retained here as an editorial issue, not silently corrected or treated as approved legal copy.

The source legal labels remain Impressum, Datenschutz, AGBs, and Sicherheit, all 8px / 1.4. Legal and newsletter consent copy, link descriptions, routes, social profile destinations, exported social-mark assets, newsletter processing and submission states, and mobile composition are **to be defined**. Repeated waitlist labels do not establish distinct destinations or product availability. The icon-only newsletter action does not resolve its accessible name, focus, validation, checked-consent, success, or error behavior.

### Reuse and asset mapping

Paths below are relative to this document. Match the source frame’s crop and logo variant; filenames alone do not authorize a different composition.

| Designed use | Existing asset |
| --- | --- |
| Brand desktop hero / full-width media scene | [01-family-a-building-landscape.png](../../assets/imagery/brand/01-family-a-building-landscape.png), visually matched to the family/building scene |
| Mobile Brand/B, dropdown, footer portrait scene | [02-family-a-drawing-portrait.png](../../assets/imagery/brand/02-family-a-drawing-portrait.png); footer layer explicitly uses this filename; preserve each crop |
| Split desktop hero and Mobile A portrait | [04-family-a-rabbit-portrait.png](../../assets/imagery/brand/04-family-a-rabbit-portrait.png), named in the Figma layers |
| Product gallery and thumbnails, all four Shop steps | [07-final-stone-detail-landscape.png](../../assets/imagery/products/night/07-final-stone-detail-landscape.png), named in the Figma layers and repeated in every main image and thumbnail; preserve the thumbnail crops, 8px radii, and first-thumbnail 25% image-fill opacity |
| CTA product artwork | [schlafsteine.png](../../assets/imagery/products/night/schlafsteine.png), named in the Figma layer |
| Expanded Steps image | [04-shared-story-landscape.png](../../assets/imagery/products/night/04-shared-story-landscape.png), named in the Figma layer |
| Navigation logo | [1:1 color SVG](<../../assets/logo/svg/Format=1_1, Color=color, Size=Large.svg>); scale the supplied vector to the 32 × 32px Small instance |
| Brand hero horizontal white logo | [default Screen SVG](<../../assets/logo/svg/Format=default, Color=screen, Size=Large.svg>); scale the supplied vector to the 125 × 40px Small instance |
| Other logo placements | [Logo assets](../../assets/logo/); match format, color, and size to the instance |
| FAQ/navigation direction | [Ink chevrons](../../assets/icons/ink/chevrons.svg) · [Screen chevrons](../../assets/icons/screen/chevrons.svg) |
| Product feature pills | [Ink asterisk](../../assets/icons/ink/asterisk.svg) |
| Shop confirmation panels | [Ink rocket](../../assets/icons/ink/rocket.svg) · [Ink heart-fun](../../assets/icons/ink/heart-fun.svg) |
| Shop consent artwork | [Ink unchecked box](../../assets/icons/Icons/ink/box-unchecked.svg); [checked box artwork](../../assets/icons/Icons/ink/box-checked.svg) is also available, but not composed as a checked Shop state |
| Shop directional icon | [Ink arrow-right](../../assets/icons/ink/arrow-right.svg); preserve the source orientation |
| Steps | [Screen alarm-clock](../../assets/icons/screen/alarm-clock.svg) |
| Ratings / attribution | [Screen star](../../assets/icons/screen/star.svg) · [Screen person](../../assets/icons/screen/person.svg) |
| Other button icons | [Existing SVG icon families](../../assets/icons/), matched to the actual selected instance |
| Optional illustration layers | [Brand overlays](../../assets/illustrations/brand/) · [Night overlays](../../assets/illustrations/product/night/), with their corresponding mockups |

Image-fill matches without explicit layer filenames are visual matches, not verified byte-identical Figma exports. Do not replace a source crop with an unrelated image. Illustration overlays are available assets but are not added to the inspected website patterns by this specification. If a later design uses one, pair it with its documented source photograph and preserve the overlay’s coordinate frame. Do not apply it to a different crop without checking alignment.

Logo format colons are represented by underscores in local filenames. Current exports are grouped under `assets/logo/svg/` and `assets/logo/png/`, with Large files for each format/color combination; use the vector artwork at the documented instance size rather than linking nonexistent Small exports. The Shop box artwork is available in the nested `assets/icons/Icons/` export folder, including Ink, Screen, and Primary checked/unchecked versions. The Ink SVGs have a 40 × 40 viewBox; scale the supplied unchecked artwork to the 24px consent-row instance instead of substituting another checkbox icon. Availability of a checked drawing does not define the complete checked-control interaction. Social marks visible in the footer still have no identified matching files in the supplied icon families.

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
  shop-confirmation-panel:
    backgroundColor: "{colors.night-sage}"
    textColor: "{colors.ink}"
    rounded: "{rounded.8}"
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

Reuse the combinations designed inside each component: photo + title + action(s) + logo in Brand Hero; shared gallery + benefit pills + step-specific product/form/confirmation content in Shop; question/answer items + dividers in FAQ; the four compact/expanded panel arrangements in the standalone Steps set; rating + quote + attribution in Testimonial; and logo + brand paragraph + newsletter presentation + navigation + portrait/legal links in Footer.

The Web page presents separate reusable component sets. Their canvas order is not an approved website sitemap or page sequence. Final page inventory, section order, navigation destinations, and rules for combining sections into complete pages are **to be defined**. Do not treat repeated sample actions as separate confirmed user journeys.

## Unresolved source and publication conflicts

- **Color names and swatch labels:** the specific Figma/digital.md discrepancies are recorded in Colors. Applied fills and variable values establish the reference appearance; the conflicting labels and token spelling still require reconciliation in their owning sources.
- **Large button sizing:** Primary-red Default is 64px high but Hover is 56px; Large Secondary is 56px in both states. Other Large filled colors remain 64px. Do not call this intentional or normalize it without a design decision.
- **“Bold” typography naming:** `Typography/Body-Bold` and `Typography/Body - Small - Bold` use Figtree Black/900, not 700. Whether to rename those styles or change their weight remains an owner decision; this document retains the actual 900 values.
- **Shop control semantics:** field-looking nodes still reuse Button variants, including Hover for confirmation presentations. Checked/unchecked box artwork is available, but real input/confirmation states, a composed checked-control state, optional-community exit, validation, submission and consent behavior remain unspecified. The Waitlist-root click-to-Community prototype reaction does not resolve those requirements.
- **Accessibility versus visual fidelity:** the source's white text on `morning`, `day`, `night-sand`, `night-sage`, `night-lavender`, and `primary` includes normal-text combinations below the WCAG AA 4.5:1 threshold. Some also fall below the 3:1 large-text threshold. Preserving the reference does not establish accessible production use. Resolve contrast, the 8px consent/legal copy, focus treatment and interaction accessibility with the design owner rather than silently recoloring or claiming conformance.
- **Publication evidence:** placeholder benefits/descriptions, price, out-of-stock and contact promises, consent/legal copy, sample testimonials, routes and integrations remain unverified. Mobile Shop and other missing responsive sections remain undefined; the existing mobile Hero A/B testing requirement is unchanged.

## Do's and Don'ts

- **Do** preserve the supplied Figma combinations, mobile alternatives, component-specific spacing and icon visibility; record unresolved differences instead of assuming intent.
- **Do** reuse canonical palette tokens and supplied assets; map differing Figma names by actual value.
- **Do** use Selba for display titles and Figtree for the documented text and control roles.
- **Do** retain mobile A and B and run the required A/B test once its specification is defined.
- **Do** keep children active in the story and preserve the photograph’s meaningful gestures and product details when matching crops.
- **Do** follow the brand’s factual boundaries: use verified product information and traceable real testimonials.
- **Don’t** import the generic template’s fonts, palette, components, or example rules into selba.
- **Don’t** infer missing breakpoints, mobile sections, additional form states, animation timing, navigation behavior, or routes from a static frame.
- **Don’t** treat Shop's supplied email/phone fields and consent rows as a complete form-control library, or invent radio buttons, tooltips, validation states, or additional controls merely because a generic format mentions them.
- **Don’t** turn sample copy, prices, star counts, or persona stories into claims of verified product or customer facts.
- **Don’t** add illustrations to existing compositions simply because overlays are available.