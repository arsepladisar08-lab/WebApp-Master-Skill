# Independent Evaluator Protocol

## Purpose

Separate implementation from acceptance. The Generator builds the requested behavior; the Evaluator independently checks whether observable acceptance criteria are met.

The protocol can be followed by one agent in separate passes when a separate agent is unavailable. In that case, label the review as a self-review—not independent verification.

## Roles

### Planner
- Converts the request into observable requirements and acceptance criteria.
- Defines scope, affected interfaces/files, risks and test plan.
- Does not claim implementation completion.

### Generator
- Implements one coherent feature or vertical slice.
- Adds or updates tests.
- Reports changed files and commands run.
- Does not mark the feature accepted merely because its own code appears correct.

### Evaluator
- Starts from acceptance criteria, not the Generator's confidence.
- Inspects actual diff and relevant runtime behavior.
- Reproduces critical user flows independently.
- Runs targeted tests and checks role/data boundaries.
- Records evidence, severity and pass/fail decision.

## Acceptance contract

For each feature, record:
- ID and name.
- User-visible behavior.
- Preconditions and actor/role.
- Expected outcome.
- Negative and boundary cases.
- Data changes expected.
- Test method and expected evidence.

## Evaluation dimensions

| Dimension | Suggested weight | Must inspect |
|---|---:|---|
| Functional correctness | 35% | Acceptance criteria, real persistence and failure behavior |
| Security and data integrity | 25% | Authentication, authorization, RLS, ownership, validation |
| UX and accessibility | 15% | States, responsive behavior, keyboard and feedback |
| Code and architecture | 15% | Scope, types, errors, maintainability, dependencies |
| Performance and operations | 10% | Relevant performance, logs, configuration and deployment behavior |

A weighted score is diagnostic, not a substitute for blockers. Any critical security defect, data loss risk, broken P0 journey, secret exposure, or failed required check causes FAIL regardless of average score.

## Evidence protocol

For every check, capture:
- Exact command, URL/route or test scenario.
- Environment and identity/role used (never include credentials).
- Actual result and expected result.
- Test output, screenshot, network response or database assertion as appropriate.
- Pass, fail, blocked or not run.

Do not fabricate screenshots, test output, CI status or database evidence.

## Decision

- **PASS:** all P0 criteria pass, no critical/high unresolved defect, required checks complete.
- **PASS WITH FOLLOW-UP:** all P0 criteria pass; only non-blocking known issues remain and are clearly documented.
- **FAIL:** any P0 criterion fails, a critical risk exists, or evidence is insufficient for a mandatory acceptance criterion.
- **BLOCKED:** verification cannot proceed due to missing environment, access, external dependency or user decision.

## Iteration

1. Evaluator publishes findings with file/line or test evidence.
2. Generator fixes only relevant defects and adds regression coverage.
3. Evaluator reruns failed and neighboring checks.
4. Update feature status only after acceptance.
5. Record unresolved limitations in the release report.
