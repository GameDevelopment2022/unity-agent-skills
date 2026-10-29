# unity-agent-skills

Reusable Unity workflows for UI and environment design. This public repository is the canonical source for the skills below; individual Unity projects retain their own assets, architecture and project instructions.

| Skill | Rules |
|---|---|
| [Unity UI Agent](skills/unity-ui-agent/SKILL.md) | Reuse matching original sprites/GUIDs; use image generation for genuinely different missing artwork; check adaptability at a compact set of supported sizes and aspect ratios. |
| [Unity Environment Agent](skills/unity-environment-agent/SKILL.md) | Reuse matching textures; distinguish mapping/material issues from different surface artwork; generate genuinely different missing textures. |

Current rule versions: **1.0.1**. See [MANIFEST.json](MANIFEST.json) for exact file hashes and versions.

## Use in a chat

Ask an agent with repository-reading access:

> Read the latest relevant skill and supporting references from https://github.com/GameDevelopment2022/unity-agent-skills. Apply those rules to this task along with the current project's instructions. Report which version you used. Do not assume a previous chat's copy is current.

For installed skills, explicitly select Unity UI Agent or Unity Environment Agent in the host's skill selector. Availability depends on the client and its installed skills/tools; a public URL alone does not install or activate a skill.

## Install in local Codex

Use the skill installer in a client where it is available. Example prompt:

> Use $skill-installer to install the Unity UI Agent skill from https://github.com/GameDevelopment2022/unity-agent-skills/tree/main/skills/unity-ui-agent and the Unity Environment Agent skill from https://github.com/GameDevelopment2022/unity-agent-skills/tree/main/skills/unity-environment-agent as personal skills available across my projects. Inspect existing installations first and preserve intentional local changes.

The source folders include their SKILL.md, optional agents/openai.yaml and any referenced files. Keep each complete folder together. The YAML describes skill presentation; it does not create a separate background agent or a Unity connection.

For product-specific installation behaviour, see [official skill documentation](https://learn.chatgpt.com/docs/build-skills). Repository/project rules do not grant access to Unity, image generation or GitHub; the executing session needs the relevant tools.

## Update from another chat or computer

1. Read this repository's current [AGENTS.md](AGENTS.md), manifest and affected skill files.
2. Make the requested change without replacing newer unrelated edits.
3. Increment the affected rule version, validate the skill and refresh its manifest entries.
4. Publish the change to this repository through authenticated write access.
5. Explicitly update any installed account/client copies from the verified public source. Do not assume automatic two-way synchronization.

Anyone can read these public files. Writing requires an authorized GitHub connection/account. Reading a link in a chat is different from installing a reusable personal skill.

## Implementation handoffs

Keep the full implementation Markdown and short prompt separate from a requested supporting ZIP. Include the current manifest in the ZIP. Include changed relevant rule files/references under `agent-kit/`; include the complete relevant skill on the first handoff or when the previously delivered version is unknown. Record the actual source commit used so a changing `main` branch cannot make an old handoff ambiguous.

## Default UI adaptability sample

For supported landscape projects, fallback samples are 1280×720, 1024×768 and 2400×1080. Portrait equivalents and the complete procedure are in [adaptability.md](skills/unity-ui-agent/references/adaptability.md). Use the actual supported minimum/ratios when they differ. Keep checks brief and Editor-only by default; these samples do not prove every device is covered.

This repository contains reusable instructions and metadata, not game artwork, purchased textures, Unity projects, credentials or Editor verification results.
