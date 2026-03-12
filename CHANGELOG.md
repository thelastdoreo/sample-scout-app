## v0.4.3 (2026-03-12)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.4.3_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.3/Sample-Scout_0.4.3_universal.dmg) |
| Windows | [Sample-Scout_0.4.3_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.3/Sample-Scout_0.4.3_x64-setup.exe) |
| Linux | [Sample-Scout_0.4.3_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.3/Sample-Scout_0.4.3_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- adaptive time ruler with colon format and letter spacing
- multi-resolution waveform system for editor zoom
- pre-rendered drag exports with Clip-typed pipeline

### Fixes
- dispatch synthetic pointerup after external drag to prevent text selection
- drag export respects clip custom name instead of using cached filename
- use actual pointer position for drag-out-of-window detection
- use time-based zoom cap (50ms min visible window)
- unblock UI during fine waveform generation
- increase fine waveform resolution and add short-file guard
- stale closures in ctrl+click and shift+click multi-select

### Other
- change multi-drag count badge color to neon-orange
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.4.2...v0.4.3

## v0.4.2 (2026-03-10)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.4.2_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.2/Sample-Scout_0.4.2_universal.dmg) |
| Windows | [Sample-Scout_0.4.2_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.2/Sample-Scout_0.4.2_x64-setup.exe) |
| Linux | [Sample-Scout_0.4.2_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.2/Sample-Scout_0.4.2_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- click-to-seek on waveform during editor playback
- add editor shortcut (C) to help screen

### Fixes
- analysis updates not reaching detail pane due to snake_case mismatch
- tune editor overlay glow values — 8px blur, consistent opacity, double-pass corner glow
- replace canvas sprites with DOM divs for play cursor and playback indicator
- correct editor toggle tooltip shortcut key (F → C)
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.4.1...v0.4.2

## v0.4.1 (2026-03-08)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.4.1_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.1/Sample-Scout_0.4.1_universal.dmg) |
| Windows | [Sample-Scout_0.4.1_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.1/Sample-Scout_0.4.1_x64-setup.exe) |
| Linux | [Sample-Scout_0.4.1_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.1/Sample-Scout_0.4.1_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- show CLIP label instead of file size for clips in set pane
- show clip bounds on detail pane waveform
- improve detail pane tag drawer and spacing
- redesign detail pane layout, spacing, and tag styling

### Fixes
- playback bar uses clip positions for clip-relative progress
- pass correct memberId to detail pane for set membership lookup
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.4.0...v0.4.1

## v0.4.0 (2026-03-07)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.4.0_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.0/Sample-Scout_0.4.0_universal.dmg) |
| Windows | [Sample-Scout_0.4.0_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.0/Sample-Scout_0.4.0_x64-setup.exe) |
| Linux | [Sample-Scout_0.4.0_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.0/Sample-Scout_0.4.0_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

# v0.4.0 — The Editor

### Introducing Clips

To support our editor I've now brought a concept of **clips** — a metadata-only format that has all the fade and cut data but behaves throughout the app just like samples do. Clips aren't real audio until you export them. Create them, recall them, refine them, and they stay linked to the source audio they came from.

### The Workflow

- Create clips from longer files and add them directly to your sets
- Easily add fades with custom curves to define clip boundaries
- Real-time preview means you hear exactly what your clip will sound like
- Clips are non-destructive until export — no wasted disk space while you experiment. When you do export, the system is smart about doing the least work necessary and carries forward file attributes already defined
- Clip badge in the editor gives you quick access to all clips on a sample — recall, rename, or delete from one place
- Clips auto-name themselves based on the source filename, and you can rename them inline from the clip badge dropdown or in the set pane

### The Editor

- Built a new **Editor panel** from scratch for viewing and working with audio at the waveform level. Open it with the new Editor button next to the detail pane info button in the playback area.
- Purpose-built waveform renderer using offscreen compositing for a clean look that maintains the app's overall feel.
- Editor area has adjustable height so you can balance browser and editor to your preference
- While the browser requires simple input and speed, the editor requires precision. Mouse controls are central because they feel natural in this context: Navigate with zoom, pan, scroll wheel, click-drag, and select keyboard shortcuts
- Careful attention paid to interaction feel and performance — precise mouse hit testing, smooth hover states, and visual feedback with a goal to work naturally and intuitively
- Clips open directly to their region so you're immediately looking at the relevant content

### Playback Engine

- Overhauled the playback system to support editor features, including brand new looping functionality
- A lot of work went into making the clip system interact with the existing app flow in a way that feels seamless and transparent
- Deep integration with the existing app — shared transport controls, unified state

### Under the Hood

- Caching improvements across the board for better responsiveness — layered caching pipeline, sprite caching, pre-composited static layers
- Extensive tuning and refinement of editor visuals, scrollbar behavior, toolbar consistency, and playback smoothness - still WIP. Expect more polish and changes
- Added a regression testing suite to maintain performance and quality as the editor evolves

### Fixes

- Deleted samples now restore to their original position in a set, not appended to the end
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.4.0...v0.4.0

## v0.3.2 (2026-03-05)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.3.2_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.3.2/Sample-Scout_0.3.2_universal.dmg) |
| Windows | [Sample-Scout_0.3.2_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.3.2/Sample-Scout_0.3.2_x64-setup.exe) |
| Linux | [Sample-Scout_0.3.2_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.3.2/Sample-Scout_0.3.2_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- add Legacy WAV export option for classic hardware/software compatibility (Thanks @mylarmelodies!)
### Fixes
- lock bit depth to 16-bit when Legacy WAV is enabled
- write scan_errors.log to app logs directory, bump to 0.3.2

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.3.2...v0.3.2

## v0.3.1 (2026-02-26)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.3.1_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.3.1/Sample-Scout_0.3.1_universal.dmg) |
| Windows | [Sample-Scout_0.3.1_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.3.1/Sample-Scout_0.3.1_x64-setup.exe) |
| Linux | [Sample-Scout_0.3.1_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.3.1/Sample-Scout_0.3.1_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

# v0.3.1

## Fixes
- Migration system overhauled — all schema changes now run in order alongside data changes, fixing a status backfill ordering bug on first launch
- Fixed invalid SQL in scanner upsert that caused BPM values (`bpm_beatthis`, `bpm_acf`) to not save correctly
- Fixed collection ID backfill using the wrong path separator on Windows
- Offline grace period redesigned — tracks when grace started rather than counting from last validation, adds a `GraceExpiredPending` state so returning users can revalidate before being blocked

## Infrastructure
- ONNX Runtime now loaded dynamically from a bundled shared library, enabling universal macOS builds (x86_64 + arm64)

# v0.3.0

## New Features
- **Audio analysis pipeline** — Two-tier BPM and key detection powered by ONNX neural networks, with tag/filename extraction as a fast first pass before deep analysis
- **Always-visible analysis fields** — BPM/key columns with confidence values and informational tooltips
- **Non-destructive sample lifecycle** — Handles missing and orphaned files gracefully instead of deleting records

## Fixes
- DB-driven analysis flags prevent re-analysis and infinite retry loops
- Analysis update events now emit proper COALESCE'd display values
- Re-probe files missing `metadata_version` so filename-derived BPM takes priority
- Tier 2 analysis and live result updates work correctly in the set pane
- Dual analysis flag maps with correct timing and pitch fields on sets
- Fixed missing `SELECT` keyword in `get_set_samples` query
- Analysis tooltips reordered to lead with user-relevant info

## Performance
- Removed DB mutex from worker queue path, restoring lock-free architecture for big performance gains


**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.3.1...v0.3.1

## v0.2.3 (2026-02-25)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.2.3_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.3/Sample-Scout_0.2.3_universal.dmg) |
| Windows | [Sample-Scout_0.2.3_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.3/Sample-Scout_0.2.3_x64-setup.exe) |
| Linux | [Sample-Scout_0.2.3_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.3/Sample-Scout_0.2.3_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- add playback volume control with real-time stereo dB metering
- inline set rename in export dialog (thanks decurus!)

### Fixes
- remove unused volumeToDbString to fix release build

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.2.2...v0.2.3

## v0.2.2 (2026-02-19)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.2.2_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.2/Sample-Scout_0.2.2_universal.dmg) |
| Windows | [Sample-Scout_0.2.2_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.2/Sample-Scout_0.2.2_x64-setup.exe) |
| Linux | [Sample-Scout_0.2.2_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.2/Sample-Scout_0.2.2_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- graceful collection removal with offline sample support
- permanent download links via dl.samplescout.app

### Fixes
- walk up path hierarchy when browse pane shows empty results
- orphaned samples show visual selection without audio playback
- make fade widths absolute instead of clip-relative

### Other
- ui: update view mode tooltip to clarify flat view behavior

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.2.1...v0.2.2

## v0.2.1 (2026-02-19)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.2.1_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.1/Sample-Scout_0.2.1_universal.dmg) |
| Windows | [Sample-Scout_0.2.1_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.1/Sample-Scout_0.2.1_x64-setup.exe) |
| Linux | [Sample-Scout_0.2.1_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.1/Sample-Scout_0.2.1_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.2.2...v0.2.1

## v0.2.0 (2026-02-08)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.2.0_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.0/Sample-Scout_0.2.0_universal.dmg) |
| Windows | [Sample-Scout_0.2.0_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.0/Sample-Scout_0.2.0_x64-setup.exe) |
| Linux | [Sample-Scout_0.2.0_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.0/Sample-Scout_0.2.0_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- auto-updater system with platform-aware update notifications

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.1.0-alpha.15...v0.2.0

## v0.1.0-alpha.15 (2026-02-07)

### Features
- add check for updates with download progress in About tab
- redesign update check flow in About tab
- unify update status styles and add checking state
- Linux update notification in footer and eager font preload

### Fixes
- use arch-specific platform keys and improve update status UI
- add app bundle target for updater signature generation

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.1.0-alpha.14...v0.1.0-alpha.15

## v0.1.0-alpha.14 (2026-02-07)

### Features
- add CHANGELOG.md to public repo, link from Help dialog
- add release infrastructure with auto-update, CI/CD pipelines, and APT repo
- re-encrypt license.dat with new SampleScout salt
- migrate app data directory from sample-manager to sample-scout

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.1.0-alpha.13...v0.1.0-alpha.14
