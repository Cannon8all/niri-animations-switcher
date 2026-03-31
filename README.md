# Niri Animation Switcher

A handy script to dynamically toggle between different animation presets in the Niri compositor. Change your desktop's visual style with a single click (via Otter-Shell) or a keyboard shortcut.

## 🌟 Features

*   **Automatic Cycling:** Cycles through all `.kdl` files in your animations folder.
*   **System Notifications:** Sends a notification with the name of the active animation.
*   **Simple Integration:** Easy to use with Otter-Shell or custom keybindings.

## 🛠️ Installation

### 1. Place the files
Clone this repository or download the files manually:
*   Place the `animations/` folder in `~/.config/niri/`.
*   Place the script `niri-anim-toggle.sh` in `~/.local/bin/`.

### 2. Set up the script
Make the script executable and create the initial symlink to give the script a starting point:

ln -s ~/.config/niri/animations/pop-drop.kdl ~/.config/niri/animations/current_animation.kdl
```bash
# Make executable
*    `chmod +x ~/.local/bin/niri-anim-toggle.sh`

# Create the first link (required once)
*    `ln -s ~/.config/niri/animations/pop-drop.kdl ~/.config/niri/animations/current_animation.kdl`

3. Niri Configuration
Open your ~/.config/niri/config.kdl. Remove the existing animations { ... } section and replace it with the following line:

*    include "animations/current_animation.kdl"

4. Otter-Shell Integration
Add a button to your Otter-Shell configuration with the following command:

    Command: niri-anim-toggle.sh

    [!IMPORTANT]
    Log out and back in (or restart Niri) to activate the changes.

📜 Credits
The animations in this project come from the following creators:

    jhsu: ditcher-glitch
    jgarza9788: Blur Glitch (01), smoke, energize_b, tv_crt
    XansiVA: bloom, burn-ashes, burn-multicolor, burn, fold-window, glitch, pixelate, pop-drop, ribbons, roll-drop, swipe-window, unravel
