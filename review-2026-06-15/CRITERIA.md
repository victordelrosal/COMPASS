# COMPASS Review — Acceptance Criteria (frozen at FRAME)

1. Every broken or dangling reference in the COMPASS files is identified with file:line evidence. (env-checkable: grep)
2. Every COMPASS file (COMPASS.md, COMPASS-MINI.md, COMPASS-LLM-BUILD.md, LIMITATIONS.md, README.md, INSTALL-UNIVERSAL.md, CLAUDUS.md, ASCII-ART.md) is given an explicit KEEP / REFRESH / RETIRE verdict with a one-line rationale.
3. The review names at least 3 specific 2026 agentic failure modes COMPASS does not currently address, each tied to a concrete sBs learning (e.g. the blank-engine verify rule, cold-verifier-beats-self-critique, unattended-loop security tax, prompt-injection via skills/MCP).
4. For every recommended change there is a concrete redline: exact proposed text, exact deletion, or exact replacement. No "consider improving" non-recommendations.
5. Recommendations are prioritized P0 (bug) / P1 (high-value) / P2 (nice-to-have), and the P0 set contains only bug-fixes (broken refs, stale dates), nothing doctrinal.
6. No recommendation duplicates content already in global ~/.claude/CLAUDE.md (verify-before-done, no em dashes, Dropbox rules, palette, tiering). Additions either live in COMPASS or reference CLAUDE.md, never copy it.
7. A cold red-team verifier, given only this CRITERIA.md and the artifacts (not the builder's reasoning), passes every criterion with evidence.
8. The review preserves COMPASS's core thesis (small canon; only what the model does not already do); every proposed addition is justified against that bar and the net canon does not re-bloat toward the retired v2.1 framework.
