---
name: character-board
description: "Compile one polished image-generation prompt for an artistic 16:9 character identity board from an attached character portrait, a character name, and a short character description. Use when the user asks for a Character Board, Character Identity Board, character reference board, or a prompt that must extend a full-body identity from a full-body, half-body, bust, or portrait reference while strictly preserving the reference face, rendering medium, and visual style."
---

# Character Board

Create prompt text only. Do not generate an image, invoke an image or video tool, edit media, or start another filmmaking workflow unless the user separately asks for that action.

## Required inputs

Use these inputs:

1. One attached character reference image.
2. Character name.
3. A short character introduction, role, personality, or story function.

Accept optional outfit, mood, posture, age-impression, or production notes.

If the reference image is missing, ask the user to attach it and stop. If the name or introduction is missing and cannot be safely inferred, ask only for the missing information. Do not invent a different identity.

## Inspect the reference

Classify the visible coverage as one of:

- full body
- three-quarter body
- half body
- bust
- head-and-shoulders portrait
- close-up portrait

Extract two separate locks.

### Identity lock

Record the visible identity evidence:

- face shape and facial proportions
- eye shape, spacing, and gaze character
- nose, mouth, jaw, cheeks, and age impression
- skin tone and distinctive facial details
- hairstyle, hairline, volume, texture, and silhouette
- visible body proportions
- visible outfit, accessories, and hand behavior

Never use the role description to redesign the face, ethnicity, age, hairstyle, or other visible identity evidence.

### Style lock

Describe the reference image's actual visual medium and rendering language, including:

- medium, such as stylized 3D, photorealistic photography, hand-painted animation, anime, stop-motion, clay, ink, or another visible medium
- facial stylization and shape language
- linework or edge treatment
- materials, shading, and surface finish
- color palette and saturation
- contrast and lighting softness
- texture and detail density

Use the reference style as the authoritative visual medium for every character study. Do not default to stylized 3D unless the reference is visibly stylized 3D or the user explicitly requests a style transformation.

If the user explicitly requests a new medium, preserve the reference identity but use the requested medium consistently across the board.

## Complete the unseen full body

The board must contain complete full-body studies even when the source is cropped.

When the lower body, footwear, hands, or parts of the outfit are not visible:

- preserve all visible costume evidence exactly
- extend the visible garment logic into a coherent complete outfit
- infer plausible body proportions from the face, visible torso, age impression, and character description
- infer lower garments and footwear that support the role without turning the character into a stereotype
- keep the completion visually simple when evidence is weak
- keep the same completed outfit and proportions in every view
- never imply that an inferred detail was visible in the source

Prioritize, in order:

1. face and identity fidelity
2. reference visual-medium and style fidelity
3. coherent full-body completion
4. character-specific posture and performance
5. artistic page design

## Apply restrained color correction

Correct accidental exposure, white-balance, tint, or contrast problems in the reference while preserving deliberate palette choices, skin tone, material colors, and the source's artistic character.

Keep the corrected palette identical across every view. Do not use color correction as permission to redesign the character.

## Compress the character

Silently derive:

- `NAME`: the user-provided name
- `ROLE`: a short narrative function
- `CORE MOOD`: 3 to 8 words describing emotional temperature
- `VISUAL SIGNATURE`: concise visible identity markers, prioritizing face, hair, outfit silhouette, body shape, and posture
- `POSE LANGUAGE`: weight distribution, spine attitude, shoulder tension, hand behavior, gaze, and movement energy suited to the character introduction

Use the character introduction wherever it improves expressions, posture, outfit completion, and annotations. Keep the face and reference style independent from invented story details.

## Develop one coherent pose-study direction

Translate `POSE LANGUAGE` into a consistent performance concept for the whole board. Apply it to:

- neutral full-body view
- back view
- profile view
- seated pose
- leaning pose
- crouching pose
- top-down full-body angle
- low-angle full-body angle

Make each pose character-specific rather than generic. Keep each one an isolated studio study, never a scene. Do not add a setting. Avoid props unless one is essential to the character introduction.

## Preserve strict layout safety

Every character image must remain separate.

- no overlap between character images
- no merged or intersecting bodies
- no stacked figures
- no hidden faces
- no face cut off by a frame or page edge
- no cropped hero, body-view, or pose-study limbs
- no hands or feet lost outside the page
- no text on faces, hair, bodies, clothing, hands, or detail studies
- no image used as a background behind another image

Portrait studies may use a head-and-shoulders composition, but the entire face, hair silhouette, and chin must remain visible.

If the requested content risks crowding, reduce decorative marks and scale down supporting studies. Never solve crowding by overlapping or cropping character images.

## Build the board content

Always request:

- one large off-center hero full-body view as the visual anchor
- one neutral full-body view
- one back full-body view
- one profile full-body view
- seated, leaning, and crouching pose studies driven by the same pose language
- one top-down full-body angle
- one low-angle full-body angle
- 4 subtle, character-specific expression portraits
- 2 to 3 simplified black silhouettes
- 3 to 6 detail studies covering the most useful face, hair, outfit, hand, or footwear features
- one minimal `CHARACTER ID` block

Require strict identity consistency across every study: same face, facial proportions, eye shape, hairstyle, hair silhouette, skin tone, outfit, completed lower-body design, footwear, body proportions, posture language, visual personality, visual medium, rendering language, and corrected palette.

## Write the final prompt

Output one complete image-generation prompt in English unless the user requests another language. Output the prompt only, without analysis, preamble, alternatives, Markdown fences, or follow-up suggestions.

Use the structure and wording below. Replace every placeholder with concrete compiled information. Do not leave brackets or placeholder labels in the final prompt.

Create an artistic 16:9 CHARACTER IDENTITY BOARD.

SUBJECT: use the attached reference image as the strict identity anchor. Name: [NAME]. Preserve the visible face, facial proportions, age impression, skin tone, hairstyle, hair silhouette, and distinctive identity markers. The source is a [SOURCE COVERAGE] reference; reconstruct a coherent complete full body wherever the source is cropped, extending the visible outfit into [COMPLETED OUTFIT AND FOOTWEAR] while preserving every visible costume detail. Apply restrained color correction: [COLOR-CORRECTION DIRECTION].

CHARACTER DIRECTION: [ROLE]. [CORE MOOD]. [CLEANED CHARACTER INTRODUCTION].

VISUAL MEDIUM: [REFERENCE-DERIVED OR EXPLICITLY REQUESTED MEDIUM AND STYLE FINGERPRINT]. Inherit this visual medium, rendering language, facial stylization, materials, shading, texture, palette, and detail density consistently across every view.

Pure white / soft off-white background.
No environment, no logo, no watermark.

DESIGN DIRECTION:
Do not create a standard character reference sheet.
Create a cinematic identity board that feels like a high-end animation studio character study mixed with an artbook layout.

The layout should be asymmetrical, elegant and visually memorable.
Use large empty space, varied image scale and intentional imbalance.
Avoid grids, blueprint design, catalog layout and repetitive turnaround presentation.

IMPORTANT LAYOUT RULE:
Do not overlap any character images.
Every view must have clear separation and breathing room.
Keep all bodies, portraits, silhouettes and detail studies visually distinct.
No cropped faces, no hidden limbs, no stacked figures, no merged poses.
Keep every full-body study complete from head to feet, with readable hands and footwear.
If space becomes tight, reduce decorative elements and supporting-study scale rather than overlapping or cropping the character.

MAIN COMPOSITION:
Place one large hero full-body view slightly off-center as the visual anchor. Use [HERO POSE DIRECTION].

Around it, arrange smaller supporting studies with clean spacing:
neutral full-body view,
back view,
profile view,
seated pose [SEATED DIRECTION],
leaning pose [LEANING DIRECTION],
crouching pose [CROUCHING DIRECTION],
top-down full-body angle [TOP-DOWN DIRECTION],
low-angle full-body angle [LOW-ANGLE DIRECTION],
expressive portrait studies.

Each view should feel like a separate clean character study, not a frame from one scene.

FULL-BODY COMPLETION:
The reference may not show the complete body. Infer the unseen anatomy, lower garments, hands and footwear conservatively from the visible character design and role. Preserve all visible evidence exactly. Use the same completed body proportions, outfit construction and footwear in every study. Do not create alternate costumes or alternate body types.

POSE LANGUAGE:
[POSE LANGUAGE]. Make every pose express this same character-specific physical personality through weight distribution, shoulders, spine, hands, chin, gaze and movement energy.

IDENTITY LOCK:
Preserve strict identity consistency across all views:
same face,
same facial proportions,
same eye shape,
same skin tone,
same hairstyle,
same hair silhouette,
same outfit,
same completed lower-body design and footwear,
same body proportions,
same posture language,
same visual personality,
same visual medium,
same corrected color palette.

USEFUL REFERENCE DETAILS:
Make the character readable for future image and video generation:
clear face shape,
clear hair silhouette,
clear outfit silhouette,
clear body shape,
clear hands,
clear footwear,
clear posture,
clear expression range.

ARTISTIC SECTIONS:
Include a small silhouette study area with 2-3 simplified black character silhouettes showing the recognizable hair, body, outfit and posture shapes.
Include a small expression study area with these four subtle emotional variations: [EXPRESSION 1], [EXPRESSION 2], [EXPRESSION 3], [EXPRESSION 4]. Preserve the exact same face in every portrait.
Include a small detail study area showing [3-6 KEY VISUAL DETAILS] from the face, hair, outfit, hands and footwear.

TEXT DESIGN:
Add one stylish CHARACTER ID block.
Keep it minimal, bold and art-directed.
Use only:
NAME: [NAME]
ROLE: [ROLE]
CORE MOOD: [CORE MOOD]
VISUAL SIGNATURE: [VISUAL SIGNATURE]

Use small handwritten-style labels only where helpful.
Subtle editorial arrows and annotation marks are allowed, but keep them minimal and elegant.
Keep all text in reserved negative space and away from every character image.

STYLE:
minimal,
cinematic,
premium,
artbook-like,
clean,
expressive,
useful for production.

The final image should feel like an artistic character identity board designed to help an AI model understand the character's face, silhouette, completed outfit, body proportions, posture and emotional range.

## Quality gate

Before responding, silently verify that the final prompt:

- names the source coverage and explains full-body completion
- makes face and style inheritance higher priority than invention
- describes the actual reference medium or an explicit requested override
- includes restrained color correction
- gives a character-specific pose direction
- includes every required body view, artistic section, and identity field
- forbids overlap, cropped faces, hidden limbs, stacked figures, and merged poses
- contains no environment, logo, or watermark
- contains no unresolved placeholders
- asks for one image-generation prompt and nothing else
