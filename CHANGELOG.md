## v0.1.0-alpha.15 (2026-02-08)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.1.0-alpha.15_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.15/Sample-Scout_0.1.0-alpha.15_universal.dmg) |
| Windows | [Sample-Scout_0.1.0-alpha.15_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.15/Sample-Scout_0.1.0-alpha.15_x64-setup.exe) |
| Linux | [Sample-Scout_0.1.0-alpha.15_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.15/Sample-Scout_0.1.0-alpha.15_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- Linux update notification in footer and eager font preload
- unify update status styles and add checking state
- redesign update check flow in About tab
- add check for updates with download progress in About tab
- sync README to public repo with download links on release
- add download guide with direct links to release notes
- add build output listing for debugging updater artifacts

### Fixes
- use arch-specific platform keys and improve update status UI
- move BASE_URL to env block for Python access
- rewrite README sync to avoid heredoc YAML parsing error
- remove pending artifact delete step
- add app bundle target for updater signature generation
- enable updater artifact generation
- sanitize inputs and fix release notes tag matching
- include updater bundles in artifact uploads
- checkout build commit SHA in release workflow
- make release creation idempotent for re-runs

### Other
- bump version to 0.1.0-alpha.15
- separate private/public READMEs
- add .env to gitignore and update tauri-cli to 2.10.0
- update Cargo.lock for alpha.14 version bump

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.1.0-alpha.14...v0.1.0-alpha.15

## v0.1.0-alpha.14 (2026-02-07)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.1.0-alpha.14_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.14/Sample-Scout_0.1.0-alpha.14_universal.dmg) |
| Windows | [Sample-Scout_0.1.0-alpha.14_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.14/Sample-Scout_0.1.0-alpha.14_x64-setup.exe) |
| Linux | [Sample-Scout_0.1.0-alpha.14_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.14/Sample-Scout_0.1.0-alpha.14_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- add build output listing for debugging updater artifacts
- add CHANGELOG.md to public repo, link from Help dialog
- auto-generate release notes from conventional commits
- delete pending artifact after stapling notarized DMG
- add release infrastructure with auto-update, CI/CD pipelines, and APT repo
- re-encrypt license.dat with new SampleScout salt
- migrate app data directory from sample-manager to sample-scout
- add Windows and Linux build workflows, add Rust caching
- add Windows and Linux build workflows

### Fixes
- remove pending artifact delete step
- add app bundle target for updater signature generation
- enable updater artifact generation
- sanitize inputs and fix release notes tag matching
- include updater bundles in artifact uploads
- checkout build commit SHA in release workflow
- make release creation idempotent for re-runs
- base64 decode GPG key in release workflow
- add actions:read permission to all-release workflow
- prevent pending artifacts from reaching public release
- conditional artifact download in poll-notarization
- use input check instead of event_name in poll-notarization
- remove permissions block from mac-poll-notarization
- move permissions to job level in mac-poll-notarization
- rename secret to SUBMODULE_PAT
- rename secret to ASSETS_SUBMODULE_PAT
- use PAT for private submodule checkout
- rename installer files to use hyphens, fix package name

### Other
- add .env to gitignore and update tauri-cli to 2.10.0
- update Cargo.lock for alpha.14 version bump
- bump version to 0.1.0-alpha.14
- decouple all-release from builds, standardize workflow names
- update Tauri crates and npm packages to 2.10.x
- update package-lock.json for sample-scout rename
- rename SampleManager component and references to SampleScout
- rename app to Sample Scout for Apple submission

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.1.0-alpha.13...v0.1.0-alpha.14

## v0.1.0-alpha.14 (2026-02-07)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.1.0-alpha.14_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.14/Sample-Scout_0.1.0-alpha.14_universal.dmg) |
| Windows | [Sample-Scout_0.1.0-alpha.14_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.14/Sample-Scout_0.1.0-alpha.14_x64-setup.exe) |
| Linux | [Sample-Scout_0.1.0-alpha.14_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.14/Sample-Scout_0.1.0-alpha.14_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- add build output listing for debugging updater artifacts
- add CHANGELOG.md to public repo, link from Help dialog
- auto-generate release notes from conventional commits
- delete pending artifact after stapling notarized DMG
- add release infrastructure with auto-update, CI/CD pipelines, and APT repo
- re-encrypt license.dat with new SampleScout salt
- migrate app data directory from sample-manager to sample-scout
- add Windows and Linux build workflows, add Rust caching
- add Windows and Linux build workflows

### Fixes
- remove pending artifact delete step
- add app bundle target for updater signature generation
- enable updater artifact generation
- sanitize inputs and fix release notes tag matching
- include updater bundles in artifact uploads
- checkout build commit SHA in release workflow
- make release creation idempotent for re-runs
- base64 decode GPG key in release workflow
- add actions:read permission to all-release workflow
- prevent pending artifacts from reaching public release
- conditional artifact download in poll-notarization
- use input check instead of event_name in poll-notarization
- remove permissions block from mac-poll-notarization
- move permissions to job level in mac-poll-notarization
- rename secret to SUBMODULE_PAT
- rename secret to ASSETS_SUBMODULE_PAT
- use PAT for private submodule checkout
- rename installer files to use hyphens, fix package name

### Other
- add .env to gitignore and update tauri-cli to 2.10.0
- update Cargo.lock for alpha.14 version bump
- bump version to 0.1.0-alpha.14
- decouple all-release from builds, standardize workflow names
- update Tauri crates and npm packages to 2.10.x
- update package-lock.json for sample-scout rename
- rename SampleManager component and references to SampleScout
- rename app to Sample Scout for Apple submission

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.1.0-alpha.13...v0.1.0-alpha.14
