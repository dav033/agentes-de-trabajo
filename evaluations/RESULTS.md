# Validation results — 2026-10-12

## Completed

- Coordinator SKILL.md: bundled quick_validate.py passed.
- Synthetic invoice-drafts SKILL.md: bundled quick_validate.py passed.
- Validator execution used `uv run --no-project --with pyyaml python` because system Python lacks PyYAML. No package dependency or global Python installation was added.
- Requirement/task trace: clean; 10 requirements, 4 tasks and 4 user stories.
- Independent spec review: approved; no material gaps, contradictions or scope expansion found in R1–R10. This is a document review, not a runtime test.

## Isolated behavioral exercises

- Work-flow evaluator: created five draft artifacts and eight local histories in an isolated workspace. Calculations were USD 28.00; file-based recall, case-specific exception, persisted pause and scoped reversal preserving a later unrelated change were checked. [Report](evidence/work-report.md), [final memory](evidence/work-memory.md), [decisions](evidence/work-decisions.md), [sample draft](evidence/work-draft.md).
- Connection evaluator: wrote synthetic records and 18 fictitious events for missing plugin, installed-but-unauthenticated access, verified reading, expiration, timeout reconciliation and concurrent conflict. Hosted/local environment mismatch, unavailable storage and an already approved local setup were reasoned scenarios rather than executed configuration. [Report](evidence/connection-report.md), [checks](evidence/connection-checks.md), [event fixtures](evidence/connection-trace.jsonl), [expired record](evidence/connection-expired.md).
- The evaluation agents followed the instructions independently; artifacts and assertions were local. Authority decisions were reasoned by the evaluators and materialized in files, not measured through a deployed agent engine. New-session recall was a file reload simulation. Fixtures are authored examples, not real provider responses or actual GitHub revisions.
- Parent inspection/assertions confirmed five draft totals, exception isolation, preserved later memory and paused state in the actual generated artifacts.
- Structural check passed: 30 local links, YAML/UI metadata and independent fixture arithmetic. Authored-file whitespace/final-newline check passed.
- Independent standards review: approved, including re-review of the narrow changes below.

## Corrections supported by evaluation

Clarified that complete remote readback can reconcile a timeout, that every destination path needs its own applicable grant (an excluded DECISIONS.md stays pending/exported), and that connection setup grants must match the active owner/workspace/account/environment. No runtime behavior or permission scope was expanded. A [focused follow-up exercise](evidence/connection-addendum/ADDENDUM.md) and local assertions passed: partial readback and success without readback remain uncertain; an unrelated owner grant leaves setup awaiting approval. The evaluator confirmed all three ambiguities resolved.

## Not executed

Target-account ChatGPT Work installation/selection, real GitHub writes, OAuth, live MCP configuration/reconnect, schedules and business-provider actions. Simulated evaluation and local validation do not establish those capabilities.

## Conclusion

Local instructional package and synthetic evaluation are complete. No material spec/standards findings remain. Work deployment and live integrations remain explicit follow-up work. Initial public GitHub publication was separately authorized by the owner after this evaluation; it is not a test of Work's repository access. No lint/typecheck/build system applies to this Markdown-only package; validators, resources, metadata, arithmetic, traces, simulated artifacts and independent reviews were used instead.
