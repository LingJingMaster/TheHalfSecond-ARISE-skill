# TheHalfSecond-ARISE-skill

> 🌐 **Language**：[中文（主 / primary）](./README.md) · **English**

> A **single-file AI agent skill** that distills the core method of Li Xiaolai's *The Half Second* into a tool you can call on demand
> Use an **ARISE script** to edit your "first reaction." This repo is **Chinese-primary**, with an **English translation** alongside.

- Drop [`SKILL.en.md`](./SKILL.en.md) into any Skill-aware AI assistant (Claude Code, Claude.ai, GitHub Copilot CLI, Amp, …)
- When you say "I want to change a habit / I snap when provoked / the inner critic / panic with money"
- the assistant follows the book's method to **draft a script → route-check it → plan how to install it**.

> 📄 The two skill files in this repo have identical content, in different languages:
> - [`SKILL.md`](./SKILL.md) —— **Chinese (primary)**
> - [`SKILL.en.md`](./SKILL.en.md) —— **English**
>
> Either can be used directly as a skill — pick the one in your language.

---

## What this is

- A "first reaction" is what you do in the **half-second** before you can think — reaching for the cigarette, snapping back, panic-selling, hearing "you're not good enough."
- Willpower can't reach that window, because it arrives too late.

The book's method: **repeat one chosen sentence** until the brain's "familiarity counter" makes it the new default. The framework for writing that sentence is **ARISE**:

| Letter | Dimension | In one line |
|---|---|---|
| **A** | Action | The only required part: a behavior the body can do under stress |
| **R** | Reason | Optional: a `because` you'd still mean on the 1000th rep |
| **I** | Identity | Usually carried implicitly by the action verb |
| **S** | Situation | Optional: named only when it fires at a specific cue |
| **E** | Emotion | Optional: invest *real* feeling — never performed |

---

## How to use

### Option 1: One-line install (recommended)

```bash
# Install to whichever agent the current project recognizes (auto-detects the root SKILL.md)
npx skills add LingJingMaster/TheHalfSecond-ARISE-skill

# Install specifically to Claude Code
npx skills add LingJingMaster/TheHalfSecond-ARISE-skill -a claude-code

```

> The CLI detects the repo's root `SKILL.md` (the **Chinese primary** version) by default.
Restart your session, then say something like "I want to stop scrolling my phone before bed" to trigger it.

### Option 2: Copy into your skills directory

Put `SKILL.md` (or the English `SKILL.en.md`) into your client's skills directory, e.g.:

```bash
# Claude Code (personal skills)
mkdir -p ~/.claude/skills/half-second-arise
cp SKILL.en.md ~/.claude/skills/half-second-arise/   # use SKILL.md for the Chinese version
# Restart the session to trigger it
```

> Skills directories vary by client (`~/.copilot/skills`, `~/.agents/skills`, `.claude/skills`, …) — place it in the matching one.

### Option 3: Use it as a plain prompt
Even if your assistant has no Skill mechanism, paste the contents of `SKILL.en.md` as a system prompt / context, then describe the reaction you want to edit.

---

## A minimal example

> **You**: I start scrolling my phone the moment I sit on the couch, often until past midnight.
>
> **Assistant (using this method)**:
> - Action (not a mood like "use my phone less"): **"When I sit on the couch, I put my phone out of reach first."**
> - Scope: situated (trigger = sitting on the couch)
> - Route-check: say it aloud — if it feels "mildly silly, then nothing," it's right; if your chest tightens, rephrase
> - Install: repeat anywhere, expect the first ~100 reps to feel stupid (normal), plan for 3–12 months, and add a little environmental friction (move the charger to the bedroom)

---

## Credit to the original author

Every idea in this skill — "the half-second," "frequency counter," "routing," "ARISE," "identity is the hub," "re-ordering, not erasure" — comes from Li Xiaolai's book **《The Half Second: How first reactions get installed, and how to edit them》**.

- Original author on GitHub: **[@xiaolai](https://github.com/xiaolai)**

This repo only organizes the book's operational method into a single-file skill an AI assistant can call. **Copyright and originality belong to the author.** If the method helps you, please read the book — it has the full mechanism, the research, and the cases.

---

## Notes & boundaries

- This skill is for editing **everyday, language-accessible** first reactions. It does **not** replace professional medical or psychological care.
- For severe trauma, substance dependence with physical withdrawal, an active psychiatric crisis, or any abusive / coercive relationship, seek professional help — see the "When NOT to use this" section at the end of [`SKILL.en.md`](./SKILL.en.md).

---

## License

The skill files (the organizing/rewriting work) are released under the MIT license; the underlying ideas and framework remain the copyright of the original author, Li Xiaolai.
