# ADR 0001: Skills as plain `SKILL.md` text

## Status

Accepted (commit `22839e9`, 2026-11-09).

## Context

The two ideas need to change what the agent does before and after a task. A tool or hook would need code, tests and installation.

## Decision

Each skill is one `SKILL.md` with a front matter, numbered steps with a completion condition, and a fixed output block. The repository holds no code.

## Consequences

- Install is one symbolic link per skill.
- The agent applies a skill only when the `description` matches the task; nothing enforces it.

## Evidence

- `git ls-files`: `README.md`, two `skills/*/SKILL.md`, two `docs/diagrams/*.svg`.
- Commit `22839e9` "Add two Claude Code skills based on the Tractatus".
