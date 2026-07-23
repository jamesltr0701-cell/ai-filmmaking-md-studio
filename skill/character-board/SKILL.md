---
name: character-board
description: "Compile one concise image-generation prompt for a minimalist artistic 16:9 character identity board from an attached character portrait, a character name, and a short introduction. Use when the user asks for a Character Board or character reference board that preserves the reference face and visual style, completes a consistent full body from a cropped portrait, and shows only front, side, back, high-angle, low-angle, expression, and half-body studies."
---

# Character Board

Create prompt text only. Do not generate an image or begin another filmmaking workflow unless the user separately asks.

## Inputs

Use:

1. One attached character reference image.
2. Character name.
3. A short character introduction, role, or personality note.

If the image is missing, ask the user to attach it and stop. Ask for missing text only when it cannot be safely inferred.

## Lock the reference

Inspect whether the source is full body, partial body, bust, or close portrait.

Preserve:

- face, facial proportions, age impression, skin tone, and distinctive features
- hairstyle and hair silhouette
- all visible costume and accessory evidence
- the source image's actual medium, rendering style, shape language, palette, texture, and finish

If the source is cropped, infer a simple coherent full body, lower outfit, and footwear from visible evidence and the character introduction. Keep the same completion in every view. Never use the role to redesign the visible identity.

Apply only restrained color correction for accidental exposure or white-balance problems. Preserve deliberate colors and style.

## Use the character introduction lightly

Silently compress the introduction into:

- a short role
- one core mood
- one understated posture tendency
- 3 or 4 subtle expression variations
- one brief visible character line

Use this information to guide stance, gaze, expressions, and the inferred outfit. Do not create narrative scenes or additional pose studies.

## Required board content

Request only:

1. one primary front full-body view
2. one side full-body view
3. one back full-body view
4. one complete high-angle top-down full-body view
5. one complete low-angle full-body view
6. one expression study containing 3 or 4 small head-and-shoulders portraits
7. one large half-body portrait

Do not add:

- seated, leaning, crouching, action, or alternate-costume poses
- silhouette studies
- detail studies of eyes, hair, hands, fabric, shoes, or props
- repeated portrait rows
- extra turnaround angles
- decorative objects or environmental fragments

## Minimal editorial layout

Create an open 16:9 composition inspired by a premium animation artbook or fashion character plate.

- Use one clean flat or near-flat background color: soft ivory by default, or one restrained color field derived from the character palette.
- Place the large half-body portrait at one outer edge as the emotional anchor.
- Arrange the front, side, and back full-body views as a calm central lineup.
- Keep the high-angle and low-angle views smaller and nearby.
- Place the expression portraits as one compact strip or vertical column at the opposite edge.
- Separate images with generous negative space rather than boxes.
- Use varied scale and slight asymmetry without making the page busy.

Avoid grids, cards, visible panel borders, contact sheets, technical diagrams, dense annotation systems, collage fragments, paper scraps, and repeated rectangular image tiles.

Do not overlap character images. Keep every face intact and every full-body view complete from head to feet.

## Minimal text

Visible text must never dominate the page.

Include only:

- the character name as one elegant display title
- one short secondary line, 8 to 18 words, combining role and character mood

Optional tiny labels such as `FRONT`, `SIDE`, `BACK`, or `EXPRESSIONS` are allowed only if they improve clarity.

Do not show `NAME:`, `ROLE:`, `CORE MOOD:`, `VISUAL SIGNATURE:`, long biographies, paragraphs, slogans, measurements, or technical notes.

## Identity consistency

Keep the same face, facial proportions, hairstyle, skin tone, outfit, inferred lower-body design, footwear, body proportions, visual medium, and palette across every view.

## Final prompt

Output one English image-generation prompt unless the user asks for another language. Aim for 300 to 450 words and never exceed 500 words. Output the prompt only, with no analysis, alternatives, Markdown fence, or follow-up.

Use this compact structure and replace every placeholder:

Create a minimalist artistic 16:9 CHARACTER IDENTITY BOARD.

Use the attached reference image as the strict identity and style anchor for [NAME], [SHORT CHARACTER INTRODUCTION]. The source is a [SOURCE COVERAGE] image. Preserve the exact visible face, facial proportions, age impression, skin tone, hairstyle, hair silhouette, costume evidence, and distinctive identity markers. If the source is cropped, infer a coherent complete body, [LOWER OUTFIT AND FOOTWEAR], and keep that completion identical in every full-body view. Apply restrained color correction only where needed.

VISUAL STYLE:
Inherit the reference image's [CONCISE STYLE FINGERPRINT] consistently across the whole board. Do not convert it into another medium.

LAYOUT:
Use a clean flat [BACKGROUND TONE] background with no environment. Create an open premium artbook composition with generous negative space, calm asymmetry, and no boxed panels or visible grid.

Include only seven study groups:
1. a primary front full-body view with [SUBTLE CHARACTER-SPECIFIC STANCE];
2. a side full-body view;
3. a back full-body view;
4. a complete high-angle top-down full-body view;
5. a complete low-angle full-body view;
6. one compact expression strip with [3 OR 4 SUBTLE EXPRESSIONS];
7. one large half-body portrait at the outer edge as the emotional anchor.

Keep every image separate. No overlap, no cropped faces, no missing hands or feet, no alternate costume, and no identity drift.

TEXT:
Show only the elegant name `[NAME]` and one small secondary line: `[8-18 WORD ROLE AND MOOD LINE]`. Optional tiny view labels may be used sparingly. No biography, no four-field identity block, and no technical annotations.

Do not include seated, leaning, crouching, action, silhouette, detail, prop, or extra portrait studies. No environment, logo, watermark, collage, contact sheet, decorative frame, or repeated image tiles.

The result should feel minimal, cinematic, character-focused, quietly art-directed, and useful as a clean identity reference.

## Quality gate

Before responding, verify:

- the final prompt contains only the requested seven study groups
- the large half-body portrait and expression strip are present
- silhouettes, detail studies, and extra poses are absent
- visible text is limited to the name and one short line
- the layout uses open negative space rather than tiles or boxes
- full-body completion and reference-style inheritance remain explicit
- the prompt is no longer than 500 words
- no placeholders remain
