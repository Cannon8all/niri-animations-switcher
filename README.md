# Setting up Niri Animations & Otter-WM Button

This guide explains how to set up the Niri animations script and integrate it with an Otter-shell button.

## Installation Steps

### 1. File Placement
*   Add the `animations` folder to `~/.config/niri/`
*   Add the `niri-anim-toggle.sh` script to `~/.local/bin/`

### 2. Initialize the Script
Create a symbolic link so the script has a starting point:
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
WARNING:I made this script with the help of a clanker (gemini), this was just for a personal project.
Credits for the animations
https://github.com/jhsuditcher-glitch
https://github.com/jgarza9788 Blur Glitch (01) smoke energize_b tv_crt
https://github.com/XansiVA bloom.kdl burn-ashes.kdl burn-multicolor.kdl burn.kdl fold-window.kdl glitch.kdl pixelate.kdl pop-drop.kdl ribbons.kdl roll-drop.kdl swipe-window.kdl unravel.kdland
