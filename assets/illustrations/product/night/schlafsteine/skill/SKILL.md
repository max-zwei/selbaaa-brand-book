---
name: selba-bedtime-illustrations
description: Write reference-based illustration prompts for the existing selba bedtime-routine boy and girl, given a character and an activity. Preserve their approved SVG identity, clothing, palette, and small-print style when extending the collection; also guide artwork creation when explicitly requested.
---

# Selba bedtime illustrations

Extend the approved bedtime-routine collection with the same boy or girl performing a new activity. The character definitions below reflect the actual approved SVGs, not the earlier brief: both children have peach skin; the boy wears sage pyjamas and the girl wears lavender pyjamas.

## Inputs and output

Required inputs:
- `character`: `boy` or `girl` (accept natural-language equivalents).
- `activity`: a bedtime-routine action in plain language, such as “washing hands,” “cuddling a teddy,” or “closing the curtains.”

Optional inputs: daytime clothing or pyjamas, a specific pose or prop, updated approved references, and output mode.

Infer the required inputs from the user's request and established context. Ask only for missing required inputs. Do not restrict activities to the examples in this skill. If the user requests both children or several activities, create the corresponding separate prompts.

Default output: one complete, copyable illustration prompt assembled from the selected character template, a concrete activity scene, and the shared production template below. Replace all template variables; the final prompt must stand alone without references to “the shared section” or this skill. Include the three reference filenames and make the corresponding files available to the recipient. A filename alone is not an attached reference.

If the user explicitly asks to create the artwork, apply the assembled prompt to that work. Do not generate images merely because the skill was invoked to write a prompt. Native SVG output requires actual editable vector paths; a raster preview or raster image embedded in SVG does not satisfy that deliverable. Use the available vector-authoring workflow for SVG work and report any unavailable capability honestly.

Example invocations:
- `$selba-bedtime-illustrations girl washing her face`
- `$selba-bedtime-illustrations boy cuddling a soft toy`
- `$selba-bedtime-illustrations boy putting away his slippers, already in pyjamas`

## Approved references

Read only the selected child's three SVGs unless a cross-series comparison is needed. Paths are relative to this skill folder:

| Character | Daytime appearance | Dressing pose | Completed pyjamas |
| --- | --- | --- | --- |
| Boy | [boy-brushing-teeth.svg](assets/boy-brushing-teeth.svg) | [boy-putting-on-pyjamas.svg](assets/boy-putting-on-pyjamas.svg) | [boy-picking-a-book.svg](assets/boy-picking-a-book.svg) |
| Girl | [girl-brushing-teeth.svg](assets/girl-brushing-teeth.svg) | [girl-putting-on-pyjamas.svg](assets/girl-putting-on-pyjamas.svg) | [girl-picking-a-book.svg](assets/girl-picking-a-book.svg) |

The bundled files are approved originals copied from:
`/Users/max/Documents/GitHub/selbaaa-brand-book/assets/illustrations/product/night/schlafsteine/`

Prefer newly supplied, explicitly approved references when the user updates the character. Otherwise use the bundled files. If this SKILL.md is used without its assets, try the original directory; if neither is available, request the three references rather than claiming to have inspected or extracted them.

When producing artwork, inspect rendered references as well as their SVG structure. For prompt-only work, the templates supply the established appearance, but the recipient still needs the actual reference files for extraction and matching. Preserve the approved source files.

## Build the activity scene

Convert `activity` into one clear, frozen action. Specify:
- Body position and viewing angle, keeping recognizable facial and hair features visible where practical.
- What each hand is doing and the exact contact with the relevant object.
- One principal prop, with at most a few secondary context shapes.
- The visible cue that distinguishes the action from merely standing beside or holding the prop.
- Only activity-specific exclusions that prevent likely ambiguity or impossible anatomy.

Choose clothing from the routine stage. Unless the user specifies otherwise, use daytime clothing for tidying toys, brushing teeth, washing hands, and washing the face; use completed pyjamas for choosing or reading a book, drinking bedtime water, cuddling a toy, getting into bed, and switching off a lamp. For a new activity, infer its likely stage and state the chosen outfit in the prompt. Do not ask a separate clothing question when a reasonable choice is available.

For dressing activities, describe the transitional garment state instead of inserting the completed-outfit rule.

Use a short English kebab-case activity slug, e.g. `washing-hands`, for `{activity-slug}`. Preserve the boy/girl filename prefix. For paired scenes, keep the action, principal prop, and background treatment coordinated while preserving each child's identity and clothing.

### Proven activity staging

Use these as starting points for these activities, not as a mandatory seven-scene output:

| Activity | Pose and readable action | Minimal context |
| --- | --- | --- |
| Tidying toys | Crouching or kneeling; one hand lowers a large block partly through the basket opening; the other rests on a knee or the rim. | Low sand basket; at most two other toys. |
| Washing hands | Three-quarter view; both hands rub together under a short water stream, visible above the basin rim. | Reuse the reference basin and curved tap; one or two broad foam shapes. |
| Washing the face | One hand presses a small sage washcloth against one cheek; the other arm rests naturally; most of the face and fringe remain visible. | A quiet glimpse of the reference basin. |
| Drinking water | Both hands hold a plain navy cup with its rim touching the lips; slight tilt; face and grip remain readable. | Small oval rug or short floor line; no straw or lettering. |
| Reading a book | Seated on a small sage rug; an open book rests across the lap, both hands supporting its outer edges; gaze downward. | Reference sage book cover, two broad white pages, at most one simple picture; no words or bookshelf. |
| Cuddling a soft toy | Seated on a low bed edge; both arms wrap visibly around a small sand teddy; head tilts toward it. | A small sage blanket section and white pillow; minimal teddy features. |
| Switching off a lamp | Standing beside a low table; fingertip visibly contacts a switch on the lamp base; other arm relaxed. | Sage shade and navy base; lamp within reach, unlit, without glow or motion symbols. |

For book selection, show a closed book partly withdrawn from a shelf with a plausible grip. For reading, show an open book and the child's attention directed to its pages. For putting on pyjamas, make the raised shirt and hands pulling its hem visibly distinct from a fully worn outfit.

## Girl prompt template

Use this character block, then insert the resolved activity scene and the complete shared production template.

```text
Create one additional bedtime-routine illustration featuring the EXACT SAME girl shown in the three supplied reference SVGs, performing this activity: {activity}.

This extends an approved collection. It must look like a new pose of the original girl, not a newly designed character. The illustration will be printed approximately 25–30 mm wide.

REFERENCE FILES — REQUIRED
- girl-brushing-teeth.svg
- girl-putting-on-pyjamas.svg
- girl-picking-a-book.svg

Treat the supplied artwork as the source of truth for character identity, proportions, colors, linework, and style. Where a generic written description conflicts with the approved artwork, preserve the artwork's established appearance.

CHARACTER EXTRACTION AND CONSISTENCY
Inspect all three references. Extract the girl's character paths from the SVGs, separating her from background elements and props. Establish a reusable vector character master rather than designing a similar-looking girl from scratch. Do not use a rectangular crop or a raster tracing as the character asset.

Use girl-picking-a-book.svg as the primary reference for her completed pyjamas and girl-brushing-teeth.svg for daytime clothing. Use all three references to understand her identity across poses.

Preserve her dark navy bob ending around the jaw and neck, its distinctive softly scalloped fringe, rounded face, small ear, tiny dark eyes, simple curved nose, and gentle mouth. Keep her peach skin #FFD9C6, existing toddler proportions, head-to-body ratio, short limbs, and rounded bare feet.

Her daytime outfit is a purple T-shirt #AC5BAC and blue trousers #18498F. Her pyjamas are a lavender long-sleeved top and matching trousers #B0AEC9.

Reuse existing vector shapes wherever the pose permits. Redraw only the parts needed for the new action or viewing angle, maintaining the established shapes and proportions. Adapt the head naturally without stretching it or changing the hairstyle. Do not add bows, ponytails, eyelashes, patterns, or new identifying features. Keep her barefoot unless the requested activity specifically involves footwear.

CLOTHING FOR THIS SCENE
{resolved-clothing-description}

SCENE — {activity-title}
{resolved-activity-scene}

DELIVERABLE
One separate editable SVG named girl-{activity-slug}.svg.
```

## Boy prompt template

Use this character block, then insert the resolved activity scene and the complete shared production template.

```text
Create one additional bedtime-routine illustration featuring the EXACT SAME boy shown in the three supplied reference SVGs, performing this activity: {activity}.

This extends an approved collection. It must look like a new pose of the original boy, not a newly designed character. The illustration will be printed approximately 25–30 mm wide.

REFERENCE FILES — REQUIRED
- boy-brushing-teeth.svg
- boy-putting-on-pyjamas.svg
- boy-picking-a-book.svg

Treat the supplied artwork as the source of truth for character identity, proportions, colors, linework, and style. Where a generic written description conflicts with the approved artwork, preserve the artwork's established appearance.

CHARACTER EXTRACTION AND CONSISTENCY
Inspect all three references. Extract the boy's character paths from the SVGs, separating him from background elements and props. Establish a reusable vector character master rather than designing a similar-looking boy from scratch. Do not use a rectangular crop or a raster tracing as the character asset.

Use boy-picking-a-book.svg as the primary reference for his completed pyjamas and boy-brushing-teeth.svg for daytime clothing. Use all three references to understand his identity across poses.

Preserve his short dark navy hair, rounded crown, distinctive side-swept fringe, rounded face, small ear, gently projecting nose, tiny dark eyes, and simple gentle mouth. Keep his peach skin #FFD9C6, existing toddler proportions, head-to-body ratio, short limbs, and rounded bare feet.

His daytime outfit is a coral T-shirt #FF7852 and blue trousers #18498F. His pyjamas are a sage long-sleeved top and matching trousers #BDDC9F. Preserve the sage pyjamas; do not change them to the girl's lavender.

Reuse existing vector shapes wherever the pose permits. Redraw only the parts needed for the new action or viewing angle, maintaining the established shapes and proportions. Adapt the head naturally without stretching it or changing the hairstyle. Do not add spikes, curls, accessories, patterns, or new identifying features. Keep him barefoot unless the requested activity specifically involves footwear.

CLOTHING FOR THIS SCENE
{resolved-clothing-description}

SCENE — {activity-title}
{resolved-activity-scene}

DELIVERABLE
One separate editable SVG named boy-{activity-slug}.svg.
```

## Shared production prompt template

Append this entire block to the selected character template. Resolve its character-specific color variables. Do not include both daytime shirt colors in a single child's prompt.

```text
SVG CONSTRUCTION
Use genuine editable vector paths and shapes, with no embedded raster images, fonts, or external dependencies. Use viewBox="0 0 212 212", matching the references. Keep character and background elements in separate named groups where practical. Leave the remaining canvas transparent; do not add a white background rectangle.

VISUAL STYLE
Match the approved illustrations closely: warm, simple picture-book artwork with softly rounded flat-color shapes, natural gestures, and selective fine navy contours. Match the references' stroke weights, rounded line caps, facial detail, garment hems, and restrained fabric folds. Do not outline every shape. Avoid gradients, shadows, textures, comic styling, exaggerated expressions, and decorative detail absent from the originals.

Keep the child and action dominant. Use only a few broad background shapes, quieter and less detailed than the character. No full room interiors, enclosing frames, labels, lettering, or motion symbols. Leave open space around the hands and important props.

COLOR PALETTE
- Night navy #0B1946 — hair, facial features, selective contours.
- Peach #FFD9C6 — skin; do not substitute sand.
- Night lavender #B0AEC9 — {lavender-role}.
- Night sage #BDDC9F — {sage-role}.
- Night sand #D7C9C2 — furniture, rugs, or soft toys.
- White #FFFFFF — pages, foam, or pillow.
- {day-shirt-color} — daytime T-shirt only.
- Day blue #18498F — daytime trousers only.

Keep the night palette dominant. Use only the colors needed for this scene. Separate adjacent same-color clothing and props with clear silhouettes, composition, or selective navy contours rather than inventing new shades.

COMPOSITION AND FINAL CHECK
Maintain the reference character scale, visual weight, and generous margins. Seated or crouching poses must retain the same anatomical proportions; do not enlarge them merely to fill the square. Keep limbs, feet, and props within the canvas.

Simplify hands to rounded palms and small thumbs where useful. Check continuous limbs, plausible joints, natural grips, and correct front-to-back overlaps. Fingers must not pass through props. Preserve face and hairstyle identity as the viewing angle changes.

Compare the new illustration with all three originals at full size and at approximately 25–30 mm print width. The activity must be recognizable without a caption. Correct any drift in hairstyle, face, skin tone, proportions, clothing, palette, stroke weight, or detail. Check that the requested action is visibly happening rather than merely suggested by a nearby prop.

Match the companion series in activity, prop design, background treatment, and overall illustration style when companion references are supplied, while preserving this child's identity and clothing.
```

Resolve color roles as follows:

| Variable | Girl | Boy |
| --- | --- | --- |
| `{lavender-role}` | pyjamas | secondary props and background accents |
| `{sage-role}` | selected props and background shapes | pyjamas and selected props |
| `{day-shirt-color}` | Day purple #AC5BAC | Day coral #FF7852 |

For completed pyjamas, explicitly state that the top covers the torso and waistband. For a dressing action, replace that statement with the specific transitional garment position. Match expression to the activity while keeping the same minimal facial vocabulary; closed eyes are appropriate for sleeping.

## Completion check

For prompts, verify that the chosen character, all three reference filenames, clothing, palette, activity, and output filename agree; all variables are resolved; and the shared production rules are present. Return only the requested number of scenes, with no unrequested character sheet or collection expansion.

For artwork, additionally verify the actual SVG structure and visually review the rendered output beside the references at the intended small size. Do not claim reference extraction or visual validation unless it was actually performed.
