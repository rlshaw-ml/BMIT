# BMIT compared to nearby public approaches

| Approach | Useful overlap | Where BMIT differs |
| --- | --- | --- |
| General vibe coding | Encourages momentum and direct code writing | BMIT adds explicit altitude control and a fixed test order |
| Ponytail-style / "lazy senior" prompting | Good Inner-level taste: reuse, stay tight, avoid premature DRY | BMIT uses that taste only for local work; it is not the whole framework |
| GitHub Spec Kit | Clear staged delivery and convergence | Spec Kit is spec -> plan -> tasks -> implement; BMIT is write-at-altitude first, then T1 -> T2 -> T3 |
| Red/blue or adversarial testing | Close cousin to T3 | BMIT treats adversarial work as the final test layer, not the entire method |

## Short version

- If you need a **planning framework**, Spec Kit is closer.
- If you need **local implementation taste**, Ponytail-style prompts can help Inner.
- If you need **attacker pressure**, red/blue testing maps to T3.
- If you need a **practical coding loop across structure, subsystem, local code, and staged testing**, use BMIT.
