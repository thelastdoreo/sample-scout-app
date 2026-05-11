# Sample Scout

A keyboard-first sample audition tool for music producers. Rapidly browse and audition your sample library using keyboard shortcuts.

<!-- DOWNLOADS_START -->
## Download v1.0.8

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_1.0.8_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.8/Sample-Scout_1.0.8_universal.dmg) |
| Windows | [Sample-Scout_1.0.8_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.8/Sample-Scout_1.0.8_x64-setup.exe) |
| Linux | [Sample-Scout_1.0.8_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v1.0.8/Sample-Scout_1.0.8_amd64.deb) |
<!-- DOWNLOADS_END -->

## Linux APT Repository

```bash
# Add the GPG key
curl -fsSL https://dl.samplescout.app/apt/gpg-key.asc | sudo gpg --dearmor -o /usr/share/keyrings/sample-scout.gpg

# Add the repository
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/sample-scout.gpg] https://dl.samplescout.app/apt stable main" | sudo tee /etc/apt/sources.list.d/sample-scout.list

# Install
sudo apt update && sudo apt install sample-scout
```

## Links

- [Changelog](https://dl.samplescout.app/CHANGELOG.md)
- [All Releases](https://github.com/thelastdoreo/sample-scout-app/releases)
