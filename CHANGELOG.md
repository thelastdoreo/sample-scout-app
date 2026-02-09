## v0.2.1 (2026-02-09)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.2.1_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.1/Sample-Scout_0.2.1_universal.dmg) |
| Windows | [Sample-Scout_0.2.1_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.1/Sample-Scout_0.2.1_x64-setup.exe) |
| Linux | [Sample-Scout_0.2.1_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.2.1/Sample-Scout_0.2.1_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- progressive folder updates during library scanning

### Fixes
- prevent white flash during startup
- tag library click not registering when filter text is active
- consolidate log directory under sample-scout data path

### Other
- unify startup scan events with regular scan conventions

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.2.0...v0.2.1

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
