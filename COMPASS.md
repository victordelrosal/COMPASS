# COMPASS: Victor's Coding Canon

Version 3.0. Personal canon. May 2026.

This is Victor's working coding discipline. It is deliberately small.

---

## What loads automatically

`COMPASS-MINI.md` is the actual standard, loaded at SessionStart by hook. Five rules: red flags that mean stop, ask before risky data ops, one hypothesis at a time, simplicity first, surgical changes. That is the entire runtime guardrail.

## What loads only when relevant

`COMPASS-LLM-BUILD.md`: load when actually building AI features. Covers prompt injection, output validation, sensitive data in pipelines, LLM endpoint cost and rate controls. Skip for ordinary code.

## What lives elsewhere

Agent orchestration: see the `agentic-orchestration` skill (research-grounded, with hard numbers and red flags, superior to anything written here).

Web design and HTML output: see the `web-design-standard` skill plus the Lapis Lazuli + Antique Gold palette in `~/.claude/CLAUDE.md`.

Formal reports: see the `formal-report-standard` skill.

Personal preferences (no em dashes, succinct natural-academic voice, Dropbox protection rules, palette, path shortcuts, time discipline): live in `~/.claude/CLAUDE.md`, project CLAUDE.md, and project-specific files. They are not duplicated here.

Security for ordinary code (OWASP, input validation, auth, parameterized queries, secrets handling): Opus 4.8 follows these by default. If a project needs a written security standard for compliance audit, that is a separate compliance artefact, not runtime context.

TDD, SOLID, naming conventions, Clean Code: model defaults. If a project needs deviation, document the project-specific rule in that project's CLAUDE.md.

---

## Where the agency canon lives

COMPASS-MINI is the always-on, ordinary-coding guardrail. The agentic disciplines live where they load when relevant, and COMPASS does not duplicate them:

- Verifying your own work before claiming done: the blank-engine rule in `~/.claude/CLAUDE.md`.
- Long-run drift, cold-verifier-over-self-critique, cost and STOP gates: the `crank` skill.
- Confidence calibration and not overselling: `/bet-weights`.
- Multi-agent orchestration and context budgets: the `agentic-orchestration` skill.

---

## Why this canon is small

The previous version of COMPASS was a 6,500-line public framework with eight modules. After a 2026-05 review, most of it taught Opus 4.7 things it already knew (SOLID, naming, TDD, OWASP), or duplicated content across modules (prompt injection rules appeared in three files near-verbatim). The framework had outpaced the model it was written for.

What remains: only the rules that fire often, only the rules that catch real failures, only the rules Opus 4.8 does not already follow by default.

The full v2.1 framework is preserved at git tag `v2.1-archive` for anyone who wants to fork the long version.

---

## Loading discipline

At session start: MINI loads via hook. Nothing else.

When working on AI features: explicitly load COMPASS-LLM-BUILD.

For everything else: trust the model, trust the skills, trust CLAUDE.md.

If something is needed often enough that it should be canon, add it to MINI. If it fires rarely, it does not belong in runtime context.
