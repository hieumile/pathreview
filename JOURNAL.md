## Week 7 — Issue selection

**Issue link:** https://github.com/ascherj/pathreview/issues/37

**Issue title:** Add snapshot tests for prompt templates to catch accidental changes

**Tier:** Tier 1

**Problem summary:**
Prompt templates directly affect review quality. Add snapshot tests that fail if a template's content changes without a version bump, so developers must consciously version templates rather than silently editing them. the part of the codebase it affects is the tests path.

**Branch name:** test/37-add-snapshot-tests-for-prompt-templates

**Setup confirmation:** [X] App runs locally at localhost:5173

**Cohort ledger:** [X] Issue added to cohort ledger