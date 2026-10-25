# AWS Certificate Generator

A single-page, browser-based certificate generator for producing AWS-themed student certificates from a predefined template.

## Purpose

This project generates personalized certificate PNG files using a canvas renderer that matches a fixed template layout (name block, university/group text block, and signature placement).

## Features

- Live certificate preview on canvas (preview uses the same renderer as export)
- Template/theme toggle (dark/light) with accent color controls
- Name input from:
  - CSV file (single-column support)
  - Manual pasted list
- Per-field positioning/size controls for fine alignment:
  - University block X/Y/size
  - Student name X/Y/size/letter spacing
  - Signature width/Y position
- Export options:
  - Current certificate as PNG
  - All loaded names as a ZIP of PNG files
- Safe output naming (`Certificate_<Name>.png`)

## Project Structure

- `/home/runner/work/awscert/awscert/index.html` — entire app (UI, rendering logic, embedded assets)
- `/home/runner/work/awscert/awscert/README.md` — project documentation

## How to Run

No build step is required.

1. Open `/home/runner/work/awscert/awscert/index.html` in a modern browser.
2. Load names from CSV or paste names manually.
3. Adjust layout controls as needed.
4. Download one PNG or all certificates as ZIP.

## Configuration Notes

- Rendering is tuned for a fixed high-resolution certificate canvas (3508×2475) used by the template.
- Text placement and sizing are controlled through on-page sliders.
- ZIP creation and file saving use CDN-loaded libraries:
  - JSZip
  - FileSaver.js

## Security and Privacy Notes

- This app is client-side only; name data is processed in the browser.
- No backend/API keys are configured in this repository.
- If you host this file publicly, review and pin third-party CDN dependencies for supply-chain risk control.

## Compatibility

Use an up-to-date Chromium, Firefox, or Safari browser for best results.
