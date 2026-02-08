# Sample Scout

A keyboard-first sample audition tool for music producers. Rapidly browse and audition your sample library using keyboard shortcuts.

<!-- DOWNLOADS_START -->
## Download v0.1.0-alpha.15

| Platform | Installer |
|----------|-----------|
| macOS | [Sample-Scout_0.1.0-alpha.15_universal.dmg](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.15/Sample-Scout_0.1.0-alpha.15_universal.dmg) |
| Windows | [Sample-Scout_0.1.0-alpha.15_x64-setup.exe](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.15/Sample-Scout_0.1.0-alpha.15_x64-setup.exe) |
| Linux | [Sample-Scout_0.1.0-alpha.15_amd64.deb](https://github.com/thelastdoreo/sample-scout-app/releases/download/v0.1.0-alpha.15/Sample-Scout_0.1.0-alpha.15_amd64.deb) |
<!-- DOWNLOADS_END -->

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `↑/↓` Arrow keys | Navigate up/down |
| `Enter` | Enter folder |
| `Backspace` | Go up one level |
| `Tab` | Switch panes |
| `Home/End` | Jump to top/bottom |
| `Space` | Play/Pause |
| `←/→` Arrow keys | Seek -/+ 10 seconds |
| `p` | Toggle autoplay |
| `v` | Toggle folder/flat view |
| `a` | Add to active set |
| `d` | Remove from set |
| `n` | New set |
| `s` | Switch active set |
| `i` | Toggle info panel |

## Linux APT Repository

```bash
# Add the GPG key
curl -fsSL https://releases.samplescout.app/apt/gpg-key.asc | sudo gpg --dearmor -o /usr/share/keyrings/sample-scout.gpg

# Add the repository
echo "deb [signed-by=/usr/share/keyrings/sample-scout.gpg] https://releases.samplescout.app/apt stable main" | sudo tee /etc/apt/sources.list.d/sample-scout.list

# Install
sudo apt update
sudo apt install sample-scout
```

## Links

- [Changelog](https://releases.samplescout.app/CHANGELOG.md)
- [All Releases](https://github.com/thelastdoreo/sample-scout-app/releases)
