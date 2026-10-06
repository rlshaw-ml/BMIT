# BlastLoop routing card

## Load the right build prompt

- Load [`prompts/blast.md`](./prompts/blast.md) for system-level structure, repo shape, top-level contracts, or broad architectural moves.
- Load [`prompts/mid.md`](./prompts/mid.md) for subsystem work, feature slices, integrations, or module-level refactors.
- Load [`prompts/inner.md`](./prompts/inner.md) for local file edits, unit changes, targeted bug fixes, and small tests.

## Then run the test loop in order

1. [`prompts/t1-structural.md`](./prompts/t1-structural.md)
2. [`prompts/t2-bug-ops.md`](./prompts/t2-bug-ops.md)
3. [`prompts/t3-adversarial.md`](./prompts/t3-adversarial.md)

## Restart rule

If T3 finds a structural problem, do **not** patch around it in place.

Restart like this:

**T3 -> T1 -> route correction to Blast, Mid, or Inner -> T2 -> T3**

## Rule of thumb

**Structure first, function second, attack third.**

See [`docs/HANDOFFS.md`](./docs/HANDOFFS.md) for the required handoff packet and route rules. A stage may recommend a fix, but the owning altitude still decides and implements it.
