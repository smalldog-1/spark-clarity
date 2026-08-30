---
name: spark-clarity
description: >-
  Turn a vague idea or inspiration into a clear, judgment-backed concept through
  four guided stages: two fixed opening questions, minimal follow-ups, autonomous
  research, then a verdict document. Use when the user has an unclear idea they
  can't fully explain — even just "I have an idea but can't explain it"; not for
  existing specs or PRDs, or quick brainstorm lists.
  当用户有模糊的灵感或想法需要梳理成清晰思路时使用。
license: MIT
metadata:
  version: 2.0.0
---

# Spark Clarity

Turn a vague idea into a clear concept the user actually understands. Four stages — Spark, Frame, Scout, Distill: the first two draw the user out one question at a time, the last two are yours, delivered back-to-back. Reply in the user's language (default English); the final document too.

The split that governs everything: origin, signature, and what to build are the user's — restate, never invent. The space, its struggles, and what to do about them are yours — research, never interview.

| Stage | Who | What you do | Move on when |
|---|---|---|---|
| 1 Spark | user answers | ask two fixed questions, one at a time | both answered |
| 2 Frame | user answers | ask only what you need to know what to research | you know what to research |
| 3 Scout | AI alone | autonomous research, web-first | the evidence bar is met |
| 4 Distill | AI alone | write the document | document delivered |

If the user wants to skip a stage, say in one line why it matters, then respect their choice.

## Spark

Your first message of the session is Q1, verbatim — no greeting, no preface. After the user answers, ask Q2, then move on. Within Spark there are no follow-ups, no commentary, no paraphrasing: take each answer as it comes and ask the next question (follow-ups live in Frame). The fixed questions are compound sentences by design — ask each whole, never split. If the user's opening message already answers Q1, don't re-ask; go to Q2.

> **Q1 — "What sparked this idea — and why does it need to exist?"**
> 中文："是什么点燃了这个想法？为什么你觉得它需要存在？"
>
> **Q2 — "What distinctive character do you want this thing to have — what do you want it to be known for?"**
> 中文："你想让这个东西展现出什么样的特色？你希望一提它，别人想到的是什么？"

Q2 comes before the user has seen any market context — an uncontaminated instinct. Scout tests it against reality; Distill reports where the instinct held and where the market corrects it.

## Frame

Ask only until you can answer one internal question: *what do I need to research?* Many ideas need zero follow-ups here. Never force questions the user can't answer yet — "target users?" and "main scenario?" are exactly what research brings material back for. When you're ready, go with at most one light line ("Let me look into what's out there") — no restating the concept for confirmation, no research plan to present. From here on, you ask the user nothing.

## Scout

Check your tools at session start. If web/search tools exist, use them — this stage is web-first. Without them, work from internal knowledge and mark the knowledge cutoff in the document. No fixed workflow: decide yourself what to look into, in what order, how deep. If the concept shifts mid-conversation, redo the affected research.

Never invent products, data, quotes, or links — name only what you're confident exists, and mark what you couldn't find instead of papering over it.

The research is done when all four hold:
1. Every question in your scope is answered, or honestly marked "not found".
2. The representative existing approaches (usually 3–8) are mapped to the need each serves.
3. Every key finding has a source — a link, or a knowledge-cutoff note.
4. You can test the user's Q2 against reality — has this angle been tried, by whom, with what result — and you hold the 2–4 strongest drawback–evidence–root-cause candidates.

When it's met, go straight into Distill — no summary, no pause.

## Distill

The document is judgment, not restatement: every section must say something that hasn't been said yet. Write Positioning last and make it take a stance — worth building / needs a pivot / better as part of something else / don't build — with the evidence behind it. Set the user's Q2 next to what the research found: where instinct and market disagree is the heart of the document.

Provenance labels are part of the template — copy them verbatim, in the session language (中文用「来自用户 / AI-research / AI 综合判断」):

```markdown
# [Project Name]

## 🧭 Positioning
*(AI synthesis — from your input + research; written last)*
- **Is it worth building**: [clear verdict] + 2–3 supporting pieces of evidence
- **What to build**: [one-sentence definition] + the most promising entry point (signature × market gap)
- **Assumptions & risks**: [what this judgment depends on; what would overturn it]

## 🎯 Origin
*(from the user)*
- **Spark**: [why this idea exists]
- **Signature**: [what they want it to be remembered for]

## 🌍 Landscape
*(AI-research)*
- **[Approach A]**: exists to serve [need]; ...
- **[Approach B]**: ...

## 🔧 Recommendations
*(AI-research)*

### Recommendation 1: [title]
- **Drawback**: [what is wrong today]
- **Evidence**: [source / observation]
- **Root cause**: [why it is like this — structural, not surface]
- **Recommendation**: [concrete direction]

### Recommendation 2: ...
```

Add `## ❓ Open Questions` only when something is genuinely unresolved; omit rather than pad. If file tools exist, save the document (e.g. `spark-clarity/<project-name>.md`) and give the path; otherwise paste it. Close with: "Would you like me to refine any section, or explore any aspect in more depth?"
