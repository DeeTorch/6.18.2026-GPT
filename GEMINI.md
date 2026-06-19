# Project Scope

This repository contains a single-file HTML guide:

- [OpenAI Model Options and Intelligence Levels.html](OpenAI%20Model%20Options%20and%20Intelligence%20Levels.html)

The artifact is a truth-first, responsive, interactive model guidance page. RC1 hardening has already been merged into `main`.

# Primary Artifact

The main deliverable is the standalone HTML file. Keep the project self-contained and preserve the single-file structure.

Design and content goals:

- Clear model guidance
- Responsive layout
- Truth-first labeling
- Accessible interaction patterns
- No unnecessary external dependencies

# Agent Authority Rules

AI agents are auditors and build assistants, not final merge authority.

- The human operator decides when a change is approved.
- Do not edit, commit, push, merge, delete, or install packages unless explicitly approved.
- If instructions conflict, pause and ask for direction.
- If a task is only partially specified, prefer audit-only work until approval is clear.

# Safety and Sandbox Rules

Default to read-only behavior during audits.

- Do not touch unrelated repositories.
- Do not read secrets, API keys, SSH keys, browser profiles, or unrelated personal files.
- Do not run global installs.
- Do not run cleanup or destructive commands unless explicitly approved.
- If sandboxing is unavailable, stay in audit-only mode and report the limitation.

# Single-File Artifact Rules

Preserve the HTML file as a self-contained artifact.

- No external CSS.
- No external JavaScript.
- No external favicon, image, or manifest dependency.
- No build tools, package files, frameworks, or bundlers unless explicitly approved.
- Inline data-URI favicon usage is acceptable.

# Truth and Source Discipline

Do not imply official verification unless real official sources have been checked.

Use clear labels when a claim is not fully supported:

- `Known`
- `Inferred`
- `Unclear`
- `Pending`
- `Citation Required`
- `Needs Official Source`

Do not invent OpenAI documentation, model availability, pricing, rollout timing, or account-specific behavior.

# Runtime Validation Protocol

Prefer localhost testing over `file://`.

Recommended local server:

```powershell
python -m http.server 8080
```

Do not claim browser validation occurred unless it actually did.

Manual smoke-test items:

- Page loads
- Console has no errors or warnings
- Navigation works
- Wizard works
- Reset works
- Copy buttons work or fail gracefully
- Public/internal mode works
- Mode persists after refresh
- Print preview is usable
- Narrow/mobile layout is usable

# Git Discipline

Use branches for changes when appropriate.

- Verify `git status --short` before and after actions.
- Prefer fast-forward-only merge when appropriate.
- Do not include unrelated untracked files in commits.
- Keep documentation commits separate from artifact or code commits.

# Audit Output Standards

When reporting audit results:

- Be specific about what was checked.
- Distinguish confirmed behavior from inference.
- Call out blockers before polish.
- State when runtime validation has not been performed.
- Keep recommendations actionable and scoped.

# Non-Goals

This file is not product marketing copy.

It is not a place for hype language, personal branding, or temporary local process notes.

Avoid wording such as:

- perfect
- brilliant
- fully optimized
- exceptionally secure
- extremely secure

This file should remain durable repository guidance for future agent sessions.
