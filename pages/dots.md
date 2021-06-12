---
title: /dots
layout: page
permalink: /dots
---

# my mac setup

### directories

### Turn Off System Integrity Protection (SIP)
1. Restart computer.
2. Hold down `Command-R` to reboot into Recovery Mode.
3. In the menu bar, choose `Utilities`, then `Terminal`
4. Run:
```bash
# If you're on macOS 10.14 and above
# (printed warning can be safely ignored)
csrutil enable --without debug --without fs

# If you're on macOS 10.13
# (disables SIP completely)
csrutil disable
```
5. Restart computer.
6. Check that SIP was disabled: `$ csrutil status`

### Homebrew

### iTerm 2 - Terminal

### fish - shell

### Python

### font

### Pecan - Menubar

### [Yabai](https://github.com/koekeishiya/yabai) - Tiling Windows Manager

#### System Preferences
| Category | Options |
| -------- | ------- |
| Mission Control  | on - Displays have separate Spaces </br> off - Automatically rearrange Spaces based on most recent use |
