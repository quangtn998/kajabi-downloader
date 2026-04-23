# Downloader for Kajabi

Chrome extension for detecting and downloading videos from Kajabi lesson pages.

## Current state

- Extension login/activation has been removed
- Users still need valid access to the Kajabi page itself for private lessons
- Active Manifest V3 background worker uses `serp-bundles/background-service-worker.graph.js`

## Features

- Detects video content on Kajabi pages
- Opens a popup UI for extraction and download
- Handles background download flow through the extension service worker
- Includes bundled download and media-processing modules already checked into the repo

## Install locally

1. Open `chrome://extensions`
2. Enable `Developer mode`
3. Click `Load unpacked`
4. Select this folder: `/Users/tranngocquang/Downloads/kajabi-downloader`

## Project files

- `manifest.json`: extension manifest
- `popup.html`: popup entry
- `popup-enhanced.js`: popup behavior
- `background-enhanced.js`: source background logic
- `serp-bundles/background-service-worker.graph.js`: active background worker from manifest
- `detectors/`: page-specific video detection logic
- `download-manager/`: download orchestration and UI integration
- `modules/`: media helpers and bundled vendor code

## Notes

- There is no build setup in this repo right now; committed bundle files are used directly
- If you change source behavior for popup/background, keep the active bundle in sync with `manifest.json`
- Local-only files are ignored through `.gitignore`

## GitHub

Public repo:

- [quangtn998/kajabi-downloader](https://github.com/quangtn998/kajabi-downloader)

## License

MIT
