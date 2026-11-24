# ADR 0002: Check before and after the work

## Status

Accepted (commit `22839e9`, 2026-11-09).

## Context

The agent delivers some result $x$ that satisfies the words of a request ($x \in P$). The owner wants a result from $C$. A result from $P \setminus C$ fulfils the words and misses the intent. A report of the result can also be false.

## Decision

Split the check into two skills. `tractatus-sense` runs before the work and narrows $P$ with negative conditions and questions. `tractatus-verify` runs before the word "done" and compares each elementary proposition of the claim with the live system.

## Consequences

- Each skill stays short (40 and 36 lines) and has one trigger.
- An agent can load one skill without the other, so a task can be checked only at one end.

## Evidence

- `README.md`, section "Why".
- `skills/tractatus-sense/SKILL.md` and `skills/tractatus-verify/SKILL.md`, `description` fields.
