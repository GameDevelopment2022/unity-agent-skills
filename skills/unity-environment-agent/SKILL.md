---
name: unity-environment-agent
description: Design, implement, polish, or review Unity environments with existing texture reuse and image generation for genuinely different surfaces. Use for Unity scene art, environment materials/textures, and environment design handoffs; not ordinary UI panels or unrelated gameplay code.
---

# Unity Environment Agent

Rule version: 1.0.1

Canonical source: [GameDevelopment2022/unity-agent-skills](https://github.com/GameDevelopment2022/unity-agent-skills/tree/main/skills/unity-environment-agent).

When asked to change these rules, read the latest canonical files and repository instructions first. Preserve newer edits, increment the rule version, validate the change and update the public source, then explicitly refresh installed personal copies. Do not assume an installed copy or old handoff is current. If the source cannot be read, report that limitation before overwriting it.

Read applicable project instructions, the current environment brief and approved references. Preserve each project's art direction, render pipeline and material/shader conventions; do not carry one project's textures or settings into another project by default.

## Reuse matching textures; generate genuinely different surfaces

1. Inspect the project's existing textures, atlases, terrain layers, material assignments and relevant purchased/imported art before creating an image. Compare actual appearance and intended use, not filenames alone. If the project inventory is unavailable, report that reuse is unverified rather than declaring the texture absent.
2. When an existing texture supplies the same required surface appearance, reuse that original resource and GUID. Reuse its compatible material when appropriate. Do not copy, repaint or regenerate the same stone, wood, ground, wall or other surface for another object or panel merely because its location differs.
3. First distinguish an artwork difference from a mapping/lighting/material issue. Correct supported UV scale, tiling, orientation or material parameters where that accurately matches the reference. Preserve shared consumers: a necessary separate material configuration is not a reason to duplicate its texture, and editing a shared material must not silently change unrelated objects.
4. When the brief/reference requires genuinely different visual content—such as a different grain, motif, stone pattern, damage, color variation baked into the art, or surface identity—and no existing resource supplies it, create that distinct raster texture using the available image-generation skill. Read that skill, inspect the reference inputs and generate only the missing asset. Do not force a visibly wrong existing texture onto a distinct surface to avoid generation.
5. Specify intended use, resolution, seamless tiling when needed, UV/orientation expectations and consistent project art direction. Preserve original resources and name the new asset clearly. Once approved/created, reuse it for later matching surfaces rather than regenerating it.
6. For material workflows, inspect the pipeline's required channels, packing, color-space and import settings. Verify tiling seams, repetition, surface scale and lighting consistency on the actual material. Do not claim that a generated color image is automatically a validated physically based material set. Use suitable existing material-authoring tools for required map conversion/packing and verify the result.
7. If image generation is unavailable, state the specific missing texture/dependency. Do not claim it was generated or substitute unapproved artwork. Keep any existing approval requirements for a new visual identity or major art-direction change.

## Work and evidence

Keep changes within the approved environment scope. Preserve unrelated objects, gameplay, colliders, navigation, saves and working render settings unless the task explicitly calls for changing them. Inspect the actual scene/material assignments with available Unity tools; do not claim a Unity check from a generated proposal alone.

Report the original textures/materials reused, new distinct textures and why they were needed, relevant import/material checks and remaining limitations. Default to a brief affected-scene Editor inspection for an art-only pass, not a build or long gameplay replay unless requested.

When preparing a requested Codex handoff, preserve the user's separate full Markdown, short prompt and supporting ZIP convention. Carry the current version of these rules when changed since the prior handoff, plus a version/hash manifest. Include the complete rules on the first handoff or when the earlier version is unknown. Do not assume a separate local Codex environment has received an account skill update.
