## v0.4.0 (2026-03-07)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.4.0_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.0/Sample-Scout_0.4.0_universal.dmg) |
| Windows | [Sample-Scout_0.4.0_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.0/Sample-Scout_0.4.0_x64-setup.exe) |
| Linux | [Sample-Scout_0.4.0_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.4.0/Sample-Scout_0.4.0_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

Previous release: v0.3.2

### Features
- add Legacy WAV export option for classic hardware/software compatibility (Thanks @mylarmelodies!)
- resizable editor panel with drag handle
- scrollbar zoom, panel exclusivity, footer button consistency
- disambiguate clip identity — memberId-based highlights, editor clip management
- auto-zoom editor viewport to frame clip region on load
- editor visual overhaul — corner frames, overlay blend modes, glow enhancements
- marker-based loop stop, DRY cpal callback helper
- editor playback with live state, looping, and position tracking
- layered caching pipeline, fade rendering + interaction
- clips badge with registry dropdown, wire delete button
- clip-aware preload system with member_id cache keys
- wire clip extraction to sets (E and Shift+E)
- wire editor keyboard actions (nudge, jump, landmark, delete)
- wire editor toolbar, shared transport buttons, loop state
- pointer-events passthrough, coordinate-based edge detection, hover highlight
- interaction hooks, clip overlay, and play cursor tracking
- editor overlay components — play cursor, playback indicator, clip region
- editor zoom/pan with wheel, drag, and keyboard support
- waveform fill+stroke with offscreen compositing
- waveform envelope rendering with screen blend mode
- EditorWaveform LCD background with effects, noise, and ticks
- EditorPanel layout, editor state, and keyboard wiring
- regression testing baseline — 21 new tests, fix clip name bug
- clip export pipeline with trim, fade, and per-item decision tree
- frontend member_id migration, DRY membership tracking
- clip CRUD commands, member_id universal identity, evolve set operations
- add editor keyboard context with browserOpen/editorOpen state conditions
- bounded playback with clip bounds and fade curves
- add clips schema, evolve SetSample to Clip type, duration to number

### Fixes
- reduce editor zoom sensitivity and fix fade fill scaling on vertical resize
- move blend modes from CSS to canvas compositing for macOS WebKit
- add missing ContinuousTimecode component
- remove duplicate cherry-picked export code, integrate legacy WAV into export.rs
- lock bit depth to 16-bit when Legacy WAV is enabled
- write scan_errors.log to app logs directory, bump to 0.3.2
- update editor panel footer hints, tooltips, and clip badge hover
- add 10px threshold before scrollbar Y-axis zoom activates
- clip recall restores region without viewport reset, rename syncs set pane
- smooth editor playback indicator and prevent overflow scrollbar
- prevent tooltip visibility changes from re-rendering all consumers
- reject empty rename input and add volume control to editor
- editor tooltips and inline clip rename
- use memberId for set removal to correctly handle clips
- position ring eliminates cross-thread race in loop playback
- pause before seek in toggleLoop to prevent auto-restart
- decouple loop stop from reached_eof, declarative toggleLoop(reset)
- seekTo source of truth, editor cursor playback, fade opacity
- fade handle polish — hit testing, hover states, visual tuning
- clip auto-naming uses filename and max number
- clip name in sets + streaming playback start from clip position
- restore deleted samples at original position, not end of set
- membership map lookups use member_id format, DetailPanel takes playingMemberId

### Other
- editor tuning — remove playback smoothing, lower scroll zoom, select-none waveform
- editor visual tuning — scrollbar, toolbar, footer consistency
- add color palette mockup
- memoize RowContent to prevent hover flash on play/stop
- isolate isCurrentlyPlaying from SampleScout render cycle
- isolate playback position and levels from SampleScout render cycle
- default editor height to 50%
- editor visual tuning — clip fill, corners, cursor, background
- restore per-element overlay architecture, 9-slice base layer
- persistent sprite canvases, fade fill sprite caching
- pre-composite static layer, eliminate hot-path redraws during fade drags
- noise tile optimization, time ruler, static layer split
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.3.2...v0.4.0

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
