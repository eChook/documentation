# Documentation Style Guide

This guide keeps the eChook documentation consistent, readable, and safe to follow for new teams.

## Core principles

1. Put safety-critical information first.
2. Use clear, direct language.
3. Keep steps in strict order where order matters.
4. Explain why a value or check matters when it is not obvious.

## Writing style

- Use sentence case in headings.
- Keep sentences short where possible.
- Prefer active voice.
- Avoid slang and ambiguous wording.
- Expand acronyms on first use in a page.

## Units, naming, and formatting

- Use `5V`, `12V`, and `24V` (capital `V`).
- Use `mA`, `A`, `kOhm`, and `uF` consistently.
- Use the exact filenames when referencing code files, for example `calibration.h`.
- Use consistent board naming: `V1.x` and `V2+`.

## Step-by-step guidance

- Start procedural pages with prerequisites.
- Add a verification check after critical steps where practical.
- Include expected values for voltage checks where known.
- If there are known failure modes, add a short warning block before the step that can cause them.

## Images and diagrams

- Prefer repository-managed images over externally hosted images for critical content.
- Add a short sentence before each image explaining what to look for.
- Avoid relying on a single image without supporting text.

## Links and structure

- Use relative links for internal docs pages.
- Keep one clear navigation path from setup to telemetry.
- If a page has version-specific instructions, separate them early and clearly.
