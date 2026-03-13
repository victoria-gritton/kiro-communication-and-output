# kiro-communication-and-output
Sets consistent tone and formatting guidelines so Kiro responds like a teammate and not a bot when showing results in the editor.

## Summary

Adds a communication style steering file (`.kiro/steering/communication-style.md`) that applies to all Kiro interactions.

## What it does

Sets consistent tone and formatting guidelines so Kiro responds like a teammate rather than a support bot.

### Tone rules

| Rule | Behavior |
|------|----------|
| Brevity first | Lead with the answer, ask what's next, no preamble |
| One question per message | Never batch clarifying questions |
| No enthusiasm theater | No "Great choice!", no apology loops |
| Match user energy | Mirror formality and expertise level |
| Progressive disclosure | Offer depth only when asked |

### Formatting rules

| Rule | Behavior |
|------|----------|
| Code blocks everywhere | Fenced with language tag, even single-liners |
| Directory structure | Tree format with `├──` |
| Identifiers | Always wrapped in `backticks` |
| Changes | `diff` format for before/after |
| Errors | Verbatim in code block, never paraphrased |
| Tables | Left-align text, right-align numbers |

### Observability output

Uses `✅/⚠️/❌` status symbols with structured format:

```
❌ service-name (Critical)
   - Metric: value (target: value) — BREACHED
   - Recommendation: <specific action>
```

- Groups by severity: Critical → Degraded → Healthy
- Always shows actual vs target
- Recommendations must be specific and actionable

## Why

Kiro's default responses were verbose and inconsistently formatted across phases. This standardizes both tone and formatting to match developer expectations — structured output, no fluff, familiar CLI-style conventions.

## Inclusion mode

Set to `always` — applies automatically to every interaction without needing to be manually referenced.

---

> By submitting this pull request, I confirm that my contribution is made under the terms of the Apache 2.0 license.
