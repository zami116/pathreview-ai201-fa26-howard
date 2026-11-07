## Unit 7 — Issue selection

**Issue link:** [https://github.com/codepath/pathreview-ai201-fa26-howard/issues/66](https://github.com/codepath/pathreview-ai201-fa26-howard/issues/66)

**Issue title:** structlog output is not captured by pytest caplog — log assertions fail suite-wide

**Tier:** [X] Tier 1  [ ] Tier 2  [ ] Tier 3

**Problem summary:**
The app logs through structlog, but structlog isn’t wired into Python’s standard logging during tests, so pytest’s caplog never sees the messages. The code logs correctly, but the log assertions fail. In tests, structlog isn’t configured to hand its output to Python’s standard logging, so every caplog assertion in the suite fails. The fix is to configure structlog in tests/conftest.py so events become standard log records.

**Branch name:** fix/66-structlog-caplog

**Setup confirmation:** [X] App runs locally at localhost:5173

**Cohort ledger:** [X] Issue added to cohort ledger

**Selection notes ("Is this right for me?" checklist):**

- [x] I can explain the problem and the expected behavior in 2–3 sentences without reading the issue.
- [x] I've located the relevant files and confirmed they exist in the codebase.
- [x] I can describe a concrete before-and-after: what the user sees before the fix and what they see after.
- [x] I'm choosing Tier 1.
- [x] I'm not choosing a Tier 3 issue to "challenge myself" if I haven't completed a Tier 1 or 2 first — scope surprises in Unit 9 don't have a safety net.
- [x] I've found and read the specific code the issue references (not just the file — the function or section).
- [x] I've read enough surrounding context that I can write a rough plan for the fix without looking anything up.
- [x] I've found the test file for my module and read at least one test end-to-end.
- [x] I've checked the issue comments and the ledger's Claims count, and I'm fine with how many others are on this issue.
- [x] I've estimated the time this will take and I'm confident I can complete it before the Unit 9 deadline.
- [x] This issue has no open blockers or dependencies on other unresolved issues.
