# Setting up Niri Animations & Otter-WM Button

This guide explains how to set up the Niri animations script and integrate it with an Otter-shell button.

## Installation Steps

### 1. File Placement
*   Add the `animations` folder to `~/.config/niri/`
*   Add the `niri-anim-toggle.sh` script to `~/.local/bin/`

### 2. Initialize the Script
Create a symbolic link so the script has a starting point:
```bash
ln -s ~/.config/niri/animations/pop-drop.kdl ~/.config/niri/animations/current_animation.kdl

### Step 3: Permissions & Configuration

To make the script work and integrate it into your Niri setup, follow these steps:

1. **Make the script executable:**
   Run the following command in your terminal:
   ```bash
   chmod +x ~/.local/bin/niri-anim-toggle.sh


Edit your niri config.kdl, remove the animation section and add in its place
include "animations/current_animation.kdl"
Add a button in otter-shell
Button animation command: niri-anim-toggle.sh
!! Logout and back in !!

## Credits & Disclaimer

> [!CAUTION]
> This script was created with the help of a clanker for a personal project. Use at your own risk.

### Animation Sources:

*   [jhsuditcher-glitch](https://github.com)
*   [jgarza9788](https://github.com): *Blur, Glitch (01), smoke, energize_b, tv_crt*
*   [XansiVA](https://github.com): *bloom, burn-ashes, burn-multicolor, burn, fold-window, glitch, pixelate, pop-drop, ribbons, roll-drop, swipe-window, unravel*
