# Maintaining unity-agent-skills

This repository is the canonical public source for the Unity UI Agent and Unity Environment Agent skills. Read the current user request, README.md, MANIFEST.json and affected skill/reference files before editing.

## Scope

- Keep workflows reusable across Unity projects. Read project-specific scene paths, art, UI framework, localization and supported display targets from the project using the skill.
- Preserve the required distinction: reuse matching original assets/GUIDs; generate genuinely different missing raster artwork with the image-generation skill. Do not force an unsuitable existing asset into a different reference.
- Preserve the UI skill's compact adaptability checks. Keep checks proportional, orientation-aware and brief in the Editor by default. Do not promise every device is covered.
- Keep each SKILL.md concise, with only name and description in YAML frontmatter. Keep supporting material in referenced files and metadata in agents/openai.yaml. Do not duplicate full rules in README.md.
- Keep project assets, purchased content, normal user data, credentials and unrelated files out of this repository.

## Changes and validation

- Inspect the latest branch/head before publishing; preserve existing unrelated content and concurrent edits. Do not force-push over another change.
- Increment the Rule version in an affected SKILL.md when its instructions or supporting references change. Keep metadata consistent with the skill.
- Validate frontmatter, referenced paths and metadata. Use the available skill-creator validator for a managed personal-skill update. Run focused behavioural checks when workflow logic changes; report what was actually checked.
- Regenerate SHA-256 hashes and byte counts in MANIFEST.json for every covered changed file. The manifest deliberately excludes itself. Keep its repository URL, paths and skill versions accurate.
- Publish requested edits to this public source, then explicitly refresh installed personal/client copies where that update is authorized and supported. Treat those as separate operations; never claim they update automatically.
- If the canonical source cannot be read or a publication outcome is uncertain, stop the conflicting write and report the limitation rather than replacing unknown newer content.

## Handoffs

When preparing a requested implementation handoff, keep full Markdown and short invocation outside the supporting ZIP. Include the current manifest and changed relevant skill files/references under agent-kit/. Include the complete relevant skill when no previous delivery can be verified. Record the source commit actually used and preserve all project instructions.
