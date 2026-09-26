---
name: council
description: Run the idea council (Believer, then Skeptic, then Investor, then Judge) on an idea and save the verdict to council/ledger.md. Use when the user asks to run the council, get a verdict on an idea, or continue a council session.
---

# Run the council

The council is four subagents defined in `.claude/agents/`: `believer`, `skeptic`, `investor` and `judge`. Its shared memory is `council/ledger.md`. See `council/README.md`.

1. **Read `council/ledger.md` first.** If the idea has been judged before, put the previous verdict, risk and test result in the brief, so the council builds on them instead of starting over.
2. **Write the brief** to `council/sessions/<YYYY-MM-DD>-<slug>/idea.md`: the idea as it currently stands, in the founder's terms, plus what changed since the last verdict and what's still unknown.
3. **Run the roles in order, one at a time, in the foreground.** Paste the inputs into each prompt rather than relying on the agent to find them:
   1. `believer` gets the brief.
   2. `skeptic` gets the brief and the Believer's case.
   3. `investor` gets the brief and both arguments.
   4. `judge` gets the brief and all three arguments, plus the ledger path, the entry format at the top of the ledger, and the session folder's file names.

   Save each role's output verbatim to the session folder as `1-believer.md`, `2-skeptic.md`, `3-investor.md` and `4-judge.md`. Ask the first three roles to mark any figure they didn't verify as an estimate.

   If the role agents aren't available by name (they load when a session starts), run each one as a general-purpose agent with the body of `.claude/agents/<role>.md` pasted at the top of its prompt as its instructions.
4. **Check the Judge's ledger entry** (right place, right format, links work), then commit and push the session.
5. **Report back** with the verdict, the biggest risk and the 10-minute test, and flag any factual error in the arguments.
