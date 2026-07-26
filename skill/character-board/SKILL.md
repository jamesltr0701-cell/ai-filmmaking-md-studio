---
name: character-board
description: "Generate and directly deliver one minimalist artistic 16:9 character identity board image from an attached character portrait, a character name, and a short introduction. Use when the user asks for a Character Board or character reference board that preserves the reference face and visual style, completes a consistent full body from a cropped portrait, and shows only front, side, back, high-angle, low-angle, expression, and half-body studies."
---

# Character Board

Generate the finished character-board image with the built-in image-generation tool and deliver the image directly. Treat the generation prompt as an internal implementation detail. Do not return prompt text instead of the image unless the user explicitly asks for a prompt-only deliverable.

## Inputs

Use:

1. One attached character reference image.
2. Character name.
3. A short character introduction, role, or personality note.

If the image is missing, ask the user to attach it and stop. Ask for missing text only when it cannot be safely inferred.

If the reference is a local file that is not already visible in the conversation, inspect it with the image-viewing tool before generation. When calling the image-generation tool, include the reference through its supported image-input mechanism. Never omit the reference or substitute a text-only reconstruction of it.

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

Generate exactly one 16:9 board containing only:

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

## Generate and deliver

1. Compose one concise internal image-generation specification from the instructions above. Replace all inferred details before generation; leave no placeholders.
2. Use the built-in image-generation tool with the attached portrait as the strict identity and style reference. Generate one board image by default.
3. Inspect the result for identity consistency, complete bodies, the seven required study groups, minimal text, and an open unboxed layout.
4. If the first result has a material identity, anatomy, cropping, text, or layout failure, make one targeted regeneration that explicitly corrects only those failures.
5. Deliver the successful image inline as the primary response. Keep accompanying text to a brief completion note.

Do not expose the internal prompt, offer prompt alternatives, or begin another filmmaking workflow unless the user asks. If image generation is unavailable or fails after the targeted retry, report the failure clearly; do not replace the requested image with prompt text.

## Internal generation specification

Build the generation request around these constraints:

- Use case: stylized-concept.
- Asset type: minimalist 16:9 character identity board.
- Use the attached reference as the strict identity and style anchor.
- State the source coverage and any inferred lower outfit or footwear.
- Preserve the exact visible identity, costume evidence, visual medium, and palette.
- Request only the seven required study groups.
- Specify the open premium-artbook layout, negative space, and restrained background.
- Include the exact character name and one 8-to-18-word role-and-mood line.
- Repeat the identity-consistency and complete-head-to-feet requirements.
- Repeat all excluded poses, studies, objects, frames, grids, logos, and watermarks.

## Quality gate

Before finishing, verify:

- an image was generated and is the primary deliverable
- the attached reference was passed into image generation
- the board contains only the requested seven study groups
- the large half-body portrait and expression strip are present
- silhouettes, detail studies, and extra poses are absent
- visible text is limited to the name, one short line, and optional tiny view labels
- the layout uses open negative space rather than tiles or boxes
- every required full-body view is complete from head to feet
- full-body completion and reference-style inheritance remain consistent
- no internal prompt or placeholder text is exposed
