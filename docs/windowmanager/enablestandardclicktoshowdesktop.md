---
title: Enable standard click to show desktop | Window Manager
description: Enable or disable showing the desktop when clicked outside Stage Manager
head:
  - - meta
    - property: 'og:title'
      content: macOS defaults > Window Manager > Enable standard click to show desktop
  - - meta
    - property: 'og:description'
      content: Enable or disable showing the desktop when clicked outside Stage Manager
---

# Enable standard click to show desktop

Enable or disable showing the desktop when clicked outside Stage Manager

<!-- break lists -->

- **Tested on macOS**:
  - Sonoma
- **Parameter type**: int

## Set to `0`

Enable showing the desktop when clicked only in Stage Manager

```bash
defaults write com.apple.WindowManager "EnableStandardClickToShowDesktop" 0
```

<!-- TODO: change image -->
<img
  src="./images/tilesize/36.png"
  alt="Example output with value set to 36"
  width="740" height="463" style="height: auto"
/>

## Set to `1` (default value)

Enable showing the desktop outside of Stage Manager 

```bash
defaults write com.apple.WindowManager "EnableStandardClickToShowDesktop" 1
```

<!-- TODO: change image -->
<img
  src="./images/tilesize/48.png"
  alt="Example output with value set to 48"
  width="740" height="463" style="height: auto"
/>

## Read current value

```bash
defaults read com.apple.dock "tilesize"
```

## Reset to default value

```bash
defaults delete com.apple.dock "tilesize" && killall Dock
```

## Set value from UI

1. <a href="x-apple.systempreferences:com.apple.preference.dock?Dock">Access Dock settings from macOS UI</a>
2. Slide "Size" range value
