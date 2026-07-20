# Character Board

An original Character Board prompt compiler developed by filmmaker **Tairan Li** for AI filmmaking character development.

The repository now contains one focused Codex Skill. It converts an attached character portrait, a character name, and a short character introduction into one polished prompt for an artistic 16:9 character identity board.

## What it prioritizes

- strict face and identity inheritance from the reference image
- exact inheritance of the reference image's visual medium and rendering style
- conservative full-body and outfit completion from cropped portraits
- character-specific pose language derived from the role description
- consistent front, back, profile, seated, leaning, crouching, top-down, and low-angle studies
- clean separation between all figures, portraits, silhouettes, details, and text
- restrained color correction without character redesign
- an asymmetrical, cinematic, premium artbook layout that remains useful for production

## Install in Codex

Ask Codex to install:

> `https://github.com/jamesltr0701-cell/ai-filmmaking-md-studio/tree/main/skill/character-board`

Invoke it with `$character-board`, then attach a character image and provide the character name plus a short introduction.

The Skill returns prompt text only. It does not start image or video generation unless the user separately requests that action.

## Skill source

- [`SKILL.md`](skill/character-board/SKILL.md)

## Repository policy

Excluded by design: videos, generated images, case libraries, active projects, private working material, caches, and third-party tools.

Copyright © 2026 Tairan Li. All rights reserved. No license for reuse or redistribution is granted unless stated separately.
