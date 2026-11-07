## Unit 7 — Issue selection

**Issue link:** [https://github.com/codepath/pathreview-ai201-fa26-howard/issues/66](https://github.com/codepath/pathreview-ai201-fa26-howard/issues/66)

**Issue title:** structlog output is not captured by pytest caplog — log assertions fail suite-wide

**Tier:** [X] Tier 1  [ ] Tier 2  [ ] Tier 3

**Problem summary:**
The app logs through structlog, but structlog isn’t wired into Python’s standard logging during tests, so pytest’s caplog never sees the messages. The code logs correctly, but the log assertions fail. In tests, structlog isn’t configured to hand its output to Python’s standard logging, so every caplog assertion in the suite fails. The fix is to configure structlog in tests/conftest.py so events become standard log records.

**Branch name:** fix/66-structlog-caplog

**Setup confirmation:** [X] App runs locally at localhost:5173

**Cohort ledger:** [X] Issue added to cohort ledger
