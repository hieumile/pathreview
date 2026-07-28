## Week 7 — Issue selection

**Issue link:** https://github.com/ascherj/pathreview/issues/37

**Issue title:** Add snapshot tests for prompt templates to catch accidental changes

**Tier:** Tier 1

**Problem summary:**
Prompt templates directly affect review quality. Add snapshot tests that fail if a template's content changes without a version bump, so developers must consciously version templates rather than silently editing them. the part of the codebase it affects is the tests path.

**Branch name:** test/37-add-snapshot-tests-for-prompt-templates

**Setup confirmation:** [X] App runs locally at localhost:5173

**Cohort ledger:** [X] Issue added to cohort ledger

## Week 8 — Reproduction & solution planning

**Reproduction commit link:** https://github.com/hieumile/pathreview/commit/c5f0f10e45b4027b0481eecb513c6d8ffd2e0fa4

**Reproduction summary:**
Altering any prompt template inside `rag/generator/prompt_templates.py` results in a changed MD5 hash, yet `test_template_snapshot_content_hash` continues to pass. This happens because the test only asserts the output is a 32-character string rather than validating it against a reference hash.

**PLAN.md link:** https://github.com/hieumile/pathreview/blob/test/37-add-snapshot-tests-for-prompt-templates/PLAN.md

**Walkthrough video (recommended):** 

**Blockers or open questions:**
None.