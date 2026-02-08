## v0.1.0-alpha.15 (2026-02-07)

### Download

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.1.0-alpha.15_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.15/Sample-Scout_0.1.0-alpha.15_universal.dmg) |
| Windows | [Sample-Scout_0.1.0-alpha.15_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.15/Sample-Scout_0.1.0-alpha.15_x64-setup.exe) |
| Linux | [Sample-Scout_0.1.0-alpha.15_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.15/Sample-Scout_0.1.0-alpha.15_amd64.deb) |

*Other files listed below are for the auto-updater and can be ignored.*

### Features
- add check for updates with download progress in About tab
- Linux update notification in footer and eager font preload
- redesign update check flow in About tab
- unify update status styles and add checking state

### Fixes
- use arch-specific platform keys and improve update status UI
- enable updater artifact generation
- add app bundle target for updater signature generation
- remove pending artifact delete step
- sanitize inputs and fix release notes tag matching
- include updater bundles in artifact uploads
- checkout build commit SHA in release workflow
- make release creation idempotent for re-runs
- rewrite README sync to avoid heredoc YAML parsing error
- move BASE_URL to env block for Python access

### Other
- separate private/public READMEs
- add download guide with direct links to release notes
- sync README to public repo with download links on release
- add .env to gitignore and update tauri-cli to 2.10.0
- clean up release workflow summary

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.1.0-alpha.14...v0.1.0-alpha.15

## v0.1.0-alpha.14 (2026-02-07)

### Features
- add release infrastructure with auto-update, CI/CD pipelines, and APT repo
- add Windows and Linux build workflows
- add CHANGELOG.md to public repo, link from Help dialog
- auto-generate release notes from conventional commits
- delete pending artifact after stapling notarized DMG
- re-encrypt license.dat with new SampleScout salt
- migrate app data directory from sample-manager to sample-scout

### Fixes
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
- rename app to Sample Scout for Apple submission
- rename SampleManager component and references to SampleScout
- update Tauri crates and npm packages to 2.10.x
- decouple all-release from builds, standardize workflow names

**Full changelog**: https://github.com/thelastdoreo/sample-scout-app/compare/v0.1.0-alpha.13...v0.1.0-alpha.14
