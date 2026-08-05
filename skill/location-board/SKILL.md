---
name: location-board
description: "Generate and directly deliver one 16:9 location board from an attached single scene panorama or wide location image. Use when the user asks for a Location Board, location panel, environment reference board, or four complementary wide-angle views that preserve one location's architecture while using four truly distinct camera stations, including high-angle and low-angle views."
---

# Location Board

Generate the finished location-board image with the built-in image-generation tool and deliver the image directly. Treat the generation prompt as an internal implementation detail. Do not return prompt text instead of the image unless the user explicitly asks for a prompt-only deliverable.

## Inputs

Use:

1. One attached panorama or wide scene image that shows the location's principal layout.
2. An optional short location title or production note.

If the image is missing, ask the user to attach it and stop. If the input is already a multi-panel board, a close-up, or too cropped to establish the location, ask for one actual wide scene image or additional references instead of treating it as a reliable panorama.

Use the title if supplied. Otherwise, infer a short neutral location title only when the image makes one clear; use `LOCATION BOARD` if it does not.

## Lock the location

Inspect the source before generation. Silently identify the visible spatial anchors: room shape, entry and exit points, doors, windows, fixed furniture or equipment, primary walls, central objects, material palette, light sources, and the relationship between them.

Preserve all visible architectural evidence across every panel:

- the same room geometry, ceiling height, doors, windows, fixed fixtures, main furniture, materials, weathering, lighting direction, and time-of-day impression
- the same scale and placement of recognizable anchor objects
- the source image's visual medium, palette, texture, contrast, and finish

Infer unseen areas conservatively. Extend only what is necessary to create a coherent connected location. Do not add a major room, doorway, window, facility, furniture system, or new visual style that contradicts the visible evidence.

The result is a visual-development reconstruction, not a measured survey. Never imply that unseen areas were literally present in the source.

## Plan four genuinely separate cameras

Before generating, divide the implied accessible floor plan into four spatially separated perimeter zones. Place exactly one camera station in each zone. For an ordinary rectangular room, use four different corner, threshold, or wall-edge areas; for irregular locations, maximize separation rather than forcing literal corners.

Use this four-panel plan:

1. **High corner overview** — a high oblique camera, roughly 2.3–2.8 m high, looking diagonally through the location. Show broad floor layout and circulation. Do not make a vertical top-down plan.
2. **Eye-level cross-axis view** — a normal-height camera, roughly 1.5–1.7 m high, from a second zone looking across the location. Feature a functional wall or spatial width not dominant in panel 1.
3. **Chest-height long-axis view** — a slightly lowered camera, roughly 1.0–1.2 m high, from a third zone looking along the location's depth. Feature entry, exit, or depth relationships not primary in panels 1 or 2.
4. **Low reverse-corner view** — a low oblique camera, roughly 0.4–0.7 m high, from the remaining zone looking in a reverse diagonal direction. Reveal ceiling height and areas hidden by the other views. Do not make an extreme floor-level shot.

Keep every panel a wide establishing view. Use a consistent restrained wide-angle perspective; do not use fisheye distortion, detail shots, object close-ups, portraits, or a single hero object that overwhelms the location.

## Enforce camera uniqueness

Treat a different crop, zoom, focal length, roll, tilt, or vertical move at the same floor-plan point as the **same camera station**. It does not count as a new panel.

Reject and regenerate any pair of panels that could plausibly be created from one another by cropping, zooming, flipping, or merely looking up or down. Require every pair to differ in all of the following ways:

- camera origin belongs to a different floor-plan zone
- primary view axis or primary wall/area differs
- foreground edge anchor differs, such as a different door jamb, counter edge, shelving edge, or structural corner
- fixed objects show different parallax or occlusion relationships, proving that the camera moved through the space

High-angle and low-angle panels must not be vertically stacked at the same plan position. The board must read as four separate visits to one location, not four variations from one tripod.

## Board layout and text

Generate exactly one 16:9 board with four equally important landscape panels in a clean 2×2 grid. Use narrow dark dividers and a restrained presentation inspired by a professional location scout or production-design panel.

Include only:

- one small location-board title
- one short view label under each panel, beginning with `01`, `02`, `03`, or `04`

Use labels that describe the planned camera role, such as `01 HIGH CORNER — ENTRY VIEW`. Keep visible text minimal and secondary to the images.

Do not add color palettes, mood paragraphs, long annotations, maps, floor plans, technical diagrams, extra thumbnails, decorative collage fragments, logos, watermarks, or any fifth image.

## Generate and deliver

1. Compose one concise internal image-generation specification from the source evidence and the four-camera plan. Resolve inferred details before generation; leave no placeholders.
2. Use the attached location image as the strict architectural, material, lighting, and style reference. Generate one 16:9 board image by default.
3. Inspect the result for four distinct stations, high/eye/chest/low camera heights, broad coverage, parallax, architectural continuity, wide framing, and minimal readable labels.
4. If the first result has a material failure—repeated station, false zoom variation, missing high or low view, close-up, spatial contradiction, cropped panel, or excessive/incorrect text—make one targeted regeneration that corrects only those failures.
5. Deliver the successful board image inline as the primary response. Keep accompanying text to a brief completion note.

Do not expose the internal prompt, offer prompt alternatives, begin video generation, or start another filmmaking workflow unless the user asks. If image generation is unavailable or fails after the targeted retry, report the failure clearly; do not replace the requested image with prompt text.

## Internal generation specification

Build the generation request around these constraints:

- Asset type: a single 16:9 four-panel cinematic location board.
- Input image: strict architectural, material, lighting, and visual-style reference for one connected location.
- Reconstruction policy: preserve visible anchors exactly; infer unseen areas minimally and coherently.
- Camera plan: four separate perimeter zones, with high oblique, eye-level cross-axis, chest-height long-axis, and low reverse-corner views.
- Wide framing: every panel is a broad establishing view with restrained wide-angle perspective and no fisheye distortion.
- Uniqueness: no shared camera origin; no crop, zoom, flip, tilt, or vertical-only variation; visible parallax and changed occlusion must demonstrate physical camera movement.
- Continuity: doors, windows, fixed equipment, furniture, surfaces, scale, light direction, palette, and time-of-day remain coherent across all panels.
- Layout: exactly four equal 2×2 landscape panels, narrow dividers, one small title, and four short numbered labels.
- Avoid: people or characters unless integral to the source, close-ups, detail panels, extra images, maps, floor plans, palettes, dense text, logos, watermarks, and unrelated scenery.

## Quality gate

Before finishing, verify:

- an image was generated and is the primary deliverable
- the attached scene image was passed into image generation
- the board contains exactly four wide location views
- panels 1 through 4 use high, eye, chest, and low heights respectively
- all four camera origins occupy separate spatial zones; high and low views are not stacked at one point
- every pair shows a distinct axis, foreground edge anchor, and parallax or occlusion relationship
- no panel is a crop, zoom, flip, tilt, or proximity variant of another
- visible architecture, fixed anchors, materials, lighting, scale, and style remain coherent
- no close-up, fisheye, extra panel, unrelated character, decorative collage, or dense annotation system appears
- text is limited to one title and four short numbered labels, with no material text error
- no internal prompt or placeholder text is exposed
