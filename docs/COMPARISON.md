# BlastLoop compared to nearby public approaches

| Approach | Useful overlap | Where BlastLoop differs |
| --- | --- | --- |
| General vibe coding | Encourages momentum and direct code writing | BlastLoop adds explicit altitude control and a fixed test order |
| Focused local implementation prompts | Tight local execution on bounded changes | BlastLoop routes that work through Inner inside a broader structure-first loop |
| GitHub Spec Kit | Clear staged delivery and convergence | Spec Kit is spec -> plan -> tasks -> implement; BlastLoop is write-at-altitude first, then T1 -> T2 -> T3 |
| Red/blue or adversarial testing | Close cousin to T3 | BlastLoop treats adversarial work as the final test layer, not the entire method |

## Short version

- If you need a **planning framework**, Spec Kit can sit before BlastLoop.
- If you need **direct code-writing momentum**, vibe coding can sit inside an altitude.
- If you need **focused local implementation prompting**, that can sit inside Inner.
- If you need **attacker pressure**, red/blue testing maps to T3.
- If you need a **practical coding loop across structure, subsystem, local code, and staged testing**, use BlastLoop.
