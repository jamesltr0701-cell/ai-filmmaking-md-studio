---
name: ai-filmmaking-md-studio
description: "Explicit gateway to Tairan Li's original AI filmmaking Markdown tools: Scenewright, Production Character Board, Location Card, Render Style Bible, Artistic Character Board, and Storyboard Artifier. Use only when the user explicitly invokes this skill or names one of these studio tools and asks to apply it."
---

# AI Filmmaking MD Studio

Apply one selected Markdown system without starting media production.

## Select the tool

If the user has not named a tool, present this short list and ask them to choose:

1. Scenewright
2. Production Character Board
3. Location Card
4. Render Style Bible
5. Artistic Character Board
6. Storyboard Artifier

Do not silently select or combine tools.

## Load the authoritative reference

After selection, read the matching file completely:

- Scenewright: `references/scenewright-v0.1.md`
- Production Character Board: `references/character-board-production.md`
- Location Card: `references/location-card-compiler.md`
- Render Style Bible: `references/render-style-bible.md`
- Artistic Character Board: `references/artistic-character-board.md`
- Storyboard Artifier: `references/storyboard-artifier.md`

Before producing output, state `Loaded: <tool name> <declared version>` using YAML metadata or the title. If the source has no declared version, state `Loaded: <tool name> — version not declared`.

Follow the selected reference as the authoritative contract. Do not substitute remembered instructions.

## Tool boundary

Default to prompt text or planning output only. Do not invoke Framewright, ChatCut, OpenMontage, image generation, video generation, file mutation, or another studio tool unless the user explicitly asks for that additional action.

When the user asks only for a prompt, return the prompt and stop.
