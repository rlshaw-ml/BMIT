# Handoffs

## Why handoffs exist

In BlastLoop, one layer can know there is a problem without owning the best fix.

Seeing the problem and deciding the fix are different responsibilities. The sender's job is to pass a usable packet. The owning altitude's job is to decide what changes and edit the code at that scope.

A stage may recommend a fix that would work from its own vantage. That recommendation is advisory only. Ultimate responsibility for choosing and implementing the change stays with the owning altitude: **Blast**, **Mid**, or **Inner** when **T1** routes structural work, or **T2** for non-structural bug and ops work.

## Required packet for every handoff

Every handoff must include:

1. **What broke or what changed** - the problem found or the work completed
2. **Where it was observed** - file, module, endpoint, test, runtime path, or review point
3. **Suspected owning altitude** - Blast, Mid, Inner, T1, T2, or T3
4. **Evidence** - failing behavior, code pointer, log, test output, or attack path
5. **What the sender refuses to decide** - the decision that belongs to the next owner
6. **Suggested next owner** - the layer that should take the next action
7. **Optional recommendation** - a possible fix from the sender's vantage, clearly marked as advice and not a decision

If a stage is passing work instead of reporting a failure, say so directly. For a clean pass, write "none found" under "what broke."

## Route map

- **Blast, Mid, and Inner** can hand off among themselves when scope changes or new ownership becomes clear.
- **Build work always goes to T1 first** before T2 or T3.
- **T1** either passes to **T2** or routes correction back to **Blast**, **Mid**, or **Inner**.
- **T2** either fixes the bug or ops issue directly, or escalates to **T1** when the issue is structural.
- **T3** either passes the result or sends a structural issue to **T1** for restart.
- **T3 restart loop:** **T3 -> T1 -> Blast/Mid/Inner correction -> T2 -> T3**
- **Never skip ownership.** If another altitude owns the decision, send the packet there instead of deciding for it.
- **Do not merge or silently apply another layer's fix.** Recommenders can suggest; owners choose and implement.

## Anti-patterns

- quiet local patches for structural issues
- T2 inventing architecture to get a bug green
- Inner redesigning Blast-owned structure
- Mid silently changing a system contract without Blast owning it
- T1 or T3 prescribing detailed implementation for another altitude
- silent assumptions about who owns the next move
- a stage merging or quietly applying another layer's fix because the recommendation seemed obvious
