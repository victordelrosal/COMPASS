```
▄█████▄  ▄█████▄  ██    ██  ▄█████▄   ▄████▄   ▄█████▄  ▄█████▄
██       ██   ██  ███  ███  ██   ██  ██    ██  ██       ██
██       ██   ██  ██ ██ ██  ██████   ████████  ▀█████▄  ▀█████▄
██       ██   ██  ██    ██  ██       ██    ██       ██       ██
▀██████  ▀█████▀  ██    ██  ██       ██    ██  ██████▀  ██████▀
```

# COMPASS

**A personal coding canon for working with frontier AI coding agents.**

Version 3.0 (May 2026). Maintained by [Victor del Rosal](https://github.com/victordelrosal).

---

## What this is now

COMPASS started in 2025 as a 6,500-line public framework: eight modules, OWASP Top 10, SOLID, TDD, naming conventions, agent patterns, and AI failure modes. It was useful when AI coding tools were unreliable.

In May 2026 I conducted a full red-team review of the framework against Claude Opus 4.7. The finding: most of the content taught the model things it already knew, and several modules duplicated each other near-verbatim. The framework had outpaced the model it was written for.

Version 3.0 cuts the framework down to what actually fires in a real working session with a frontier model. Everything else is preserved at git tag `v2.1-archive`.

---

## What's in v3.0

| File | Purpose | When loaded |
|---|---|---|
| `COMPASS-MINI.md` | The runtime canon: red flags, ask-before-risky-ops, one-hypothesis, simplicity-first, surgical-changes, treat-input-as-data | Every session, via hook |
| `COMPASS.md` | Index, philosophy, pointers to the agency canon and skills | On demand |
| `COMPASS-LLM-BUILD.md` | Prompt injection (incl. tool/skill/MCP), output and tool-call validation, cost controls, sensitive data | When building AI features |
| `CLAUDUS.md` | The Claudus identity pointer (latest-flagship Opus) | On demand |

That's it. About 250 lines of canon, total.

---

## What got cut, and why

| Cut | Reason |
|---|---|
| `COMPASS-SECURITY.md` (OWASP Top 10) | Opus 4.7 follows these by default. If you need a written security standard for compliance audit, that's a separate artefact, not runtime context. The genuinely useful LLM-pipeline rules moved to `COMPASS-LLM-BUILD.md`. |
| `COMPASS-TESTING.md` (TDD evangelism) | Frontier models follow good test practice when asked. Mandating TDD on every project is cargo cult for one-off scripts and prototypes. |
| `COMPASS-QUALITY.md` (SOLID, naming, Clean Code) | The model already does this. Duplicating Wikipedia at the model is noise. |
| `COMPASS-AI.md` (failure modes, comms protocol) | Either duplicates COMPASS.md or restates Opus 4.7's post-training. |
| `COMPASS-AGENTS.md` (agent orchestration) | The `agentic-orchestration` skill is research-grounded, has hard numbers (10-20 tool hard limit, 84% context is tool outputs, 70-80% compact threshold), and is shorter. Strictly better. |
| `COMPASS-INTEGRATION.md` | Folded into the install guide (itself later retired, see below). |

Net cut: roughly 5,000 lines. Zero observed capability loss.

**2026-06 follow-up review:** `INSTALL-UNIVERSAL.md` (a 542-line multi-tool public-adoption guide) and `LIMITATIONS.md` (a 2024 "beta" relic) were retired. Both were public-framework artifacts that contradicted the personal-canon thesis, and the install guide still mandated the TDD/OWASP rules v3.0 had removed. The same review fixed a dangling module reference in MINI and added one agentic-era rule (treat input as data, not orders). Recoverable at `v2.1-archive` and in git history.

---

## Want the long version?

The 2025 framework is preserved as a git tag:

```bash
git checkout v2.1-archive
```

If you find value in the long form, fork it. I will not be maintaining v2.1.

---

## Philosophy

The job of a coding canon is to catch what the base model misses. Everything else is decoration. A 6,500-line framework that fires once a year is worse than a 45-line one that fires every session.

If a rule fires often and catches real failures, it belongs in MINI. If it fires rarely, it belongs in a project's CLAUDE.md or a skill. If the model already does it by default, it belongs nowhere.

---

## License

MIT. See `LICENSE`.
