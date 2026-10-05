---
description: "Prepare Pull Request with comprehensive title and description covering the full session"
allowed-tools: "Bash(git:*), Read, Glob"
---

# Prepare Pull Request Materials

Prepare a comprehensive PR title and description. **DO NOT create the PR automatically** — present materials for user approval first.

## Process

1. **Review the full conversation** to understand everything discussed, decided, and changed during this session. The PR description must serve as a historical record — not just a list of file diffs.

2. **Gather git context:**
   - First, fetch the base branch to ensure the remote-tracking ref is up to date: `git fetch origin main` (or appropriate base branch)
   - Then run these commands in parallel:
     - `git diff origin/main...HEAD` (or appropriate base branch)
     - `git log --oneline origin/main..HEAD`

3. **Draft PR title:**

   ```
   <Type>: <Concise description>
   ```

   - Types: Feature, Fix, Refactor, Docs, Test, Style
   - Under 80 characters
   - Specific enough to understand what changed

4. **Draft PR description** using this template:

   ```
   ## Summary

   [2-4 sentence overview: what changed, why, and any key decisions made]

   ## Context

   [Important points from the conversation not obvious from the diff — motivation, rejected approaches, follow-up ideas, etc.]

   ## Changes

   - [Change 1]
   - [Change 2]
   - [Change 3]
   ```

5. **Present materials to the user in two separate fenced code blocks** — one for the title, one for the description body. This is critical for easy copy-pasting on mobile/web.

   Example output format:

   ````
   **PR Title:**

   ```
   Feature: Add widget caching to dashboard
   ```

   **PR Description:**

   ```
   ## Summary
   ...
   ```
   ````

6. **After user approves**, check the environment:
   - If running in a **CLI terminal** (not mobile/web), offer to create the PR directly via `gh pr create`.
   - If on **web/mobile**, the user will copy-paste — do not attempt to run `gh`.

## Key Rules

- **Cover the ENTIRE conversation**, not just the latest commit or diff. The description is a historical record of the session.
- **ALWAYS** output title and description in **separate fenced code blocks** for easy copy-pasting.
- **ALWAYS** analyze ALL commits on the branch, not just the most recent one.
- **NEVER** create the PR without explicit user approval.
- **NEVER** use any auto-create PR functionality.
