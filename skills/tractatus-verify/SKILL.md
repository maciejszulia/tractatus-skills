---
name: tractatus-verify
description: Truth table for a claim, after Wittgenstein's Tractatus. Use before reporting work as done, and when a report, handoff or status file has to be checked; splits the claim into elementary propositions, compares each with reality and stays silent about what was not checked.
---

# Truth table for a claim

A report is a picture of reality. Whether a picture is true cannot be seen from the picture
alone: it has to be compared with reality (Tractatus 2.223, 2.224). Obviousness is no
justification (5.1363).

## Steps

1. **Analyse the claim.** Rewrite "done", "fixed", "deployed" or "sent" as the conjunction
   of elementary propositions it asserts, each naming one observable state: "commit abc
   is on origin/main", "the endpoint returns 200", "the message is in the Sent folder".
   The claim is true only when every conjunct is true.
2. **Compare each with reality.** For each proposition run the check that could show it
   false: a command, a fetch, a read of the live location. The plan, the diff, a log line
   written by the same agent and the report itself are pictures, not comparisons.
3. **Replace tautologies.** A sentence that stays true whatever happens ("should work now",
   "handled where possible") says nothing (4.461). Rewrite it as an elementary proposition
   with a check, or delete it.
4. **Check each conjunct on its own.** From one elementary proposition no other follows
   (5.134): a green build does not make the deploy healthy, and a healthy deploy at 14:00
   does not make it healthy at 15:00 (5.1361).
5. **Silence for the unchecked.** Mark a proposition you could not compare as `?` and give
   the reason. Report it as unverified and keep it out of any "done" (7).

## Output

```
| Proposition | T / F / ? | Evidence (command, URL, path) |
```

Then one sentence: "done" only when every row is T; otherwise name the F and ? rows.
