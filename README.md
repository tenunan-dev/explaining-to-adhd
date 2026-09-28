# Terang / Terangkan

Hermes Agent skills that make an AI assistant explain its work like a teacher, after every coding task — in simple, plain English.

Skills Hermes Agent yang menerangkan kerja dengan gaya guru selepas setiap tugasan pengkodan — dalam Bahasa Inggeris yang mudah.

## Skills

| English | Malay | File | What it does |
|---|---|---|---|
| **terang** (to explain / bright) | **terang** | [`skills/terang/SKILL.md`](skills/terang/SKILL.md) | Adds one short lesson block after each coding task: Problem → Change → Why it works → Proof → Next step → Takeaway. |
| **i-have-adhd** | **saya-ada-adhd** (informal) | [`skills/i-have-adhd/SKILL.md`](skills/i-have-adhd/SKILL.md) | Shapes every reply for a reader with ADHD: lead with the next action, number multi-step work, restate state across turns. |

The two stack: **i-have-adhd** shapes the whole reply, **terang** appends the lesson block at the end.

## How it works (the idea / Idea asas)

A coding answer usually says *what* changed. A reader who is still learning needs *why* it works.
**terang** forces one extra block at the end of the reply, written like a teacher speaking step by step:

1. **Problem** — what was wrong (one sentence)
2. **Change** — the file and what changed in it
3. **Why it works** — the concept, with every technical term defined in place
4. **Proof** — the test or output that confirms it
5. **Next step** — what happens next
6. **Takeaway** — the pattern to remember next time

Language rules are borrowed from ASD-STE100 Simplified Technical English (the controlled
language used in aviation manuals): active voice, common words, one idea per sentence,
sentences of 20 words or fewer, and every piece of jargon defined on first use.
The "if the reader is lost" re-pitch behaviour is borrowed from the
[wait-what skill](https://www.aihero.dev/skills-wait-what) by AI Hero.

## Install (Hermes Agent)

```bash
# Option A: copy into a profile's skills directory
cp -r skills/terang ~/.hermes/profiles/<profile>/skills/productivity/terang
cp -r skills/i-have-adhd ~/.hermes/profiles/<profile>/skills/productivity/i-have-adhd

# Option B: default (no-profile) install
cp -r skills/terang ~/.hermes/skills/productivity/terang
cp -r skills/i-have-adhd ~/.hermes/skills/productivity/i-have-adhd
```

Then start a new session (`/reset`). Turn off the lesson with "no terang";
turn off the reply shaping with "stop adhd mode".

## Maintaining across profiles

Both skills are installed in three places locally. Edit in the coding profile
(`~/.hermes/profiles/coding/skills/productivity/...`), then copy both `SKILL.md`
files to the other locations so they stay identical.

## Provenance

- `wait-what` concept: https://www.aihero.dev/skills-wait-what
- Plain-language discipline: ASD-STE100 (https://github.com/AminBlg/SimpleEnglish)
- Both skill files: MIT licensed.

## Privacy

These are instruction files only — markdown text. No code runs, no network calls,
no telemetry, no credentials, no personal data.
