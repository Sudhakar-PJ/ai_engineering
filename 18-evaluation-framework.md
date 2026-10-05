# Evaluation Framework

> The 5-minute assessment for any new tool, skill, or model. Used in A7, A8, A9.

---

## The 5 Questions

Ask these in order. If any answer is "no" or "unclear," the tool is likely not worth your time.

### 1. Does it solve a real problem I have?

- **Yes** — you've felt the pain; the tool addresses it.
- **No** — you're adopting because it's popular. Skip.
- **Unclear** — you don't actually know what problem it solves. Skip.

**The problem must be concrete.** "Better AI" is not a problem. "I keep rewriting the same prompt boilerplate" is.

### 2. Does it fit my stack?

- **Yes** — works with Antigravity/Codex/Cursor, free tier, TypeScript/Node.
- **Partially** — one aspect fits; another requires compromise.
- **No** — requires infrastructure or platform you don't have.

**Stack fit**:

- Primary agent: Antigravity
- Secondary: Codex CLI, Cursor
- Runtime: Node.js + TypeScript
- Data: Postgres, Redis, MongoDB
- Free tier or local only

### 3. Is there a free tier or local path?

- **Yes, generous** — free tier usable for real work.
- **Yes, limited** — free tier only for demos; production needs paid.
- **No** — paid only. Only acceptable if you can build a free alternative.

**Zero-spend guarantee**: no tool that's paid-only.

### 4. What's the lock-in?

- **None** — open standard; data exportable; migration path exists.
- **Low** — proprietary format but well-documented; alternatives exist.
- **High** — proprietary, no export, vendor-specific APIs everywhere.

**Prefer tools with export paths.** If lock-in is high, the tool must deliver significant value.

### 5. Is it actively maintained?

- **Yes** — recent commits, active issues, responsive maintainers.
- **Slowing** — last commit 3–6 months ago.
- **Dead** — no commits in 12+ months.

**Check**: last commit date, open PR count, issue response time.

---

## Red Flags

Any of these → skip, or proceed with caution.

- Paid-only with no free tier
- Single-vendor with no open standard
- No commits in 12+ months
- Hundreds of open issues with no responses
- Hype-driven (Twitter/Reddit push, no technical depth)
- Requires proprietary infrastructure you don't have
- No documentation, no examples
- Authored by unknown entity with no track record
- Bundles telemetry you can't disable

---

## Green Flags

Any of these → strong signal to try.

- Open source with clear license
- Active community (Discord, GitHub discussions)
- Well-documented with examples and use cases
- Layered design (progressive disclosure, plugin architecture)
- References + eval results published
- Comparison to alternatives documented
- Maintained by recognized contributors
- MIT/Apache licensed
- Local-first or self-hostable

---

## The Verdict Framework

| Verdict   | When                                                  |
| --------- | ----------------------------------------------------- |
| **Adopt** | All 5 questions = Yes/positive. Adopt now.            |
| **Trial** | 4/5 positive. Try on one project; revisit in 30 days. |
| **Hold**  | 3/5 positive. Bookmark; revisit in 6 months.          |
| **Skip**  | Fewer than 3 positive. Not worth your time.           |

---

## Example Evaluations

### Example 1: openclaw-skill-vetter-mcp

1. **Problem**: I need to vet skills before installing them. Yes.
2. **Fit**: MCP server; works with Antigravity. Yes.
3. **Free**: Free. Yes.
4. **Lock-in**: None; MCP standard. Yes.
5. **Maintained**: Active. Yes.

**Verdict**: **Adopt**.

### Example 2: CodeRabbit

1. **Problem**: PR review at scale. Yes.
2. **Fit**: GitHub integration. Yes.
3. **Free**: Free for public repos. Yes.
4. **Lock-in**: Low; open standard PR comments. Yes.
5. **Maintained**: Active. Yes.

**Verdict**: **Adopt** (for public repos).

### Example 3: [hypothetical paid-only LLM observability platform]

1. **Problem**: Observability for AI calls. Yes.
2. **Fit**: Hosted only; requires API keys. Partial.
3. **Free**: No free tier. No.
4. **Lock-in**: High; proprietary format. No.
5. **Maintained**: Active. Yes.

**Verdict**: **Skip** — build with OpenTelemetry instead.

---

## Logging

Every evaluation goes into `tool-evaluations.md`:

```
## [Tool Name] — YYYY-MM-DD
- Problem:
- Fit:
- Free tier:
- Lock-in:
- Maintained:
- Verdict: Adopt / Trial / Hold / Skip
- Revisit on: YYYY-MM-DD (if not Adopt)
- Notes:
```

**Revisit cadence**: quarterly for Hold/Skip verdicts. Tools improve.

---

## When to Skip Evaluation

- Trivial tools (utilities you use once and forget)
- Tools already in the stack (no need to re-evaluate)
- Tools with obvious "no" answers (paid-only, dead, wrong platform)

For all others, run the 5-minute check.
