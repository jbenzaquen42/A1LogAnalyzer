# A1 Log Analyzer

A1 Log Analyzer is a browser-based analysis tool for A1 Acoustix measurement session logs (January 20, 2026 format and later). This repository now includes a clean structure for preserving the original analyzer, hosting the current working version, and tracking project planning.

## Repository Structure

```text
A1LogAnalyzer/
├── app/
│   └── index.html                      # Current working analyzer UI
├── archive/
│   └── original/
│       └── original-analyzer-v3.5.html # Preserved original source upload
├── samples/
│   └── fake_logs.zip                   # Example logs for local testing
├── docs/
│   ├── ROADMAP.md                      # Product and technical roadmap
│   └── IMPLEMENTATION_PLAN.md          # Implementation and validation plan
└── README.md
```

## Original File Preservation and Credit

The first repository upload preserves the original analyzer file in `archive/original/original-analyzer-v3.5.html`.

- **Original creator credit:** Original creator is currently not explicitly identified in the source file metadata. This project preserves the original work and keeps attribution ready to update as soon as the creator name is confirmed.
- **Action item:** Once creator details are confirmed, update this section and add explicit attribution in both README and the in-app About section.

## Current Application Entry Point

Use `app/index.html` as the main file for ongoing development and improvements.

## Local Usage

1. Open `app/index.html` in a modern browser.
2. Upload one or more A1 log files.
3. Review chart and table outputs.
4. Use `samples/fake_logs.zip` to test parser behavior with sample datasets.

## Project Documentation

- Roadmap: [`docs/ROADMAP.md`](docs/ROADMAP.md)
- Implementation and testing plan: [`docs/IMPLEMENTATION_PLAN.md`](docs/IMPLEMENTATION_PLAN.md)

## Professional Standards for This Repository

- Preserve the original source in the archive folder.
- Keep enhancements isolated to `app/` and supporting documents.
- Use consistent naming and explicit documentation for releases.
- Record verification steps for every feature update.
