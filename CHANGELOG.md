## v1.0.9 (2026-05-15)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_1.0.9_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.9/Sample-Scout_1.0.9_universal.dmg) |
| Windows | [Sample-Scout_1.0.9_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.9/Sample-Scout_1.0.9_x64-setup.exe) |
| Linux | [Sample-Scout_1.0.9_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.9/Sample-Scout_1.0.9_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*


### Stability

- Adjusted stack management and queueing to address an edge case that could crash the app during library scanning on Windows, and hardened several audio worker-thread paths in the process.
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v1.0.8...v1.0.9

## v1.0.8 (2026-05-10)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_1.0.8_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.8/Sample-Scout_1.0.8_universal.dmg) |
| Windows | [Sample-Scout_1.0.8_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.8/Sample-Scout_1.0.8_x64-setup.exe) |
| Linux | [Sample-Scout_1.0.8_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.8/Sample-Scout_1.0.8_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*


### Audio Engine

- Fixed an edge case with multi-output audio interfaces (Expert Sleepers ES-9, MOTU, RME, etc.) — stereo playback now routes cleanly to outputs 1/2. Built-in speakers and stereo interfaces were unaffected.
- macOS no longer prompts for microphone permission on launch. This was a bug in an upstream audio library — not in Sample Scout itself — and has been resolved. The app has never recorded or used the microphone.
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v1.0.7...v1.0.8

## v1.0.7 (2026-05-02)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_1.0.7_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.7/Sample-Scout_1.0.7_universal.dmg) |
| Windows | [Sample-Scout_1.0.7_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.7/Sample-Scout_1.0.7_x64-setup.exe) |
| Linux | [Sample-Scout_1.0.7_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.7/Sample-Scout_1.0.7_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*


### Keyboard Navigation

- Pressing `V` to toggle between folder and flat view now works correctly. Previously, the keyboard shortcut updated the toggle state but didn't reload the file listing — only the header button worked. Both now behave identically.
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v1.0.6...v1.0.7

## v1.0.6 (2026-04-15)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_1.0.6_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.6/Sample-Scout_1.0.6_universal.dmg) |
| Windows | [Sample-Scout_1.0.6_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.6/Sample-Scout_1.0.6_x64-setup.exe) |
| Linux | [Sample-Scout_1.0.6_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.6/Sample-Scout_1.0.6_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*


**Sets & Collections**

- Sets are now browsable! Open any set to navigate its contents just like a folder.
- New Browse Set option is accessible as a new folder item on the Select Set dialog.
- New Category switcher is a dropdown on the folder icon in the breadcrumb header allowing you to quickly choose browsing sets or collections.
- New context menu item for Browse Set on the set membership badges in the detail pane.
- Browse, rename, and delete buttons in the set select dialog now show tooltips.

**UI Polish**

- Empty state messages now appear in folders, sets, and collections with no items.
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v1.0.5...v1.0.6

## v1.0.5 (2026-04-01)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_1.0.5_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.5/Sample-Scout_1.0.5_universal.dmg) |
| Windows | [Sample-Scout_1.0.5_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.5/Sample-Scout_1.0.5_x64-setup.exe) |
| Linux | [Sample-Scout_1.0.5_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.5/Sample-Scout_1.0.5_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

# Draft Patch Notes — v1.0.5

Previous release: v1.0.4

### Features
- license modal redesign and onboarding improvements
- tutorial polish — animation overrides, dialog steps, and styling
- tutorial script refinements and engine hardening
- step exit animation with fade-out and pause
- tutorial animations, styling, and pacing improvements
- getting started tutorial script
- auto-polling completion checks for DOM state changes
- dual key notifications, intercept keys, and case-sensitive matching
- add tutorial walkthrough engine
- add onboarding dialog for first-run collection setup

### Fixes
- progressive waveform rendering stalled on long files
- step 2 callout position — use ratio 0 to align with highlight top
- overlay click handling and callout styling
- separate control/data channels and reliable scan cancellation

### Other
- ui: tutorial script and dialog polish
- ui: polish license modal and success animation
- add test tutorial script and data-tutorial attributes
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v1.0.4...v1.0.5

## v1.0.4 (2026-03-22)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_1.0.4_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.4/Sample-Scout_1.0.4_universal.dmg) |
| Windows | [Sample-Scout_1.0.4_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.4/Sample-Scout_1.0.4_x64-setup.exe) |
| Linux | [Sample-Scout_1.0.4_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.4/Sample-Scout_1.0.4_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*


**Features**
- editor waveform reflects fade amplitude with column-slice squeeze
- ui: refine shortcut hints and tooltip content for better clarity

**Fixes**
- exclude offline files from search results
- always apply fade-in regardless of playback start position
- clamp fade widths to clip duration at rendering boundaries
- release notes generation and workflow ingestion
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v1.0.3...v1.0.4

## v1.0.3 (2026-03-20)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_1.0.3_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.3/Sample-Scout_1.0.3_universal.dmg) |
| Windows | [Sample-Scout_1.0.3_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.3/Sample-Scout_1.0.3_x64-setup.exe) |
| Linux | [Sample-Scout_1.0.3_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.3/Sample-Scout_1.0.3_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*


**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v1.0.2...v1.0.3

## v1.0.2 (2026-03-19)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_1.0.2_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.2/Sample-Scout_1.0.2_universal.dmg) |
| Windows | [Sample-Scout_1.0.2_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.2/Sample-Scout_1.0.2_x64-setup.exe) |
| Linux | [Sample-Scout_1.0.2_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.2/Sample-Scout_1.0.2_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*


**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v1.0.1...v1.0.2

## v1.0.1 (2026-03-18)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_1.0.1_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.1/Sample-Scout_1.0.1_universal.dmg) |
| Windows | [Sample-Scout_1.0.1_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.1/Sample-Scout_1.0.1_x64-setup.exe) |
| Linux | [Sample-Scout_1.0.1_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.1/Sample-Scout_1.0.1_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- D key toggles playback when selected sample matches playing sample

### Fixes
- eliminate playback indicator racing and duration flicker on sample start
- remove autoFocus on export path input and handle Escape properly

### Other
- ui: reorganize and clean up help dialog shortcuts
**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v1.0.0...v1.0.1

## v1.0.0 (2026-03-16)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_1.0.0_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.0/Sample-Scout_1.0.0_universal.dmg) |
| Windows | [Sample-Scout_1.0.0_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.0/Sample-Scout_1.0.0_x64-setup.exe) |
| Linux | [Sample-Scout_1.0.0_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.0/Sample-Scout_1.0.0_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Introduction

A keyboard-first sample audition tool built for speed. Browse, audition, clip, and export — without leaving the keyboard.

### Browse

- Keyboard-driven file browser — arrow keys fly through your library with instant audio preview on every selection
- Autoplay mode (`P`) lets every navigation instantly play — hold down-arrow to audition 10-20 samples per second
- Point at any collection: multi-million file libraries, external drives, network storage
- Search by filename, filter by folder, or use `tag:name` syntax to search by tag
- BPM and key detection — fast extraction from tags and filenames, with neural network deep analysis as a second pass
- Detail pane shows waveform preview, metadata, notes, tags, and file info at a glance

### Sets

- Press `E` to add any sample to your set — no stopping, no context switching
- Multi-select with Shift+Click and Ctrl+Click — bulk add, remove, and drag
- Delete history with preview and one-click restore
- Build sets while browsing, export when ready

### Editor

- Inline waveform editor — clip regions by dragging directly on the waveform
- Clips are non-destructive metadata regions linked to source audio — no disk space wasted while you experiment
- Drag fade handles with custom curves and immediate audio feedback
- Loop selections to audition your work before committing
- Click-to-seek, scroll-to-zoom, drag-to-pan — mouse-driven precision where it matters
- Clip badge dropdown for quick access to all clips on a sample — recall, rename, or delete

### Export

- Full DSP chain: bit depth conversion, TPDF dithering, mono downmix, normalization, and limiting
- Export presets with persistent settings across sessions
- Legacy WAV mode for classic hardware and software compatibility
- Drag and drop samples straight into your DAW — clips render on demand
- Manifest file documents exactly what processing was applied

### General

- Help overlay (`?`) with full keyboard shortcut reference
- Auto-updater with download progress on macOS and Windows; update notifications on Linux

### Platform Support

- macOS (Intel & Apple Silicon) — macOS 12 Monterey or later
- Windows 10+ (64-bit)
- Linux (Debian/Ubuntu .deb) — Ubuntu 22.04+, Debian 12+
- APT repository for automatic updates on Linux
