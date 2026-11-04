---
version: alpha
name: selba website
description: Website foundations, components, patterns, and combinations documented from the selba Figma library.
---

# selba website design system

## Overview

selba makes room for “I can do it myself.” The website combines expressive Selba display titles, clear Figtree text, family photography, playful drawn icons, and generous spacing. It addresses parents and caregivers in German-speaking DACH while keeping children’s participation at the center. Apply the intent, evidence boundaries, and naming rules in [BRAND.md](../../BRAND.md).

**Documented:** 4 November 2026. **Owner:** Max Pinkert. **Scope:** the current [Atoms page](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=0-1) foundations and [Web page](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=1-2) component inventory, including all supplied mobile variants. Measurements, text styles, visibility, and the limited prototype wiring below come from read-only inspection of the live file.

**Latest sync:** fresh read-only inspection of all Hero, Button, Sections, and Steps variants, plus their Navbar, Shop, and FAQ consumers. Updated centered Hero layouts, 8px Button hover strokes and icon defaults, differentiated testimonial cards, mobile Footer alignment, and redesigned Steps panels. Exact live `Device=Desktop` / `Device=Mobile` axes and the local typography scale remain unchanged. Static reference compositions do not establish breakpoints or runtime behavior.

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
| Testimonial cards | Opaque `morning` on the larger desktop card / `day` on the larger mobile card; smaller cards use `night`, `day`, or `morning` fills at 20% opacity | `screen`, still at 100% opacity |
| Shop benefit pills | `night-sand` | `ink` |
| Shop confirmation panels | `night-sage` | `ink` |
| Footer | `ink` | `screen` |

These are the combinations in the supplied Figma designs, not a declaration that every combination passes accessibility requirements. Palette groups do not imply automatic light/dark themes or global status colors; the green Shop panels are a local confirmation treatment. Testimonial fill opacity and differing card sizes are specific website treatments; they do not change the separate palette restrictions for illustration overlays or establish carousel behavior. See unresolved accessibility conflicts below.

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

Desktop heroes use `title`; the mobile Brand hero uses `title-s`; the other mobile heroes, Shop product names, and CTA titles use `title-xs`. Buttons use `body-tall`, `body`, and `body-small` for Large, Default, and Small respectively. Regular 12px `body-small` uses 1.4 line height, including Small buttons, default navigation labels, Shop field labels, mobile Shop benefits, larger testimonial-card attribution, smaller testimonial-card quotes, and the footer paragraph. Larger testimonial quotes use `body`; smaller-card attribution uses 8px `captions`. Navigation hover uses the distinct 12px/900 `body-small-bold` treatment at 1.2 line height; the mobile dropdown's “Produkte” heading uses 16px/900 `body-bold`. Desktop Shop field values and actions use `body-tall`; mobile field values, waitlist/community actions, and return action use `body`, while mobile Product's purchase action retains `body-tall`. The 8px `captions` style uses 1.4 line height (11.2px), including navigation descriptions, Shop consent, and footer headings, newsletter copy, and legal links; consent privacy links are underlined. Desktop FAQ questions use `heading-6`, mobile questions use `body`, and answers use `body` on both devices. Match these roles rather than treating every prominent heading as Selba. Styles named “Bold” use Figtree Black/900, not 700.

## Layout

### Reference grids

Source: [Layouts](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=7-236).

| Reference | Frame width | Columns | Outer margin | Gutter | Inner width |
| --- | --- | --- | --- | --- | --- |
| Web | 1280px | 12 stretch columns | 96px | 24px | 1088px |
| Mobile | 375px | 6 stretch columns | 24px | 12px | 327px |

Website hero specimens are 1280 × 720px on desktop and 375 × 800px on mobile. No tablet breakpoint, desktop maximum width, fluid interpolation rule, or viewport-height rule is supplied.

The supplied mobile compositions are 375px wide, usually with 24px side insets and a 327px content width. FAQ, Testimonials, Shop, and Steps use 64px top/bottom padding; Footer uses 40px. CTA, Navbar, Hero, and Video have their own arrangements below. These are reference measurements, not a rule that every section has the same height or padding. Mobile variants reorganize content, controls, and crops rather than simply scaling desktop frames.

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

The inspected website patterns use flat surfaces, whitespace, image crops, outlines, and color blocks. No shadow scale is established. Preserve the existing 1px secondary-button borders, 1px FAQ dividers, and **8px outside hover strokes** on filled buttons. Navbar dropdowns retain a distinct 4px inside Ink outline at 20% opacity; do not apply the Button hover width to those panels.

Brand hero nodes contain a photograph and an `ink` radial gradient at 50% paint opacity, with stops from opaque `ink` to 20%-opacity `ink`. The current non-Brand mobile heroes contain a photograph and a linear gradient with the reverse stop order, also at 50% paint opacity. Preserve each source node’s paint order, gradient transform, crop, and resulting appearance; do not substitute a generic CSS overlay from this abbreviated description.

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

- **4px:** action buttons, Shop field presentations and source product images, and image windows inside expanded mobile Steps panels.
- **8px:** Shop gallery thumbnails and confirmation panels, mobile Shop main-image windows, mobile Steps panels, and the portrait windows inside expanded desktop Steps panels.
- **16px:** dropdown containers and image windows, desktop Steps panels, mobile Shop benefit cards, testimonial cards, and footer portrait windows.
- **Full:** desktop feature pills beneath the product gallery.
- **Square:** full-width section surfaces and navigation-link containers retain their observed zero radius. Zero is an observed property, not an additional Figma radius variable.

Logo and icon outlines come from supplied SVG artwork. Preserve their proportions and hand-drawn character; do not replace them with text approximations or another icon family.

## Components

### Component inventory

| Figma library | Source | Available variants / artwork |
| --- | --- | --- |
| Button | [16:2891](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=16-2891) | 32 variants: filled, outlined, and navigation patterns |
| Hero | [28:3928](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=28-3928) | 10: `Device=Desktop/Mobile` × `Type=Brand/Neutral/Morning/Day/Night`; no A/B axis |
| Navbar | [44:9823](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=44-9823) | 4: Desktop `State=Default/Dropdown`; Mobile `State=State4/State3` (closed/open appearances) |
| FAQ | [49:9915](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-9915) | 4: `Device=Desktop/Mobile` × `Collapsed=OFF/ON`; OFF is question-only, ON includes answer |
| Sections | [49:10114](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10114) | 10: `Device=Desktop/Mobile` × `Type=FAQ/Video/CTA/Testimonial/Footer` |
| Shop | [68:926](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=68-926) | 8: `Device=Desktop/Mobile` × `Step=Product/Waitlist/Community/Success`; Desktop Product is default |
| Steps | [72:1422](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=72-1422) | 8: `Device=Desktop/Mobile` × `Step=1/2/3/4`; Desktop Step 1 is default |
| Logo | [2:84](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=2-84) | default / 1:1 / 1:2 × ink / screen / color × Large / Default / Small |
| Icons | [36:8227](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=36-8227) | Section containing 195 individual components: 65 each in screen, ink, and primary, including checked and unchecked boxes |

### Buttons

The property axes are `Type`, `Color`, `Size`, and `State`. The set also exposes `IconLeft`, `IconRight`, `Text`, `Subtext`, a text `Label`, and an `Icon` instance swap whose current default is `ink/arrow-right` (`36:4812`). The four visibility properties default to true and the label defaults to “Jetzt anmelden”; composed instances override these values. Use the actual available combinations, not an assumed full Cartesian product:

| Type | Colors | Sizes | States |
| --- | --- | --- | --- |
| Primary (filled) | Primary, Screen, Ink | Large, Default, Small | Default, Hover |
| Secondary (outlined) | Screen, Ink | Large, Default, Small | Default, Hover |
| Navigation | Screen | Default | Default, Hover |

Primary color buttons use `primary` with `screen` text. Screen filled buttons use `screen` with `ink` text; Ink filled buttons use `ink` with `screen` text. Secondary Screen and Ink buttons have transparent default fills and matching 1px inside borders and text. Filled Hover variants add an **8px outside stroke** in the fill color at 20% opacity. Secondary Hover adds a 20%-opacity fill in its border color while retaining the 1px border. All 32 standalone variants currently use **Ink arrow-right artwork in both icon slots**, regardless of label color; `Color=Screen` does not recolor the selected icon. In particular, Ink-filled examples place Ink icons on Ink. Record this source inconsistency rather than silently changing the icon family or calling the result accessible.

| Size | Text | Filled padding, vertical / horizontal | Outlined padding, vertical / horizontal | Gap | Icon size in source |
| --- | --- | --- | --- | --- | --- |
| Large | 20px / 1.4 | 20 / 40px | 19 / 40px | 12px | Filled 24px; outlined 16px |
| Default | 16px / 1.4 | 16 / 24px | 15 / 24px | 8px | 16px |
| Small | 12px / 1.4 | 12 / 16px | 11 / 16px | 8px | 12px |

With “Jetzt anmelden” and both icons visible, filled specimens measure **291 × 64px** (Large), **207 × 48px** (Default), and **156 × 36px** (Small); outlined specimens are **277 × 56px**, **209 × 48px**, and **158 × 36px** respectively. The **Large Primary-color Hover** specimen (`16:2873`) instead uses 16px icons and measures **275 × 56px**, versus **291 × 64px** and 24px icons in Default (`16:2875`). Large Screen and Ink filled Hover specimens remain 64px high; Large outlined variants remain 56px. These frame dimensions exclude the outside hover stroke. Preserve the measured differences in source documentation, but treat their intended runtime behavior as an unresolved design inconsistency, not an approved hover-resize rule.

Height depends on the visible children in the source: text-only instances are smaller, including the 32px-high Small navigation CTA, 43px-high Default split-hero buttons, and 54px-high Large Shop actions. The desktop Brand action group is also 54px high. Do not impose one fixed height across all instances or use text-layer ink bounds as CSS line-height values.

Navigation is a separate text-and-description pattern with a 12px / 1.4 label, 16px directional icons, optional 8px / 1.4 subtext, and 8px internal gaps. Its outer padding is 12px vertically and 16px horizontally; the standalone Default and Hover specimens measure **164 × 87px** and **168 × 87px**. Hover changes the label to weight 900 at 1.2 line height and changes its measured width; retain this distinction from the regular label. The `Color=Screen` variant name does not mean all nested text is white: the standalone sample uses `ink`; footer instances override their text and chevrons to Screen.

Composed icon overrides remain significant: Navbar's “Produkte” retains an Ink down arrow; dropdown links and FAQ retain Ink chevrons; CTA uses Ink chevrons; Steps actions and footer actions retain Screen chevrons. Hero and Shop actions and field presentations remain text-only. Do not replace those with the standalone default arrow or assume a Button default change automatically overrides every consumer. The re-inspected Navbar, Shop, and FAQ dimensions and typography remain as documented below.

No prototype reactions were found on Button variants or descendants. Pressed, focus, disabled, loading, and icon-only interaction specifications are **to be defined**. The presence of a Hover variant does not establish a hover trigger or animation timing.

### Hero patterns and combinations

All hero recipes reuse the Button and typography foundations. The Brand hero combines full-bleed family photography, a centered Selba title, two actions, and the horizontal white logo near the bottom. Desktop has 96px top / 24px bottom padding, a 738px-wide title/content group, and 64px between title and actions. Its text-only Large Primary and Large Secondary Screen buttons measure 219 × 54px and 221 × 54px, separated by 24px; the 125 × 40px logo sits at x=577.5, y=656. The mobile Brand composition has a 327px-wide content group, 64px top padding, and the same logo size.

The Desktop Neutral/Morning/Day/Night pattern is a text-and-image split: a 439px-wide text column at x=96, and a 535px-wide portrait image at x=745 extending to the right edge. The source portrait is 803px high at y=−41.5 and cropped by the 720px hero. All four text columns now use **96px top/bottom padding, vertical `CENTER` alignment, and a 64px title-to-content gap**, not `SPACE_BETWEEN`. Titles remain left-aligned, at y=157; the description/action group begins at y=398. The two 16px body paragraphs are 16px apart, followed by a 40px body-to-actions gap. Neutral shows a text-only Default Primary action plus Default Secondary Ink action, 16px apart; the range-colored desktop variants show one text-only Default Primary action.

| Type | Desktop | Mobile | Surface token |
| --- | --- | --- | --- |
| Brand | `28:3927` | `28:3922` | Photograph |
| Neutral | `28:3926` | `28:3919` | `screen` |
| Morning | `28:3924` | `28:3920` | `morning` |
| Day | `28:3923` | `28:3918` | `day` |
| Night | `28:3925` | `28:3917` | `night` |

Each ID resolves in the [Hero set](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=28-3928). Mobile Brand retains the 64px Selba title and stacks two text-only Default actions, 16px apart, 40px below its title; the white horizontal logo sits at x=125, y=736 in the 375 × 800px frame.

The other four mobile heroes use the current full-width photographic composition: a 116 × 32px text-only Small Primary action at x=235, y=477, 24px from the right edge; a 16px gap before the full-width text panel at y=525. The panel is 375 × 275px with 40px vertical / 24px horizontal padding, a **center-aligned** 40px Selba title, 40px title-to-body spacing, and two **center-aligned** 16px body paragraphs separated by 16px. Neutral uses Ink on Screen; Morning, Day, and Night use Screen text on their respective colors. The action stays above the panel, not below the description.

The former mobile A variants and A/B property are no longer present in the live set. Document the supplied single mobile composition rather than requiring an absent alternative. This inventory change is not evidence that an A/B test ran or that a winner was established. No prototype reactions were found on any current Hero variant or its descendants.

### Navigation

Default (`44:9822`) is 1280 × 88px on `screen`, with 24px outer insets, a 32 × 32px color 1:1 logo at left, and “Produkte”, “Über uns”, and a Small Primary action at right. The right-hand group is 326 × 40px, with 24px between its 186px-wide link group and 116 × 32px CTA. “Produkte” is a 105 × 40px Navigation instance: its label is followed by an 8px gap and a visible 16px `ink/arrow-down`; the leading icon and description are hidden. “Über uns” is 81 × 32px and vertically centered with the CTA. Preserve the default regular navigation label treatment rather than substituting the active bold appearance.

Dropdown (`44:9821`) is **1280 × 392px** overall. Its 1280 × 88px top bar is followed by a **16px gap** and a **1280 × 288px** Screen panel with a **4px inside Ink outline at 20% opacity** and 16px corner radius. The top-level “Produkte” link uses the bold Hover treatment and measures 109 × 40px; its link group expands to 190px and the full right-hand group to 330px, retaining the 24px gap before the CTA. The panel has 40px vertical / 96px horizontal padding; including the stroke, the 532 × 103px menu starts at x=100px, y=44px and the 200px-square rounded image starts at x=980px, y=44px. Three range groups sit 24px apart and are labeled “morgens”, “tagsüber”, and “abends”, using Morning blue, Day coral, and Night respectively. Their current link labels are “Zur Warteliste”, “Zur Warteliste”, and “Schlafsteine”; descriptions remain placeholder copy.

Mobile closed appearance is [`State=State4`, 90:1646](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=90-1646): 375 × 64px, Screen, 16px vertical / 24px horizontal padding, 32px color logo at left and 32px `ink/asymmetric-parallels` menu artwork at right. Desktop links and the primary CTA are not shown in this bar.

Mobile open appearance is [`State=State3`, 90:1653](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=90-1653): 375 × 464px, retaining the same bar and menu icon, then a 16px gap and a 375 × 384px dropdown with 16px radius, 24px padding, and a 4px inside outline. The menu begins at x=28, y=28 inside the panel (padding plus stroke). A 162 × 328px left column stacks a 16px/900 “Produkte” heading and the three range groups with 8px gaps. Range labels remain 12px in Morning/Day/Night; links are 12px Ink with 16px chevrons and 8px placeholder descriptions. A 40px column gap leads to the 117px-wide right column: a clipped 117 × 216px, 16px-radius portrait, then 16px space and right-aligned “Über Uns”, “Blog”, “Hilfe” links. Those links omit description and directional icons. No separate primary CTA or replacement close icon is shown.

No prototype reactions were found on any Navbar variant or its descendants. Opening/closing triggers, keyboard behavior, sticky positioning, overlay behavior, and destinations remain **to be defined**. `State4` and `State3` are the actual source names, not approved semantic state labels. Static menu appearances do not establish published routes or product availability.

### Shop: Product, Waitlist, Community, Success

Source: [Shop, 68:926](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=68-926). Product belongs to this set, not Sections. Axes are `Step` and `Device=Desktop/Mobile`. All four desktop specimens are **1280 × 814px**, on `screen`, with **96px padding**, **two 439px columns**, and a **210px column gap**. Their inner columns are 622px high. The four mobile compositions are specified separately below.

#### Desktop gallery and benefits

All four desktop steps retain the same left column: a gallery and three benefit pills, separated by 40px. The main image is 439 × 300px with 4px radius. Five 69 × 47px thumbnails with 8px radii form a left-aligned 377 × 47px row, with an 8px main-image-to-thumbnail gap and 8px gaps between thumbnails. In every desktop and mobile step, the first thumbnail's image fill is at 25% opacity and the other four are at 100%; this visible distinction does not establish selected/disabled states or gallery interactions. The main image and all thumbnails repeat the same photograph; do not invent a completed five-image product set. Desktop benefit pills are 439 × 65px, `night-sand`, full radius, 16px vertical / 24px horizontal padding, 16px icon-to-text spacing, and a 24px Ink asterisk icon. Pills are separated by 16px and contain placeholder body copy.

#### Step inventory

| Desktop step / source | Right-column composition | Visible action |
| --- | --- | --- |
| [Product, 49:9884](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-9884) | `abends` range label in Night, 40px Selba “Schlafsteine”, 16px description, 20px “39,90 €” price; purchase action near the bottom | Full-width Large Primary “Jetzt kaufen” |
| [Waitlist, 68:925](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=68-925) | Product heading with directional icon, description and price retained; 20px out-of-stock invitation, E-Mail field, separate email consent row | Full-width Large Primary “Auf Warteliste eintragen” |
| [Community, 68:924](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=68-924) | Product heading with directional icon, E-Mail confirmation presentation and green thank-you panel; invitation to the WhatsApp community, Telefonnummer field, separate phone consent row | Full-width Large Primary “Für Produkttests anmelden” |
| [Success, 68:923](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=68-923) | Product heading, Telefonnummer confirmation presentation and green community confirmation panel | Full-width Large outlined Ink “Zurück zur Website” |

The compositions show a product/waitlist/community sequence, not a complete implemented state machine. One Shop prototype reaction is present: clicking the **Desktop Waitlist component root** (`68:925`) changes to Desktop Community (`68:924`) with `ON_CLICK` → `CHANGE_TO` and no transition animation configured. It is not attached specifically to the submit button and does not establish validation, consent enforcement, or a successful real submission. No other Shop transition was found in inspected variants or descendants; **mobile Waitlist does not inherit this reaction**.

The Community invitation remains **optional**: email waitlist consent is not consent to WhatsApp participation or product-test contact. Do not make a phone number a prerequisite for the email waitlist. The source does not specify the optional skip control or its destination.

#### Desktop fields, consent and confirmation treatment

- **Field presentation:** 439 × 70px label/control stack with an 8px gap; 12px / 1.4 label over a 439 × 54px control, 4px radius, 1px Ink border, 19px vertical / 24px horizontal padding, and 20px text. Waitlist shows “E-Mail” / “...”; Community shows “Telefonnummer” / “+49 ...”. These are sample values, not a phone-format validation specification.
- **Source implementation boundary:** the visible field shells are reused Large Secondary Ink **Button instances**, not a dedicated Input component set. Entry presentations have no fill. The Community email and Success phone presentations reuse `State=Hover`, giving them a 20%-opacity Ink fill. This records their appearance only; it does not establish disabled, read-only, valid, or focused field semantics.
- **Consent rows:** 439 × 28px, with a 24px `ink/box-unchecked` icon, 16px gap, and 399px-wide 8px / 1.4 copy. The email row describes storing/using the address for restock notification; the phone row separately describes storing/using the number for product-test contact. Both mention withdrawal and the underlined Datenschutzerklärung. The form stack uses 16px gaps between the labeled field, consent row, and action. Both box drawings exist in the icon library and local exports, but only the unchecked presentation is composed in Shop; a checked form-control state, focus behavior, and consent submission rules are not established by the artwork alone.
- **Confirmation panels:** Community (`68:804`) and Success (`68:845`) use `night-sage` with Ink content, 439 × 143px, 8px radius, 24px padding, and 16px between the 24px icon and 16px text. Community uses `ink/rocket` with a restock thank-you message. Success uses `ink/heart-fun` and a message about later community contact. This does not establish a global success-color token.
- **Actions:** the shown Shop actions are 439 × 54px, text-only, with 20px labels. Primary actions use 20px vertical / 40px horizontal padding; the outlined return action uses 19px vertical / 40px horizontal padding.

Visible copy includes an out-of-stock statement, a promise of restock notification, and future community contact. These are design examples, not evidence of current inventory, a working integration, approved legal consent, delivery timing, or verified product facts. Price, benefits, consent wording and destinations require current product/legal approval before publication; preserve the distinction from visual fidelity.

#### Mobile Shop compositions

All mobile steps use Screen, a vertical stack, 64px top/bottom and 24px side padding, 327px content width, and 40px between major groups. Category is 16px Night; product name is 40px Selba Ink with 16px category-to-title spacing. Unlike desktop, product information comes before the gallery.

| Mobile step / source | Reference size | Content order and visible differences |
| --- | --- | --- |
| [Product, 91:2297](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=91-2297) | 375 × 941px | Heading, 16px description, 20px price; large gallery; three benefit cards; full-width Large purchase action. No back arrow. |
| [Waitlist, 91:2619](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=91-2619) | 375 × 890px | 24px back arrow above heading, description and price; short gallery; 16px availability message, email field, consent, Default action. No benefits. |
| [Community, 91:2663](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=91-2663) | 375 × 975px | Back arrow and heading; short gallery; email confirmation field and green thank-you panel; 16px optional-community invitation, phone field, consent, Default action. No description, price, or benefits. |
| [Success, 91:2707](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=91-2707) | 375 × 707px | Heading; short gallery; phone confirmation field and green community panel; outlined Default return action. No back arrow, description, price, benefits, or consent row. |

- **Gallery:** the main image is left of a vertical five-thumbnail strip, separated by 8px. Product uses a 275 × 275px clipped main window and five 44px-square thumbnails with 8px gaps, top-aligned in a 44 × 252px strip. Other steps use a 275 × 144px main window and five 44 × 22.4px thumbnails in a 144px-high strip. Main windows and thumbnails have 8px radii; the main 439 × 300px source photograph retains its own 4px radius and is cropped, not proportionately shrunk to the window.
- **Product-only benefits:** three 327 × 49px sand cards follow the gallery after 16px; cards have 16px radius, 12px vertical / 16px horizontal padding, 12px between cards, a 24px Ink asterisk, 16px icon-to-copy gap, and 12px / 1.4 text. Do not carry desktop's full-radius 16px-copy pills into mobile or show benefits in the later mobile steps.
- **Fields:** 327 × 59px label/control stacks retain 12px labels and 8px gaps; controls are 327 × 43px with 16px / 1.4 values, 4px radius, 1px Ink outline, and 15px vertical / 16px horizontal padding. They reuse **Default Secondary Ink Buttons**; confirmation presentations again reuse Hover's 20%-Ink fill. Sample phone text is “+49 ...” for entry and “+49 ” in Success. Label layers still measure 439px although their mobile stacks are 327px; treat this as unresolved source sizing, not a mobile overflow requirement.
- **Consent:** a 24px unchecked drawing, 16px gap, and 287px-wide 8px / 1.4 text; email row is 50px high, phone row 39px. Field, consent, and action remain 16px apart. No composed checked state or working input behavior is supplied.
- **Confirmation:** 327px-wide sage panels with 8px radius, 16px padding, 16px icon, and 16px body copy. Community is 137px high with a rocket and 12px icon-to-copy gap; Success is 141px high with a heart and 16px gap. This is not the desktop 24px-icon/24px-padding recipe.
- **Actions:** Product remains 327 × 54px, Large Primary, 20px label. Waitlist is 327 × 43px and Community 327 × 48px, both text-only Default Primary with 16px labels and 16px vertical / 24px horizontal padding. Success is 327 × 43px Default Secondary Ink with 16px label and 15px vertical / 24px horizontal padding. Preserve the measured Community height difference rather than declaring all text-only Default actions identical.

**To be defined:** gallery selection and active thumbnails; purchase/stock routing and transitions beyond the Desktop Waitlist-root prototype click; back/return/optional-skip destinations; editable versus read-only field behavior; required fields and consent enforcement; focus, checked-control, error, validation, loading, and submission-failure states; keyboard/screen-reader behavior; email/phone processing and WhatsApp integration; and breakpoint/interpolation rules between supplied desktop and mobile compositions. No mobile Shop reactions were found. Prototype navigation is not a working form.

### FAQ item and section

[FAQ items](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-9915) now use `Collapsed` and `Device=Desktop/Mobile`. The source naming is counterintuitive: **`Collapsed=OFF` is question-only** (Desktop `49:9914`, Mobile `91:2132`), while **`Collapsed=ON` shows the answer** (Desktop `49:9913`, Mobile `91:2136`). Preserve this mapping when identifying variants; do not infer conventional boolean semantics from the names.

Desktop questions are 20px / 1.2 with 16px / 1.4 answers, 24px question-to-answer spacing, and a 16px Ink chevrons icon separated by 64px. Standalone specimens are now **723px wide**, 16px high question-only and 93px with answer. Mobile standalone specimens are **also 723px wide**, not phone-width: questions and answers are both 16px / 1.4, answer spacing is 16px, icon gap is 16px, and heights are 16px / 60px. The composed section below supplies the actual narrow arrangement. Closed/open chevrons use −90°/+90° instance rotation.

[Desktop FAQ section, 49:10113](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10113) remains 1280 × 669px, Screen, with 96px padding and a centered 718px-wide list. Five items show four questions only and one answer, separated by 1px Ink dividers and 40px gaps between list children.

[Mobile FAQ section, 91:1881](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=91-1881) is **375 × 622px**, with 64px vertical / 24px horizontal padding and a 327 × 494px list. It retains five items, the last answer-visible, with 24px gaps around divider children. Closed items are 327 × 33px with a 295px text column and 16px icon gap; the open instance is 327 × 170px with a 287px text column and **24px icon gap**, overriding the standalone mobile 16px gap. Content determines these heights.

No reactions were found on either device's FAQ item variants or FAQ sections and descendants. Single-open versus multiple-open behavior, switching triggers, animation, keyboard/screen-reader interaction, and final questions/answers remain **to be defined**.

### Video / full-width media

[Desktop Video, 53:10756](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=53-10756) is 1280 × 669px; [Mobile Video, 91:1892](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=91-1892) is **375 × 669px**. Both are photographic-fill surfaces with no child playback controls; the narrow frame changes the crop, not the specified height. Neither has prototype reactions. A video asset, playback controls, autoplay/mute/loop rules, captions, poster behavior, and responsive sizing between references remain **to be defined**. The component name does not specify a working player.

### CTA band

[Desktop CTA, 49:10157](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10157) combines a `night-sand` surface, white copy, a white filled button with Ink text/chevrons, and a large cropped product image on the right. Reference size: 1280 × 307px. The left inset is 96px; the 625px copy column has 40px top/bottom padding, 24px between title and body, and 40px to the button. The 559px right image window crops the larger product artwork. Preserve this crop rather than shrinking the entire image to fit.

The displayed title is “Schritt für Schritt / Block für Block.” Use `title-xs`, `body-tall`, and the Default Screen filled button. [Mobile CTA, 91:1893](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=91-1893) is **375 × 681px**, stacking copy and artwork on the same sand surface. It has 64px top padding; the content group uses 24px side insets, a 327px-wide **center-aligned** 40px Selba title and 20px body, 24px title-to-body gap, then 40px before a centered 162 × 48px Screen button with 16px Ink label and trailing 16px Ink chevrons. After a **46px measured gap**, the 375 × 172px clipped image window begins at y=509. The approximately 402px-square product image is rotated −18.12° and offset right/up; retain the pronounced crop instead of centering or fitting all the artwork. The 46px gap is a source measurement, not a new spacing token. No reactions were found on either CTA variant or descendants. Final copy, action destination, and breakpoint rules remain **to be defined**.

### Steps panels

Source: the standalone [Steps set, 72:1422](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=72-1422), not Sections. Axes are `Step=1/2/3/4` and `Device=Desktop/Mobile`, giving **eight supplied appearances**, one expanded panel per variant; Desktop Step 1 is default.

| Step | Desktop source | Mobile source | Expanded panel |
| --- | --- | --- | --- |
| 1 | `49:10301` | `91:2920` | First — `night-sand` |
| 2 | `72:1421` | `91:3188` | Second — `night-sage` |
| 3 | `72:1420` | `91:3255` | Third — `night-lavender` |
| 4 | `72:1419` | `91:3322` | Fourth — `night` |

Every desktop reference is now **1280 × 637px**, with 96px padding and 24px gaps. All panels are **445px high** with 16px radius. Desktop panel order stays sand, sage, lavender, night, but compact widths are not equal and Step 4 has a wider expanded panel:

| Desktop Step | Sand / Sage / Lavender / Night panel widths | Expanded content order |
| --- | --- | --- |
| 1 | **718 / 161 / 68 / 69px** | Copy left, image right |
| 2 | **69 / 718 / 161 / 68px** | Image left, copy right |
| 3 | **69 / 68 / 718 / 161px** | Copy left, image right |
| 4 | **69 / 68 / 69 / 810px** | Image left, copy right |

Desktop compact panels have 40px top/bottom and **zero horizontal padding**, centered 32px Screen alarm-clock icons, and 90°-rotated 32px / 1.2 Figtree headings. They use `SPACE_BETWEEN`; configured 200px item spacing is not a fixed rendered gap. Expanded panels now use a **horizontal** layout, 40px padding, and a **24px gap** between equal-width copy and portrait columns: **307 × 365px** each for Steps 1–3 and **353 × 365px** each for Step 4. Copy contains a 32px icon and 16px label with a 16px gap; 24px to the heading/body group; a 32px / 1.2 heading and 16px / 1.4 body separated by 24px; then **96px** before the 130 × 36px Small Secondary Screen “Mehr erfahren” action with trailing 12px Screen chevrons. The image window has **8px radius** and clips a **559 × 373px** photograph at x=−113, y=−4. This replaces the former short landscape window below the copy.

Mobile Steps **1–3 are 375 × 887px; Step 4 is 375 × 863px**. All use 64px vertical / 24px horizontal padding and **12px gaps** between four vertically stacked 327px-wide, 8px-radius panels. Expanded panels remain **327 × 555px**, with 24px padding and a **40px gap** between the **279 × 323px** copy group and **279 × 144px** image window. Steps **1 and 3 place copy before the image**; Steps **2 and 4 place the image before copy**. The image has 4px radius and clips the 467 × 311px photograph at x=0, y=−50. Copy retains a 24px Screen alarm-clock, 16px label, 16px icon-to-label gap, 24px between label/description/action, a 32px / 1.2 heading, 16px / 1.4 body with 24px heading-to-body spacing, and the same 130 × 36px Small outlined Screen action.

Mobile compact panels are **327 × 48px** with 12px vertical / 24px horizontal padding, except the panel immediately following the expanded panel in Steps 1–3, which is **327 × 72px** with **24px padding on every side**. Thus the taller compact panel is sage in Step 1, lavender in Step 2, and night in Step 3; Step 4 has only 48px compact panels. All use 24px Screen icons and unrotated 20px / 1.4 Figtree labels, with `SPACE_BETWEEN` rather than a literal 200px gap. Preserve icon placement: Step 1's compact sage/night icons are left and lavender right; Step 2's compact sand/night icons are left and lavender right; Step 3's compact sage/night icons are left and sand right; Step 4's compact sage/sand icons are left and lavender right.

**Source differences requiring an intent decision:** Mobile Steps 1–2 order the colors sand, sage, lavender, night, but Mobile Steps 3–4 place **sage before sand**, then lavender and night. Desktop keeps the consistent color order, yet Steps 1–3 include one wider compact panel and Step 4 instead allocates that space to the expanded panel. The mobile 72px/48px compact-height distinction similarly makes Step 4 shorter overall. Record these actual per-variant geometries; do not silently equalize them or infer runtime resizing behavior.

Expanded states reuse the same placeholder text, icon, action, and photograph, not four approved content stories. No prototype reactions are assigned to the inspected Steps variants or descendants. Switching triggers, keyboard behavior, animation, action destinations, final copy, and breakpoint rules remain **to be defined**. Both device layouts are designed; an interactive accordion is not yet specified.

### Testimonials

[Desktop Testimonial, 49:10302](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10302) is **1280 × 303px** on Screen, with 64px vertical / 96px horizontal padding, 24px card gaps, and vertically centered children. It now contains **four cards**, with one larger opaque card and three smaller cards whose **background fills alone are at 20% opacity**; text/icons remain Screen at 100%:

| Desktop order / source | Surface | Reference size | Position in section | Quote / attribution |
| --- | --- | --- | --- | --- |
| 1 — `49:10303` | Night, 20% fill | 254 × 138px | x=96, y=82.5 | 12px / 8px |
| 2 — `49:10391` | Morning, opaque | 347 × 175px | x=374, y=64 | 16px / 12px |
| 3 — `97:3486` | Day, 20% fill | 254 × 138px | x=745, y=82.5 | 12px / 8px |
| 4 — `97:3510` | Morning, 20% fill | 254 × 138px | x=1023, y=82.5 | 12px / 8px |

All desktop cards have 16px radius and 16px internal gaps. The larger card uses 24px vertical / 40px horizontal padding and four 24px stars; smaller cards use 16px vertical / 24px horizontal padding and five 16px stars each. Stars have 8px gaps. Attribution uses a 16px person icon with an 8px gap. The four-card row is **1181px wide** and ends at x=1277 inside the clipped 1280px frame, extending past the configured 96px right inset; do not hide or redistribute the fourth card to manufacture a symmetric row.

[Mobile Testimonial, 91:1901](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=91-1901) is now **375 × 661px**, with 64px vertical / 24px horizontal padding and three horizontally centered cards separated by 24px. The first is **327 × 175px**, opaque Day at x=24, y=64, with 24px padding, five 24px stars, 16px quote and 12px attribution. The following Morning (`91:1913`) and Night (`97:3534`) cards are each **214 × 155px**, at x=80.5 and y=263 / 442, with **20%-opacity fills**, 16px padding, four 16px stars, 12px quotes, and 8px attribution. All retain 16px radius, 16px internal gaps, 8px star gaps, and a 16px person icon with an 8px attribution gap; copy uses 1.4 line height and stays fully opaque.

Use the supplied outlined star and person artwork. The differing size/fill treatments are observed appearances, not named selected/disabled states or a defined carousel: no reactions, switching controls, or playback rules are supplied on either device. Star counts, quotes, and “Mama einer Tochter” attribution are placeholder examples, not evidence of customer ratings. Real quotes, attribution, rating provenance, behavioral intent, and breakpoint rules remain **to be defined**. Do not populate this pattern with persona simulations or invented testimonials.

### Footer

[Type=Footer, 49:10755](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=49-10755) is now **1280 × 421.7px** (approximately 422px high) on Ink, with 96px horizontal / 40px vertical padding. Its horizontal auto-layout distributes two bottom-aligned main groups: 254px and 625px wide, both 341.7px high. It combines:

- A left column with an additional 40px top inset: a Small white horizontal logo measuring approximately 108.44 × 34.7px, followed after 24px by a 254px-wide 12px / 1.4 brand paragraph. The newsletter group follows the brand-information group after 40px.
- A 254 × 93px newsletter presentation with 8px vertical gaps: the 8px / 1.4 heading “zum newsletter anmelden”; a 200 × 32px “Deine E-Mail” field shell and 46 × 32px icon-only action separated by 8px; then a 16px white unchecked-box drawing, **8px gap**, and **230px-wide** 8px / 1.4 consent text. The 254 × 39px consent row starts 54px below the newsletter group's top; checkbox and text are top-aligned, with text at x=24px. The field and action reuse Small Secondary Screen Button instances with 1px white outlines and 4px radii; the field label is 12px / 1.4 and the action contains a 12px chevron icon. These are visual presentations, not evidence of editable input or working newsletter submission.
- Product and resource columns, each 161px wide, using 8px / 1.4 headings (“Produkte”, “Ressourcen”), 12px / 1.4 Navigation labels, 8px / 1.4 descriptions, and 16px directional icons. Product labels are “Schlafsteine”, “Zur Warteliste”, and “Zur Warteliste”; resource labels are “Über uns”, “Blog”, and “Hilfe”. Descriptions remain placeholder copy. These instances keep `ink/chevrons` as their selected icon component but override its actual vector paint to **Screen**, matching the white text; do not render Ink merely from that component name. Desktop footer instances remove the standard Navigation left padding; the last item in each column also removes bottom padding.
- Three approximately 24px social marks with 16px gaps, right-aligned above the 625 × 301.7px navigation/portrait row with 16px separation. That row has 24px gaps between the two link columns and a 255px-wide portrait/legal column. The portrait window is 255 × 271.7px with 16px radius, clipping the supplied drawing-family image. Legal links now sit 24px below the image, distributed with `SPACE_BETWEEN` across the full 255px width, rather than below the brand paragraph.

The current paragraph reads: “Manchmal braucht ein eigener Versuch etwas Zeit und jemanden, der den Reißverschluss festhält. Mit selba möchten wir solchen Versuchen mehr Platz im Familienalltag geben. Dafür entwickeln wir einfache, spielerische Werkzeuge, die zum Mitmachen einladen und Raum für euren eigenen Weg lassen.” Preserve its supplied hierarchy and regular Body-Small treatment.

The newsletter consent reads: “Ich bin damit einverstanden, dass selba meine E-Mail-Adresse speichert und nutzt, um miR den Newsletter zu schicken. Weitere Informationen finde ich in der Datenschutzerklärung.” The privacy reference is underlined; the source capitalization “miR” is retained here as an editorial issue, not silently corrected or treated as approved legal copy.

[Mobile Footer, 91:1934](https://www.figma.com/design/bquEWK6I7VBANubD3RHJLp/selba?node-id=91-1934) is now **375 × 819.32px** on Ink, with 40px vertical / 24px horizontal padding, 40px gaps between major groups, and centered cross-axis alignment. Its supplied order differs from desktop:

1. **Centered** white horizontal logo, approximately **101 × 32.32px**, at x=137, y=40.
2. A **327 × 207px** product-link stack with **no “Produkte” heading**. All three Navigation instances are **327 × 69px**, with centered label/icon groups and center-aligned 299px-wide descriptions. Labels remain 12px, chevrons 16px, and descriptions 8px; chevron vector paint is overridden to Screen. Each instance uses top/right/bottom/left padding of **12 / 16 / 16 / 12px** and 8px between its label group and description. Preserve these asymmetric insets rather than carrying over desktop's zero-left/last-item-zero-bottom treatment.
3. A **327 × 124px** image/resources row: **242.47 × 124px**, 16px-radius portrait crop on the left, a 12px gap, and a 72.53px-wide right column. “Über uns”, “Blog”, and “Hilfe” are right-aligned without the desktop resource heading, descriptions, or directional icons. Three approximately 16px social marks sit below those links, with 12px gaps and 24px separation from the link stack.
4. The **327px-wide brand paragraph**, then a **24px gap** before a **327 × 93px newsletter**. It keeps 8px internal gaps, an 8px heading, a **273 × 32px** email shell, 8px gap, and the **46 × 32px** icon-only submit presentation. Consent uses a 16px unchecked drawing, 8px gap, and **303px-wide** 8px / 1.4 text; row height is 39px. Small Secondary Screen styling, 4px radii, and 1px outlines remain. The visible email text is 12px; submit's text is hidden and its 12px chevrons remain visible.
5. Legal links distributed across the full **327px width**, 40px after the brand/newsletter group, rather than immediately beneath the image as on desktop.

The source legal labels remain Impressum, Datenschutz, AGBs, and Sicherheit, all 8px / 1.4. No reactions were found on either Footer variant or descendants. Legal/newsletter consent copy, link descriptions, routes, social profile destinations, exported social-mark assets, newsletter processing and submission states, and breakpoint rules remain **to be defined**. Repeated waitlist labels do not establish distinct destinations or availability. The icon-only newsletter action does not resolve its accessible name, focus, validation, checked-consent, success, or error behavior.

### Reuse and asset mapping

Paths below are relative to this document. Match the source frame’s crop and logo variant; filenames alone do not authorize a different composition.

| Designed use | Existing asset |
| --- | --- |
| Brand desktop hero / full-width media scene | [01-family-a-building-landscape.png](../../assets/imagery/brand/01-family-a-building-landscape.png), visually matched to the family/building scene |
| Mobile heroes, dropdown, footer portrait scene | [02-family-a-drawing-portrait.png](../../assets/imagery/brand/02-family-a-drawing-portrait.png); dropdown/footer layers explicitly use this filename; preserve each crop |
| Split desktop hero portrait | [04-family-a-rabbit-portrait.png](../../assets/imagery/brand/04-family-a-rabbit-portrait.png), named in the Figma layers |
| Product gallery and thumbnails, all four Shop steps | [07-final-stone-detail-landscape.png](../../assets/imagery/products/night/07-final-stone-detail-landscape.png), named in the Figma layers and repeated in every main image and thumbnail; preserve the thumbnail crops, 8px radii, and first-thumbnail 25% image-fill opacity |
| CTA product artwork | [schlafsteine.png](../../assets/imagery/products/night/schlafsteine.png), named in the Figma layer |
| Expanded Steps images | [04-shared-story-landscape.png](../../assets/imagery/products/night/04-shared-story-landscape.png), named in the Figma layers; desktop uses a 559 × 373px source at (−113, −4) inside 307/353 × 365px portrait windows, mobile a 467 × 311px source at (0, −50) inside 279 × 144px windows; preserve the distinct crops and alternating image/copy order |
| Navigation logo | [1:1 color SVG](<../../assets/logo/svg/Format=1_1, Color=color, Size=Large.svg>); scale the supplied vector to the 32 × 32px Small instance |
| Brand hero horizontal white logo | [default Screen SVG](<../../assets/logo/svg/Format=default, Color=screen, Size=Large.svg>); scale the supplied vector to the 125 × 40px Small instance |
| Other logo placements | [Logo assets](../../assets/logo/); match format, color, and size to the instance |
| Standalone Button default icons | [Ink arrow-right](../../assets/icons/ink/arrow-right.svg); both slots use this artwork in every standalone variant, including white-label and Ink-filled examples; composed overrides below remain distinct |
| FAQ / dropdown / CTA directions | [Ink chevrons](../../assets/icons/ink/chevrons.svg); Navbar “Produkte” uses the separate down arrow below |
| Navbar “Produkte” trailing direction | [Ink arrow-down](../../assets/icons/ink/arrow-down.svg); the Default instance displays the trailing icon at 16 × 16px, with its leading icon hidden |
| Product feature pills | [Ink asterisk](../../assets/icons/ink/asterisk.svg) |
| Shop confirmation panels | [Ink rocket](../../assets/icons/ink/rocket.svg) · [Ink heart-fun](../../assets/icons/ink/heart-fun.svg) |
| Shop consent artwork | [Ink unchecked box](../../assets/icons/Icons/ink/box-unchecked.svg); [checked box artwork](../../assets/icons/Icons/ink/box-checked.svg) is also available, but not composed as a checked Shop state |
| Shop directional icon | [Ink arrow-right](../../assets/icons/ink/arrow-right.svg); preserve the source orientation |
| Steps | [Screen alarm-clock](../../assets/icons/screen/alarm-clock.svg) |
| Steps actions / footer directions | [Screen chevrons](../../assets/icons/screen/chevrons.svg); Steps and newsletter buttons select this component, while footer Navigation instances select Ink chevrons with a verified Screen paint override |
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
  button-standalone-icons:
    artwork: ink/arrow-right
    color: "{colors.ink}"
  button-filled-hover:
    strokeWidth: 8px
    strokeAlign: outside
    strokeOpacity: 0.2
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
  hero-desktop-split:
    contentVerticalAlignment: center
    titleToContentGap: "{spacing.64}"
    bodyToActionGap: "{spacing.40}"
    textAlignment: left
  hero-mobile-non-brand:
    textAlignment: center
    titleToBodyGap: "{spacing.40}"
    paragraphGap: "{spacing.16}"
  product-feature-pill:
    backgroundColor: "{colors.night-sand}"
    textColor: "{colors.ink}"
    desktopRounded: "{rounded.full}"
    desktopTypography: "{typography.body}"
    mobileTypography: "{typography.body-small}"
    mobileRounded: "{rounded.16}"
  shop-confirmation-panel:
    backgroundColor: "{colors.night-sage}"
    textColor: "{colors.ink}"
    rounded: "{rounded.8}"
    typography: "{typography.body}"
  navbar:
    backgroundColor: "{colors.screen}"
    desktopReferenceWidth: 1280px
    desktopReferenceHeight: 88px
    mobileReferenceWidth: 375px
    mobileReferenceHeight: 64px
    horizontalInset: "{spacing.24}"
    desktopLinkGroupToActionGap: "{spacing.24}"
  dropdown:
    backgroundColor: "{colors.screen}"
    rounded: "{rounded.16}"
    topBarToPanelGap: "{spacing.16}"
    desktopPanelReferenceWidth: 1280px
    desktopPanelReferenceHeight: 288px
    mobilePanelReferenceWidth: 375px
    mobilePanelReferenceHeight: 384px
    strokeWidth: 4px
    strokeAlign: inside
    strokeColor: "{colors.ink}"
    strokeOpacity: 0.2
  cta-band:
    backgroundColor: "{colors.night-sand}"
    textColor: "{colors.screen}"
    desktopTextAlignment: left
    mobileTextAlignment: center
  steps-desktop:
    referenceWidth: 1280px
    referenceHeight: 637px
    outerPadding: "{spacing.96}"
    panelGap: "{spacing.24}"
    panelReferenceHeight: 445px
    panelRounded: "{rounded.16}"
    expandedPadding: "{spacing.40}"
    expandedColumnGap: "{spacing.24}"
    expandedMediaRounded: "{rounded.8}"
  steps-mobile:
    referenceWidth: 375px
    steps1To3ReferenceHeight: 887px
    step4ReferenceHeight: 863px
    verticalPadding: "{spacing.64}"
    horizontalPadding: "{spacing.24}"
    panelGap: "{spacing.12}"
    panelRounded: "{rounded.8}"
    expandedPadding: "{spacing.24}"
    expandedContentToMediaGap: "{spacing.40}"
    expandedMediaRounded: "{rounded.4}"
    compactReferenceHeight: 48px
    followingCompactSteps1To3ReferenceHeight: 72px
  testimonial-large:
    desktopBackgroundColor: "{colors.morning}"
    mobileBackgroundColor: "{colors.day}"
    backgroundFillOpacity: 1
    textColor: "{colors.screen}"
    rounded: "{rounded.16}"
    quoteTypography: "{typography.body}"
    attributionTypography: "{typography.body-small}"
    desktopReferenceWidth: 347px
    mobileReferenceWidth: 327px
    referenceHeight: 175px
  testimonial-small:
    desktopBackgroundColors: ["{colors.night}", "{colors.day}", "{colors.morning}"]
    mobileBackgroundColors: ["{colors.morning}", "{colors.night}"]
    backgroundFillOpacity: 0.2
    contentOpacity: 1
    textColor: "{colors.screen}"
    rounded: "{rounded.16}"
    quoteTypography: "{typography.body-small}"
    attributionTypography: "{typography.captions}"
    desktopReferenceWidth: 254px
    desktopReferenceHeight: 138px
    mobileReferenceWidth: 214px
    mobileReferenceHeight: 155px
  footer:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.screen}"
    mobileReferenceWidth: 375px
    mobileReferenceHeight: 819.32px
    mobileLogoAlignment: center
    mobileProductDescriptionAlignment: center
  footer-newsletter:
    stackGap: "{spacing.8}"
    fieldToActionGap: "{spacing.8}"
    consentIconToTextGap: "{spacing.8}"
    desktopConsentTextReferenceWidth: 230px
    mobileConsentTextReferenceWidth: 303px
```

### Combining the patterns

Reuse the supplied device-specific combinations: photo + title + action(s) + logo in Brand Hero; product information + gallery + step-specific form/confirmation content in Shop, with benefits in every desktop step but only mobile Product; question/answer items + dividers in FAQ; horizontal desktop and vertical mobile Steps arrangements with alternating copy/image order inside expanded panels; differently sized rating + quote + attribution cards in the four-card desktop and three-card mobile Testimonial compositions; and the differently ordered and aligned logo, newsletter, navigation, portrait, brand paragraph, and legal groups in Footer.

The Web page presents separate reusable component sets. Their canvas order is not an approved website sitemap or page sequence. Final page inventory, section order, navigation destinations, and rules for combining sections into complete pages are **to be defined**. Do not treat repeated sample actions as separate confirmed user journeys.

## Unresolved source and publication conflicts

- **Color names and swatch labels:** the specific Figma/digital.md discrepancies are recorded in Colors. Applied fills and variable values establish the reference appearance; the conflicting labels and token spelling still require reconciliation in their owning sources.
- **Large button sizing:** Primary-red Default is 64px high but Hover is 56px; Large Secondary is 56px in both states. Other Large filled colors remain 64px. Do not call this intentional or normalize it without a design decision.
- **Button icon defaults versus composed overrides:** every standalone Button variant now uses Ink arrow-right artwork, including Ink-filled variants where the icon matches the background. White labels do not imply white icons. CTA, Navbar, Steps, and Footer retain explicit icon choices/paint overrides; reconcile the standalone contrast and icon-color intent in Figma instead of forcing all consumers to a single treatment.
- **Steps geometry and order:** all desktop frames are now 1280 × 637px, but compact widths vary by Step and Step 4 has an 810px expanded panel instead of 718px. Mobile Steps 1–3 retain one 72px compact panel each while Step 4 has only 48px compact panels and a shorter 863px frame. Mobile Steps 3–4 still swap the first two colors. These source differences do not define animation or runtime resizing rules.
- **Testimonial presentation:** desktop has four cards but mobile has three, and the larger opaque card differs by device. The desktop row extends 93px into the configured right inset. Smaller cards use 20%-opacity background fills with fully opaque white text/icons and smaller 12px/8px copy. No selected-state, scrolling, carousel, or transition semantics are supplied; confirm behavioral intent and contrast rather than inventing them.
- **“Bold” typography naming:** `Typography/Body-Bold` and `Typography/Body - Small - Bold` use Figtree Black/900, not 700. Whether to rename those styles or change their weight remains an owner decision; this document retains the actual 900 values.
- **Shop control semantics:** field-looking nodes still reuse Button variants, including Hover for confirmation presentations. Checked/unchecked box artwork is available, but real input/confirmation states, a composed checked-control state, optional-community exit, validation, submission and consent behavior remain unspecified. The Desktop Waitlist-root click-to-Community prototype reaction does not resolve those requirements or establish mobile wiring.
- **Accessibility versus visual fidelity:** the source's white text on `morning`, `day`, `night-sand`, `night-sage`, `night-lavender`, and `primary` includes normal-text combinations below the WCAG AA 4.5:1 threshold. Some also fall below the 3:1 large-text threshold. The smaller testimonial cards' 20%-opacity fills against Screen further reduce contrast, and standalone Ink-filled Buttons use Ink icons. Preserving the reference does not establish accessible production use. Resolve contrast, the 8px attribution/consent/legal copy, focus treatment and interaction accessibility with the design owner rather than silently recoloring or claiming conformance.
- **Other mobile source inconsistencies:** FAQ's `Collapsed=ON` is the answer-visible state and `OFF` question-only; its standalone Mobile items are 723px wide, while composed instances are 327px. The mobile open instance uses a 24px icon gap versus the standalone 16px. Mobile Shop field-label layers remain 439px wide inside 327px stacks, and its text-only Community action is fixed at 48px high versus Waitlist's 43px hug-height action. Navbar Mobile uses generic `State4`/`State3` names. Preserve observed evidence without declaring these differences intentional.
- **Publication evidence:** placeholder benefits/descriptions, price, out-of-stock and contact promises, consent/legal copy, sample testimonials, routes and integrations remain unverified. Desktop and mobile compositions are now supplied for every section family, but viewport breakpoints, intermediate layouts, and runtime behavior are not. The removed Hero A/B alternatives do not establish test results.

## Do's and Don'ts

- **Do** preserve the supplied desktop/mobile compositions, component-specific spacing, content omissions, and icon visibility; record unresolved differences instead of assuming intent.
- **Do** reuse canonical palette tokens and supplied assets; map differing Figma names by actual value.
- **Do** use Selba for display titles and Figtree for the documented text and control roles.
- **Do** use the current Hero inventory; do not recreate removed mobile alternatives or claim a test winner without evidence.
- **Do** keep children active in the story and preserve the photograph’s meaningful gestures and product details when matching crops.
- **Do** follow the brand’s factual boundaries: use verified product information and traceable real testimonials.
- **Don’t** import the generic template’s fonts, palette, components, or example rules into selba.
- **Don’t** infer breakpoints, intermediate responsive layouts, additional form states, animation timing, navigation behavior, or routes from static frames.
- **Don’t** treat Shop's supplied email/phone fields and consent rows as a complete form-control library, or invent radio buttons, tooltips, validation states, or additional controls merely because a generic format mentions them.
- **Don’t** turn sample copy, prices, star counts, or persona stories into claims of verified product or customer facts.
- **Don’t** add illustrations to existing compositions simply because overlays are available.