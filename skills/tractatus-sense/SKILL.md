---
name: tractatus-sense
description: Truth-conditions of a request, after Wittgenstein's Tractatus. Use before acting on a vague, broad or high-stakes request, or when the owner asks what is actually wanted ("doprecyzuj", "czego właściwie chcę"); states what must be the case when the request is fulfilled and which fulfilments the owner would reject.
---

# Sense of a request

A request has sense when you know what is the case if it is fulfilled (Tractatus 4.024).
Fulfilling the words is not fulfilling the intent. Let P be the set of results that satisfy
the words and C the set the owner wants; you will deliver some x ∈ P. The work is safe
only when P ⊆ C, that is when P \ C = ∅.

## Steps

1. **Write the truth-conditions.** List the elementary propositions that must all be true
   when the request is done. Each one is observable and independent of the others
   (4.21, 2.061): "the app works" is a complex, "`npm test` exits 0 on main" is elementary.
   Done when every line can be answered yes or no by looking.
2. **Split the signs.** Mark every word that signifies in two ways (3.323): "send",
   "remove", "publish", "done", a name that matches two things. Settle each meaning from
   the repository, memory or the owner's earlier messages; a word that stays open goes
   to step 4.
3. **Find P \ C.** List the results that satisfy the truth-conditions and that the owner
   would still reject: the cheap literal reading, the destructive shortcut, the right
   change in the wrong place, the extra scope. Turn each into a negative condition
   ("and nothing outside X changes"). Done when the literal, the destructive and the
   overreaching readings have each been tried.
4. **Narrow or ask.** Add every negative condition to the plan. Ask the owner only about
   what steps 2 and 3 could not settle: one question per open sign, each with a proposed
   default.

## Output

Before the work starts, a block sized to the task (a one-line request gets one line):

```
Truth-conditions: 1. … 2. …
Excluded (P \ C): …
Open: … (proposed default: …)
```
