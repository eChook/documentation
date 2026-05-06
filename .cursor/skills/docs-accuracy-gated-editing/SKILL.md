---
name: docs-accuracy-gated-editing
description: Edit documentation in strict single-file cycles with zero-assumption behavior. Use when updating docs where accuracy is critical and the user wants a preview, clarification questions for unclear facts, and explicit approval before applying edits.
disable-model-invocation: true
---

# Docs Accuracy Gated Editing

## Purpose
Use this skill for high-accuracy documentation updates where factual drift must be avoided.

## Non-Negotiable Rules
- Work on exactly one documentation file per cycle.
- Do not infer facts that are not explicit in the current docs or user-provided input.
- If any statement is ambiguous, ask a clarification question before editing.
- Show a preview first and wait for explicit approval.
- Apply edits only after approval.

## One-File Cycle
Copy this checklist and keep it updated in each cycle:

```text
Cycle Checklist (single file):
- [ ] 1) Confirm target file path
- [ ] 2) Extract current facts and constraints from file
- [ ] 3) Draft proposed changes (preview only, no edits)
- [ ] 4) List uncertainty questions (if any)
- [ ] 5) Wait for explicit user approval
- [ ] 6) Apply exact approved diff
- [ ] 7) Report what changed and what remains
```

## Required Preview Format
Before any edit, provide:

1. **Target file**
   - Exact path
2. **Intent**
   - Why this file is being changed in this cycle
3. **Proposed edits**
   - Bullet list of concrete edits
4. **Uncertainties**
   - Numbered questions for any fact not 100% clear
5. **Planned diff scope**
   - Sections/headings to touch, and sections explicitly untouched

If uncertainties exist, stop and wait for answers.

## Approval Gate
Only proceed when the user gives explicit approval (examples: "approved", "go ahead", "apply this").

If approval includes constraints, restate them before applying.

## Editing Guardrails
- Preserve existing meaning unless user asks to change it.
- Prefer minimal, reversible edits over broad rewrites.
- Keep terminology consistent with existing docs unless user requests normalization.
- Flag legacy or potentially stale statements; do not silently replace them with guessed modern equivalents.

## Post-Apply Report Format
After applying:
- Files changed (should be one file).
- What changed (short bullets).
- Any deferred items needing user input.
- Suggested next file for the next cycle.

## Out-of-Scope Behavior
- Do not batch multiple files in one cycle.
- Do not run speculative global cleanups.
- Do not introduce new technical claims without source text or explicit user confirmation.
