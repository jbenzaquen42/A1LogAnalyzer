# A1 Log Analyzer Plan

## Why this plan exists

The tool is already useful, but most logic still lives in one HTML file. The goal is to keep current behavior stable while making future changes easier to validate and safer to release.

## Current baseline

- Original source preserved in `archive/original/`.
- Active development source is `app/index.html`.
- Sample logs available in `samples/fake_logs.zip`.
- UI already supports multi-file upload, charts, diagnostics, and export actions.

## Phase 1: Baseline and behavior lock

### Goals
- Document exactly how parsing and computed metrics behave today.
- Reduce accidental behavior changes during refactor.

### Tasks
- Map parser inputs and outputs for current log format and legacy fallback paths.
- Document metric formulas and displayed units.
- Write a short known-issues list for edge cases.

### Deliverables
- Parser behavior notes.
- Metric definition table.
- Baseline test checklist.

## Phase 2: Refactor for maintainability

### Goals
- Separate business logic from UI wiring.
- Make core logic testable without running the whole page.

### Tasks
- Move parser helpers into a dedicated module file.
- Move metric calculations and formatting into separate module files.
- Keep DOM update functions focused on rendering only.
- Add linting config and consistent formatting rules.

### Deliverables
- Modularized parser and metrics code.
- Basic lint command and style guidance.

## Phase 3: Correctness and validation

### Goals
- Ensure metrics stay accurate across different log variants.
- Catch malformed data early and explain errors clearly.

### Tasks
- Build fixture sets for valid, partial, malformed, and legacy-like logs.
- Add deterministic tests for parser outputs.
- Add expected-value tests for key computed metrics.
- Add user-facing warning messages for missing sections and invalid values.

### Deliverables
- Fixture library.
- Parser and metrics test suite.
- Improved warning and error messaging.

## Phase 4: UX and performance improvements

### Goals
- Improve readability and responsiveness for larger datasets.
- Keep the interface clear for day-to-day use.

### Tasks
- Improve chart readability on different screen sizes.
- Review table density, labeling, and unit consistency.
- Improve responsiveness when loading many logs.
- Add keyboard and accessibility improvements where practical.

### Deliverables
- UI cleanup pass.
- Performance notes with before/after checks.

## Phase 5: Release process and contribution flow

### Goals
- Make changes predictable to review and ship.
- Keep quality checks consistent.

### Tasks
- Add CI jobs for lint and tests.
- Add changelog and versioning pattern.
- Add contribution notes and a pull request checklist.

### Deliverables
- CI workflow.
- Changelog template.
- Contribution and PR checklist docs.

## Testing plan (every change)

1. Run parser and metric tests against fixture data.
2. Run browser smoke checks:
   - load single-position file
   - load multi-position files
   - switch view mode and metric mode
   - verify diagnostics update
   - export CSV and save charts
3. Check browser console for errors.
4. Record exact test commands and outcomes in the PR.

## Definition of done for upcoming milestones

- No regression on sample logs.
- No new console errors in standard flow.
- Updated docs for behavior changes.
- Test evidence included in PR.
