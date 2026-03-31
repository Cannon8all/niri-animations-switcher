# Niri Animation Switcher

A lightweight utility script for the [Niri compositor](https://github.com) that allows you to dynamically cycle through different animation presets. Perfect for users who want to change their desktop's visual flair on the fly using a script or a shell button.

## 🚀 Features
*   **Automatic Cycling**: Rotates through all `.kdl` files in your animations folder.
*   **Visual Feedback**: Sends a system notification showing the name of the active animation.
*   **Easy Integration**: Designed to work seamlessly with **Otter-Shell** or via keybindings.

## 🛠️ Installation & Setup

### 1. Place the Files
Ensure the files are in the correct directories:
*   Move the `animations/` folder to `~/.config/niri/`
*   Move the `niri-anim-toggle.sh` script to `~/.local/bin/`

### 2. Configure Permissions & Symlink
Make the script executable and create an initial symbolic link so the script has a starting point:

### 3. Make the script executable
chmod +x ~/.local/bin/niri-anim-toggle.sh

### 4. Create the initial link (one-time setup)
ln -s ~/.config/niri/animations/pop-drop.kdl ~/.config/niri/animations/current_animation.kdl

### 5. Edit Niri Configuration
Open your `~/.config/niri/config.kdl` file. Remove your existing `animations { ... }` section and replace it with this include line:

```kdl
include "animations/current_animation.kdl"
