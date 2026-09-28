---
name: terang
description: Use after coding tasks to explain the fix like a teacher.
version: 1.1.0
license: MIT
metadata:
  hermes:
    tags: "ADHD, Output Style, Teaching, STE"
    related_skills: ["i-have-adhd", "asd-ste100"]
---

# terang

Stacks on **i-have-adhd**. After a coding task, the reply ends with one short lesson that teaches the concept behind the change, so the next similar problem feels familiar. Name from Malay *terangkan* — to explain. Off switch: "no terang" or "skip the lesson".

## Relationship to i-have-adhd

- i-have-adhd shapes the whole reply. terang adds ONE block at the end. Neither replaces the other.
- The reply lead stays action-first (adhd rule 1). The lesson block goes after the next-action line.
- The adhd recap ban stays. A lesson is not a recap: a recap narrates what you did; a lesson explains why the change works. Start from the problem, never from "I did X".

## When to Use

- Fires: implementation, bug fix, refactor, config change, deployment, migration, review fixes.
- Skips: research-only answers, pure Q&A, small talk, trivial confirmations ("done").
- Scope: chat reply only. Never rewrite a deliverable (doc, code file, report) to fit — same scope rule as i-have-adhd.

## The block

Heading: "What happened, in plain English" (or the user's language). Max 6 numbered items:

1. **Problem** — what was wrong or missing. One sentence.
2. **Change** — `file:line` and what changed there. One sentence.
3. **Why it works** — the concept. This is the teaching line. Define each technical term in place ("X means ..."). Use the project's own names for things; do not invent synonyms.
4. **Proof** — the test, command, or output that confirms it. If already shown above, write "proof above".
5. **Next step** — what happens next: a test to run, a decision needed, or "nothing pending".
6. **Takeaway** — the one-line pattern to remember next time.

Drop an item that carries no information; keep numbering continuous.

## Language rules (STE-flavored)

- Active voice. Common words. One idea per sentence. Sentences of 20 words or fewer.
- No idioms, no marketing words, no hedging filler. Keep a hedge that carries real doubt ("unverified", "I think").
- Define jargon on first use. A technical noun with no definition is a bug in the lesson.
- One analogy allowed, only for abstract concepts. Mark it: "Picture: ...".

## If the reader is lost

On "wait, what" / "lost me" / "explain again": re-pitch the last lesson. Add the premise you skipped first, then simplify. Do not only shorten — shorter-and-blunter fails, shorter-and-clearer works. (Borrowed from aihero's wait-what skill.)

## Check before sending

Read the block as a reader who has never seen the codebase:

- Can they say why the change works, not only what changed?
- Is every technical term defined?
- Is the block free of action narration and repeated results?

Any "no" — rewrite the block.
