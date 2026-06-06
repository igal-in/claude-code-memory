# CLAUDE.md — Project Context for Claude Code

> Read automatically by Claude Code at the start of every session.
> This free version gives you the core session protocol. The full pack
> (JOURNAL.md + KNOWLEDGE.md templates with worked examples) is linked in the
> README.

**Owner:** [YOUR NAME / HANDLE] — [who you are, timezone if it matters].
**Style:** Terse and direct. Skip filler and flattery. Push back when I'm wrong.

---

## Session-start protocol (REQUIRED — do this before anything else)

At the start of every session, before asking what to work on:

1. **Read `docs/JOURNAL.md`** — the most recent entry and any "next steps" block at
   the bottom. The latest entry is the source of truth for where we are.
2. **Read `docs/KNOWLEDGE.md`** — fundamentals, decision log, gotchas. Don't
   re-derive facts that are already written there.
3. **Greet me with a short status summary**: current phase, last action, and the
   exact next step queued from the journal.
4. **Wait for my direction.** Don't auto-run anything that changes files, hits an
   external API, or costs money.

If there's no "next steps" block in the latest entry, ask what I want to work on.

> Don't have `docs/JOURNAL.md` and `docs/KNOWLEDGE.md` yet? They're the other half
> of this system — templates with worked examples are in the full pack (see README).
> Until then, just create both as empty files and the protocol still works.

---

## Session-end protocol (REQUIRED before we stop)

Before the session ends, **append a new entry to `docs/JOURNAL.md`**:

- **What we did** — concise bullets.
- **Pitfalls hit** — time-wasters, so future-us doesn't repeat them.
- **Phase status** — where things stand now.
- **Next steps** — the first 1–2 actions for next time, with exact commands.
- **Commit** — if this is a git repo, commit and push with an accurate message.

If I forget to ask, remind me before we shut down.

---

## Project at a glance

**Goal:** [one or two sentences — what this project is for]
**Current phase:** [e.g. MVP build / debugging X / pre-launch]
**Stack:** [language + version, framework, key services, OS/environment]

---

## Repository structure

```
docs/
├── JOURNAL.md   # session log — READ FIRST
└── KNOWLEDGE.md # fundamentals + decision log — READ SECOND
src/
└── [...]        # your code
```

---

## Working style preferences

- Iterate in small steps — plan, approve, implement a chunk, confirm, continue.
- Quote source (`file:line`), don't paraphrase from memory.
- Flag uncertainty with `UNCLEAR: [reason]`. Don't invent.
- Confirm before anything that hits an external API or costs money.

---

## Hard rules

- **Never commit secrets** (`.env`, `*.key`, plaintext API keys). Verify
  `.gitignore` before any commit.
- Never touch files outside this project directory.
- No running code from untrusted sources without my explicit OK.
- [Add your own project-specific hard rules here.]
