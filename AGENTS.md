# Project Overview

This repository contains a single-file HTML guide:

- [OpenAI Model Options and Intelligence Levels.html](OpenAI%20Model%20Options%20and%20Intelligence%20Levels.html)

The artifact is a truth-first, responsive, interactive model guidance page. RC1 hardening has already been merged into `main`.

# Codex Role

Codex is the implementation and build lane for this repository.

- Codex may perform repository write actions only after explicit approval.
- Gemini is the independent audit and challenge lane.
- The human operator is the final merge authority.

# Authority and Approval Rules

- Prefer read-only checks before write actions.
- Do not edit, commit, push, merge, delete, or install packages unless explicitly approved.
- If instructions conflict, pause and ask for direction.
- If a task is only partially specified, default to audit-only work until approval is clear.

# Repository Safety Rules

- Do not touch unrelated repositories.
- Do not read secrets, API keys, SSH keys, browser profiles, or unrelated personal files.
- Do not run global installs unless explicitly approved.
- Do not run cleanup or destructive commands unless explicitly approved.
- If sandboxing is unavailable, default to audit-only mode and report the limitation.

# File Scope Rules

- Keep changes scoped to the requested files.
- Before staging, committing, pushing, merging, or deleting anything, run `git status --short`.
- Do not include unrelated untracked files in commits.
- Keep documentation commits separate from artifact or HTML commits.

# Single-File HTML Artifact Rules

Preserve the HTML file as a self-contained artifact.

- No external CSS.
- No external JavaScript.
- No external favicon, image, or manifest dependency.
- No frameworks.
- No bundlers.
- No package files unless explicitly approved.
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

- Do not invent OpenAI documentation, pricing, rollout timing, account access, or model availability claims.
- Do not present unsupported claims as facts.

# Runtime Validation Protocol

Prefer localhost testing over direct `file://` testing.

Recommended local server:

```powershell
python -m http.server 8080
```

Do not claim runtime validation occurred unless it actually did.

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

# Git Workflow Rules

- Use branches for changes when appropriate.
- Verify `git status --short` before staging or committing.
- Prefer fast-forward-only merge when appropriate.
- Never include unrelated untracked files in commits.

# Command Safety Rules

- Prefer read-only commands during audits.
- Avoid cleanup/destructive commands unless explicitly approved.
- Avoid broad filesystem searches outside the repository unless needed and approved.
- Avoid commands that can affect unrelated repositories or global state.

# Commit and Push Rules

- Do not commit or push without explicit approval.
- Keep commit scope narrow and intentional.
- Separate documentation-only commits from artifact or code commits.
- Push only after the local review is complete and approved.

# Audit Report Format

When reporting audit results:

- Be specific about what was checked.
- Distinguish confirmed behavior from inference.
- Call out blockers before polish.
- State when runtime validation has not been performed.
- Keep recommendations actionable and scoped.

# Non-Goals

This file is not product marketing copy.

- Avoid hype language such as “perfect,” “brilliant,” “fully optimized,” or “extremely secure.”
- Avoid temporary local process notes that do not belong in durable repository guidance.
- Avoid personal or operational details that are not needed for future Codex sessions.

This file should remain durable repository guidance for future Codex sessions.
