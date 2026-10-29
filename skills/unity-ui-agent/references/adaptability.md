# Compact Unity UI adaptability checks

Inspect project-supported orientation, minimum usable viewport, Canvas/UI scaling, safe areas and existing device targets first. Preserve a stricter project matrix or an explicit task override. Do not invent unsupported orientations.

## Default minimum sample

Use three representative aspect/size cases per supported orientation. Reuse the task's existing checks when they cover these cases; avoid duplicate runs.

| Supported orientation | Small baseline | Tablet ratio | Wide/tall phone ratio |
|---|---|---|---|
| Landscape | 1280×720 (16:9) | 1024×768 (4:3) | 2400×1080 (20:9) |
| Portrait | 720×1280 (9:16) | 768×1024 (3:4) | 1080×2400 (9:20) |

These are fallback Editor sample sizes, not universal minimum-device claims. Replace the first case with a smaller supported minimum when the project defines one. Replace the wide/tall case with a more extreme supported ratio when needed. If both orientations are actually supported, cover both with these representative cases. Include desktop/window extremes only when they are supported targets.

At least one case must exercise the smallest usable content area after the project's safe-area and banner reservations. Use the existing safe-area simulator/override if available. Do not change production display settings to manufacture a check.

## Check the affected panel

- Keep the intended Canvas/UI document, references, anchors and layout ownership intact. Save intended scene/prefab changes.
- Check full text ink, joined scripts, long relevant labels/custom names, wrapping and line height. Use each requested active locale; include the longest/tallest relevant case rather than every translation combination without a reason.
- Check fixed actions, touch/hit bounds, controls/icons, selected states and navigation. Decorative graphics must not block interaction.
- Check scroll viewport/mask boundaries, first/last content, reachable endpoints and fixed footers. Enable scrolling only for real overflow; never conceal text by disabling it.
- Check modal fit, expanded/conditional rows, keyboard/input layout when the task includes an editable field, and the supported worst-case content state.
- Check safe areas and the single existing ad reservation where applicable. Keep controls and blockers out of reserved space; do not subtract it twice.
- Correct overflow, overlap, off-screen controls, tiny type and stretched sprites. Recheck the failing case and any directly affected shared consumer; do not restart the whole suite automatically.

Keep a short receipt listing the actual sizes, orientation, locale/state, result and remaining uncertainty. Use a few native captures at meaningful extremes. Do not promise that Editor samples eliminate every future device issue or replace explicitly requested device testing.
