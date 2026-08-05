# AI Filmmaking MD Studio

A public studio for original, reusable Markdown systems developed by filmmaker **Tairan Li** for AI filmmaking pre-production and visual development.

This repository contains prompt compilers and creative systems—not finished films or case-study media.

## Studio systems

### Character Board

- [`Character Board Skill`](skill/character-board/SKILL.md) — generates and directly delivers one minimalist 16:9 character-board image from an attached portrait, character name, and short introduction.

The current Character Board preserves reference identity and style, applies restrained exposure and color normalization when technical darkness or contrast obscures important details, and limits the board to front, side, back, high-angle, low-angle, expression, and half-body studies.

### Location Board

- [`Location Board Skill`](skill/location-board/SKILL.md) — generates and directly delivers one 16:9 location board from an attached panorama or wide scene image.

Location Board reconstructs one coherent location through four genuinely separate wide-angle camera stations: high corner, eye-level cross-axis, chest-height long-axis, and low reverse corner. It preserves visible architectural anchors while conservatively inferring unseen areas, and rejects crop, zoom, flip, tilt, or same-position height variations as duplicate views.

### Scenewright

- [`scenewright-v0.1.md`](studio/scenewright-v0.1.md) — an interactive pre-production orchestrator that prepares locked assets, generation units, and Framewright handoff packages.

### Archived legacy prompt compilers

The standalone Location Card and Render Style Bible compilers are retained for recovery and historical reference, but are no longer active studio entry points.

- [`location-card-compiler.md`](studio/archive/location-card-compiler.md)
- [`render-style-bible.md`](studio/archive/render-style-bible.md)

### Visual presentation

- [`storyboard-artifier.md`](studio/storyboard-artifier.md) — transforms a locked production storyboard into an artbook-style presentation prompt.

## Install Character Board in Codex

Ask Codex to install:

> `https://github.com/jamesltr0701-cell/ai-filmmaking-md-studio/tree/main/skill/character-board`

Invoke it with `$character-board`, then attach a character image and provide the character name plus a short introduction.

The Skill uses the attached portrait as its identity and style reference, generates the board image directly, and returns the finished image rather than a prompt. It does not start video generation or another filmmaking workflow unless the user separately requests that action.

## Install Location Board in Codex

Ask Codex to install:

> `https://github.com/jamesltr0701-cell/ai-filmmaking-md-studio/tree/main/skill/location-board`

Invoke it with `$location-board`, then attach one panorama or wide scene image. Optionally provide a short location title or production note.

The Skill generates one four-panel board directly. Its panels must represent separate camera positions within the same location, including high and low viewpoints; simple reframing of a shared camera position does not count as coverage.

## Related project

[Framewright](https://github.com/jamesltr0701-cell/framewright) is maintained separately as a versioned system and installable Codex Skill.

## Repository policy

Excluded by design: videos, generated images, case libraries, active projects, private working material, caches, and third-party tools such as Koda.

Copyright © 2026 Tairan Li. All rights reserved. No license for reuse or redistribution is granted unless stated separately.
