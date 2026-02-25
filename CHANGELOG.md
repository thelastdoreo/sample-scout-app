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
