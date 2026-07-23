# AI Filmmaking MD Studio

A public studio for original, reusable Markdown systems developed by filmmaker **Tairan Li** for AI filmmaking pre-production and visual development.

This repository contains prompt compilers and creative systems—not finished films or case-study media.

## Studio systems

### Character Board

- [`Character Board Skill`](skill/character-board/SKILL.md) — compiles one concise, minimalist 16:9 character-board prompt from an attached portrait, character name, and short introduction.

The current Character Board preserves reference identity and style while limiting the board to front, side, back, high-angle, low-angle, expression, and half-body studies.

### Scenewright

- [`scenewright-v0.1.md`](studio/scenewright-v0.1.md) — an interactive pre-production orchestrator that prepares locked assets, generation units, and Framewright handoff packages.

### Production asset tools

- [`location-card-compiler.md`](studio/location-card-compiler.md) — compiles a production-safe location card prompt.
- [`render-style-bible.md`](studio/render-style-bible.md) — compiles a visual style bible prompt for downstream consistency.

### Visual presentation

- [`storyboard-artifier.md`](studio/storyboard-artifier.md) — transforms a locked production storyboard into an artbook-style presentation prompt.

## Install Character Board in Codex

Ask Codex to install:

> `https://github.com/jamesltr0701-cell/ai-filmmaking-md-studio/tree/main/skill/character-board`

Invoke it with `$character-board`, then attach a character image and provide the character name plus a short introduction.

The Skill returns prompt text only. It does not start image or video generation unless the user separately requests that action.

## Related project

[Framewright](https://github.com/jamesltr0701-cell/framewright) is maintained separately as a versioned system and installable Codex Skill.

## Repository policy

Excluded by design: videos, generated images, case libraries, active projects, private working material, caches, and third-party tools such as Koda.

Copyright © 2026 Tairan Li. All rights reserved. No license for reuse or redistribution is granted unless stated separately.
