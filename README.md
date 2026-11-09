# tractatus-skills

Two Claude Code skills built on Ludwig Wittgenstein's *Tractatus Logico-Philosophicus*
(1921). They turn two of its ideas into working steps for an AI agent:

| Skill | Idea from the Tractatus | What the agent does |
|---|---|---|
| [`tractatus-sense`](skills/tractatus-sense/SKILL.md) | To understand a proposition is to know what is the case if it is true (4.024). | Before acting, writes the request's truth-conditions and the results the words allow but the owner would reject. |
| [`tractatus-verify`](skills/tractatus-verify/SKILL.md) | A picture's truth cannot be seen from the picture alone; compare it with reality (2.223–2.224). Whereof one cannot speak, thereof one must be silent (7). | Before saying "done", splits the claim into elementary propositions, checks each against the live system and marks the unchecked ones as unverified. |

## Why

What a person asks an AI for contains both what they want and what they do not want.
If P is the set of results that satisfy the request and C the set the person wants, the
agent delivers some x ∈ P, and the request is safe only when P ⊆ C. `tractatus-sense`
narrows P before the work; `tractatus-verify` checks the result after it.

## Install

```sh
git clone https://github.com/maciejszulia/tractatus-skills.git
ln -s "$PWD/tractatus-skills/skills/tractatus-sense"  ~/.claude/skills/
ln -s "$PWD/tractatus-skills/skills/tractatus-verify" ~/.claude/skills/
```

Claude Code picks them up from `~/.claude/skills` in the next session.

## Source

Proposition numbers refer to the C. K. Ogden translation (1922), public domain,
[Project Gutenberg #5740](https://www.gutenberg.org/ebooks/5740).

---

**PL:** Dwa skille dla Claude Code oparte na „Traktacie logiczno-filozoficznym”.
`tractatus-sense` przed pracą zapisuje warunki prawdziwości prośby i wyniki, których
właściciel by nie chciał. `tractatus-verify` przed słowem „gotowe” rozbija twierdzenie na
zdania elementarne, każde sprawdza z rzeczywistością, a niesprawdzone oznacza jako
niezweryfikowane.
