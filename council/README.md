# The council

Four agents that review an idea from four fixed angles, in a fixed order, and leave a verdict behind so the next session continues where the last one stopped.

| # | Role | Job | Definition |
|---|---|---|---|
| 1 | Believer | Makes the strongest honest case for the idea | [`believer.md`](../.claude/agents/believer.md) |
| 2 | Skeptic | Tries to kill it | [`skeptic.md`](../.claude/agents/skeptic.md) |
| 3 | Investor | Checks whether real money shows up, and how fast | [`investor.md`](../.claude/agents/investor.md) |
| 4 | Judge | Rules BUILD, FIX FIRST or KILL, and saves the verdict to the ledger | [`judge.md`](../.claude/agents/judge.md) |

Each role sees the idea plus every argument before it: the Skeptic reads the Believer, the Investor reads both, and the Judge reads all three.

## Files

- [`ledger.md`](ledger.md): **the shared note.** Every idea the council has reviewed and every verdict, newest first. Read it before starting a session.
- `sessions/<date>-<slug>/`: one folder per session, holding the idea brief (`idea.md`) and each role's full argument (`1-believer.md` … `4-judge.md`).

## Running it

Ask Claude to "run the council" on an idea, or type `/council`. The step-by-step procedure is in [`.claude/skills/council/SKILL.md`](../.claude/skills/council/SKILL.md).

Claude Code loads the role definitions from `.claude/agents/`, so any session can call them by name (`believer`, `skeptic`, `investor`, `judge`).
