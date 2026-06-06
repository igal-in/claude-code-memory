# claude-code-memory
# Claude Code Memory — stop re-explaining your project every session

A tiny, free protocol that gives **Claude Code** session-to-session memory using a
single file it already reads: `CLAUDE.md`. No plugins, no extensions, no
subscription.

> If Claude Code keeps forgetting your project between sessions, this is the fix.

---

## The problem

Claude Code is sharp *inside* a session and amnesiac *between* them. Every time you
reopen it you re-explain your architecture, re-state your preferences, and watch it
cheerfully re-make a mistake you already solved last week. The context you built up
is gone the moment you close the terminal.

## The fix (free, in this repo)

`CLAUDE.md` is read automatically by Claude Code at the start of every session. This
repo gives you a version with a two-part protocol baked in:

- **Session start** — Claude reads your project log, refreshes on the knowledge
  base, and greets you with *"here's where we are, here's the next step"* before
  doing anything.
- **Session end** — Claude writes down what you did, what tripped you up, and the
  exact next action, then commits — so tomorrow's session is productive in under a
  minute.

That's it. The discipline is the product; the file just makes it automatic.

```text
# CLAUDE.md (excerpt)

## Session-start protocol (REQUIRED — do this before anything else)
1. Read docs/JOURNAL.md — the latest entry is where we are.
2. Read docs/KNOWLEDGE.md — fundamentals, decisions, gotchas.
3. Greet me with current phase, last action, next queued step. Then wait.

## Session-end protocol (REQUIRED before we stop)
Append a journal entry: what we did / pitfalls hit / phase status / next steps.
Then commit.
```

Full file: [`CLAUDE.md`](./CLAUDE.md) in this repo. Drop it in your project root and
you're running.

---

## Install (60 seconds)

1. Copy [`CLAUDE.md`](./CLAUDE.md) into the **root** of your project (next to where
   you run `claude`).
2. Fill in the four marked spots (owner, goal, stack, repo map).
3. Start Claude Code. It reads the protocol and asks what to work on.

---

## Want the complete system?

The free file above is the **engine**. The full **Claude Code Memory Kit** gives you
the rest of the system — pre-built, so you're not staring at a blank page:

- **`JOURNAL.md`** template — the session-log format with the "next steps / pickup
  brief" pattern that makes "where were we?" a non-question.
- **`KNOWLEDGE.md`** template — durable facts, a **decision log** that stops settled
  questions from being re-litigated, and a gotchas section.
- **A complete filled-in example project** — the whole system working, end to end.
- **A guide** explaining why each piece is shaped the way it is, so you can adapt it
  to your own workflow instead of following it blindly.

Setup is five minutes, and it only gets more valuable the longer you run it.

### → Get the full kit for $12: https://gosdrop.gumroad.com/l/claude-code-memory-kit

---

## FAQ

**Do I need a paid Claude plan?** No. This is just files; it works with any Claude
Code setup.

**Will it bloat my context window?** `CLAUDE.md` is deliberately short — it's the
only file read in full every session. Keep it lean and it costs very little.

**Non-code projects?** Works for anything you run as a multi-session collaboration —
writing, research, ops.

---

## License

MIT — see [LICENSE](./LICENSE). Use it, fork it, build on it.

---

*Found this useful? A ⭐ helps other people find it.*
