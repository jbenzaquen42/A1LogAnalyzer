# A1 Log Analyzer

A1 Log Analyzer helps review A1X session logs from multiple measurements and compare results quickly in charts and tables.

## Credit

This project is based on and inspired by a Facebook post shared by **李益誠** in the Audyssey One Support community, where he shared the analyzer concept and usage notes.

## What changed from the original upload

The original HTML file is kept unchanged in:
- `archive/original/original-analyzer-v3.5.html`

The main working file is now:
- `app/index.html`

Major updates in the current working version include:
- Focus on multi-mic session analysis and aggregation controls.
- Drag-and-drop multi-file upload and support for loading more than one session log.
- View mode controls for aggregate per-channel analysis and per-position analysis.
- Expanded metric views including final SNR, SNR gain, acceptance rate, jitter metrics, peak-to-silence, peak magnitude, and impulse timing.
- SNR, acceptance, jitter, scatter, histogram, and heatmap visualizations for quick comparisons.
- Channel overview and diagnostics panels to highlight missing rows, low coverage, and potential data quality issues.
- Detailed tables with sorting behavior and CSV export.
- Chart image export and measurement export actions.
- Better handling for mixed logs, including legacy-like input fallback paths.

## Major next additions planned

- Extract parsing and metric logic from the inline script into dedicated modules.
- Add repeatable fixture-based parser and metric tests.
- Add CI checks so lint and tests run automatically for each change.
- Add clearer in-app error and warning messages for malformed logs.
- Improve large-file performance and accessibility.

## Quick start

1. Open `app/index.html` in your browser.
2. Upload one or more session log files.
3. Review summary cards, charts, diagnostics, and tables.
4. Use sample logs from `samples/fake_logs.zip` if needed.

## Project plan

Roadmap and implementation steps are combined in:
- `docs/PLAN.md`
