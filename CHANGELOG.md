## v1.1.0 (2026-06-09)


**Shuffle Sample Order** 
- New button in header allows randomizing the browser pane order.
- Scoped to what is currently visible in the browser pane so you can randomize the order of a single folder, a search, or your entire library flattened!
**Re-sort any view**
- Order either view pane by name, size, or audible clip length from the right-click menu.
**On-disk file management**
- Rename or delete files and folders on disk directly from the browser pane
- Delete moves to Trash.
**Post-export command**
- Run a custom shell command or script from the export directory after export completes.
- This can be used to run conversion scripts or other post-processing tasks.

**Fixes**
- **Export filenames** — OS-illegal characters are sanitized on export avoiding issues with file system operations. Export completes with mild warning for information purposes.
- **BPM & Key detection** — fixed an issue with BPM and key detection for files 15 seconds and longer.
- **WAV playback** — fixed an issue with playback of files whose RIFF header omits injected metadata chunks.
- **Clean loop playback** — fixed an issue with loops where sometimes silence appeared at loop ends due to chunk boundaries.
- **Select-all** — Cmd/Ctrl+A works as intended to select files in browser view without highlighting the interface.
- **Adjusted sorting** — browse, search, and flat view sorting adjusted to sort by name by default.
- **Collection counts** — revamped of display of orphaned and offline samples to better reflect intended state.
- **Volume fader** — popup now dismisses consistently when a drag releases outside it.

## v1.0.12 (2026-05-23)

**Features**
- Customizable keyboard shortcuts. Edit keybindings.jsonc in the app data folder; tooltips, footer hints, the help dialog, and the tutorial all reflect the live keymap.
- Status bar flags storage trouble when playback stalls past 10 seconds.

**Fixes**
- Library count reflects accessible samples — offline and orphaned files are no longer counted.
- Library scanning rebuilt for stability on large folders, with a dedicated 8MB scan thread and a flat work pipeline.
- Saved clips display their actual length, not the parent sample's duration.
- Sets handle multiple clips of the same source file as independent entries.
- Keybindings parse errors surface with per-line detail; the keybindings folder reveals reliably across platforms.

## v1.0.11 (2026-05-17)

**Fixes**
- Update Clip button now reliably clears the "modified" highlight after saving.

## v1.0.10 (2026-05-17)

**Clip Dragging**

- Feat: The clip region can now be moved as a unit. A title bar runs along the top of the clip — dragging it moves the entire clip region along the timeline maintaining the timing. 

**Search**

- Feat: Multi-word queries match each term independently. Typing "deep house kick" surfaces samples containing all three words in any order.
- Fix: The search box releases its selection on blur, keeping global shortcuts responsive after leaving the field.
- Fix: F focuses the search bar even when the waveform editor is open. Also fixed the issue with the search box not losing focus properly when opening the waveform editor.

## v1.0.9 (2026-05-15)

**Stability**

- Adjusted stack management and queueing to address an edge case that could crash the app during library scanning on Windows, and hardened several audio worker-thread paths in the process.

## v1.0.8 (2026-05-10)

**Audio Engine**

- Fixed an edge case with multi-output audio interfaces (Expert Sleepers ES-9, MOTU, RME, etc.) — stereo playback now routes cleanly to outputs 1/2. Built-in speakers and stereo interfaces were unaffected.
- macOS no longer prompts for microphone permission on launch. This was a bug in an upstream audio library — not in Sample Scout itself — and has been resolved. The app has never recorded or used the microphone.

## v1.0.7 (2026-05-02)

**Keyboard Navigation**

- Pressing `V` to toggle between folder and flat view now works correctly. Previously, the keyboard shortcut updated the toggle state but didn't reload the file listing — only the header button worked. Both now behave identically.

## v1.0.6 (2026-04-15)

**Sets & Collections**

- Sets are now browsable! Open any set to navigate its contents just like a folder.
- New Browse Set option is accessible as a new folder item on the Select Set dialog.
- New Category switcher is a dropdown on the folder icon in the breadcrumb header allowing you to quickly choose browsing sets or collections.
- New context menu item for Browse Set on the set membership badges in the detail pane.
- Browse, rename, and delete buttons in the set select dialog now show tooltips.

**UI Polish**

- Empty state messages now appear in folders, sets, and collections with no items.

## v1.0.5 (2026-04-01)

**Features**
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

**Fixes**
- progressive waveform rendering stalled on long files
- step 2 callout position — use ratio 0 to align with highlight top
- overlay click handling and callout styling
- separate control/data channels and reliable scan cancellation

**Other**
- ui: tutorial script and dialog polish
- ui: polish license modal and success animation
- add test tutorial script and data-tutorial attributes

## v1.0.4 (2026-03-22)

**Features**
- editor waveform reflects fade amplitude with column-slice squeeze
- ui: refine shortcut hints and tooltip content for better clarity

**Fixes**
- exclude offline files from search results
- always apply fade-in regardless of playback start position
- clamp fade widths to clip duration at rendering boundaries
- release notes generation and workflow ingestion

## v1.0.1 (2026-03-18)

**Features**
- D key toggles playback when selected sample matches playing sample

**Fixes**
- eliminate playback indicator racing and duration flicker on sample start
- remove autoFocus on export path input and handle Escape properly

**Other**
- ui: reorganize and clean up help dialog shortcuts

## v1.0.0 (2026-03-16)

**Introduction**

A keyboard-first sample audition tool built for speed. Browse, audition, clip, and export — without leaving the keyboard.

**Browse**

- Keyboard-driven file browser — arrow keys fly through your library with instant audio preview on every selection
- Autoplay mode (`P`) lets every navigation instantly play — hold down-arrow to audition 10-20 samples per second
- Point at any collection: multi-million file libraries, external drives, network storage
- Search by filename, filter by folder, or use `tag:name` syntax to search by tag
- BPM and key detection — fast extraction from tags and filenames, with neural network deep analysis as a second pass
- Detail pane shows waveform preview, metadata, notes, tags, and file info at a glance

**Sets**

- Press `E` to add any sample to your set — no stopping, no context switching
- Multi-select with Shift+Click and Ctrl+Click — bulk add, remove, and drag
- Delete history with preview and one-click restore
- Build sets while browsing, export when ready

**Editor**

- Inline waveform editor — clip regions by dragging directly on the waveform
- Clips are non-destructive metadata regions linked to source audio — no disk space wasted while you experiment
- Drag fade handles with custom curves and immediate audio feedback
- Loop selections to audition your work before committing
- Click-to-seek, scroll-to-zoom, drag-to-pan — mouse-driven precision where it matters
- Clip badge dropdown for quick access to all clips on a sample — recall, rename, or delete

**Export**

- Full DSP chain: bit depth conversion, TPDF dithering, mono downmix, normalization, and limiting
- Export presets with persistent settings across sessions
- Legacy WAV mode for classic hardware and software compatibility
- Drag and drop samples straight into your DAW — clips render on demand
- Manifest file documents exactly what processing was applied

**General**

- Help overlay (`?`) with full keyboard shortcut reference
- Auto-updater with download progress on macOS and Windows; update notifications on Linux

**Platform Support**

- macOS (Intel & Apple Silicon) — macOS 12 Monterey or later
- Windows 10+ (64-bit)
- Linux (Debian/Ubuntu .deb) — Ubuntu 22.04+, Debian 12+
- APT repository for automatic updates on Linux
