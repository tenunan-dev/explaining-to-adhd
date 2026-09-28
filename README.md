# Explaining to ADHD / Menerangkan Kepada ADHD

Hermes Agent skill that shapes every reply for a reader with ADHD — and after every coding task, ends the reply with one short teacher-style lesson in simple, plain English.

Kemahiran Hermes yang membentuk setiap balasan untuk pembaca ADHD — dan selepas setiap tugasan pengkodan, menutup balasan dengan satu pelajaran ringkas bergaya guru dalam Bahasa Inggeris yang mudah.

## The skill

| English | Malay | File | What it does |
|---|---|---|---|
| **explaining-to-adhd** | **menerangkan-kepada-adhd** | [`skills/explaining-to-adhd/SKILL.md`](skills/explaining-to-adhd/SKILL.md) | One skill, two jobs: shapes every reply (lead with the next action, number multi-step work, restate state across turns, cap lists to 5, no preamble/recap/closers) **and** appends a lesson block after each coding task: Problem → Change → Why it works → Proof → Next step → Takeaway. |

Off switches: "stop adhd mode" turns off the whole skill; "no terang" turns off only the lesson block.

## How it works (the idea / Idea asas)

A coding answer usually says *what* changed. A reader who is still learning needs *why* it works.
The lesson block forces one extra section at the end of the reply, written like a teacher speaking step by step:

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
mkdir -p ~/.hermes/profiles/<profile>/skills/productivity/explaining-to-adhd
cp skills/explaining-to-adhd/SKILL.md ~/.hermes/profiles/<profile>/skills/productivity/explaining-to-adhd/

# Option B: default (no-profile) install
mkdir -p ~/.hermes/skills/productivity/explaining-to-adhd
cp skills/explaining-to-adhd/SKILL.md ~/.hermes/skills/productivity/explaining-to-adhd/
```

Then start a new session (`/reset`).

## Maintaining across profiles

The skill is installed in three places locally. Edit in the coding profile
(`~/.hermes/profiles/coding/skills/productivity/explaining-to-adhd/SKILL.md`),
then copy that file to the other locations so they stay identical.

## Provenance

- `wait-what` concept: https://www.aihero.dev/skills-wait-what
- Plain-language discipline: ASD-STE100 (https://github.com/AminBlg/SimpleEnglish)
- Skill file: MIT licensed.

## Privacy

This is an instruction file only — markdown text. No code runs, no network calls,
no telemetry, no credentials, no personal data.
