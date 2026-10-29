---
name: unity-ui-agent
description: Design, implement, correct, or review Unity UI panels and prepare UI handoffs with sprite reuse and compact adaptability checks. Use for Unity menus, HUDs, Canvas/prefab UI, or approved panel references; not general environment texturing or unrelated code.
---

# Unity UI Agent

Rule version: 1.0.1

Canonical source: [GameDevelopment2022/unity-agent-skills](https://github.com/GameDevelopment2022/unity-agent-skills/tree/main/skills/unity-ui-agent).

When asked to change these rules, read the latest canonical files and repository instructions first. Preserve newer edits, increment the rule version, validate the change and update the public source, then explicitly refresh installed personal copies. Do not assume an installed copy or old handoff is current. If the source cannot be read, report that limitation before overwriting it.

Read applicable project instructions and the current task/reference. Keep project styling, UI framework, localization renderer and supported orientations project-specific. Preserve unrelated working UI and gameplay.

## Rule 1 — reuse matching sprites; generate genuinely different artwork

1. Inspect existing project sprites, prefabs, atlases, materials and approved shared controls before creating artwork. Compare the actual image/reference and intended role, not filenames alone. If project assets are unavailable, state that reuse could not be verified; do not claim an asset is missing.
2. If the new panel calls for an existing matching sprite, reuse that original asset/reference and GUID. Do not copy the PNG, regenerate the same image, or create a near-duplicate for another panel. Adjust layout, tint or nine-slicing only when that accurately preserves the requested visual result.
3. If the reference requires genuinely different artwork—such as a different silhouette, ornament, pattern, symbol or material appearance—and no existing resource supplies it, create the needed new raster asset using the available image-generation skill. Read that skill and inspect its reference inputs first. Do not force an unsuitable old sprite into a different design merely to avoid creating a new asset.
4. Generate only the distinct missing asset, with the required transparency, dimensions and intended slicing/usage. Preserve originals and name the new asset clearly. Verify the result against its reference and import it appropriately. Reuse this new asset thereafter when it matches another panel.
5. If image generation is unavailable in the executing environment, identify the specific missing asset and dependency; do not substitute unapproved artwork or claim it was generated. Keep existing approval requirements for a new identity/logo.

## Rule 2 — check adaptability before finalizing

Use the compact procedure in [references/adaptability.md](references/adaptability.md). Check the actual panel at the supported minimum size and representative aspect ratios, not only a scaled reference screenshot. Check geometry, text, controls, safe areas and the states most likely to overflow. Fix observed issues and recheck the affected case.

Default to brief Editor-only checks for UI implementation; no build, device run, full game, long suite or exhaustive matrix unless the task calls for it. Prefer anchors/layout and measured text to resolution-specific offsets. Preserve the project's UI system and existing input/navigation semantics.

For uGUI projects that require saved editable Canvas UI, author and save the objects before Play; do not use a runtime builder as a shortcut. For other frameworks, preserve their native authored structure.

For design-only proposals, evaluate the composition at the same representative sizes and reserve flexible text/control regions. Label this as a design review; it does not establish actual Unity adaptability. If Editor access is unavailable, state which implementation checks remain unverified.

## Evidence and reusable handoffs

Report matching assets reused, genuinely different assets created and why, checked resolutions/locales/states, observed failures fixed and remaining limits. A few representative checks reduce common layout failures; they do not prove every device is covered. Never claim a native Editor run from a generated mockup.

When preparing a requested Codex handoff, preserve the user's separate full Markdown, short prompt and supporting ZIP convention. Carry the current version of these rules/references when changed since the prior handoff, plus a version/hash manifest. Include the complete rule set for the first handoff or when the previous version is unknown. Do not assume a separate local Codex environment has received an account skill update.
