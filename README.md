# Niri Animation Switcher 🎬

A lightweight Bash script to toggle between different animation profiles (`.kdl` files) for the **Niri compositor**. The script rotates through all available animation files in your configuration directory and updates a symbolic link that Niri can source dynamically.

## ✨ Features
* **Sequential Rotation**: Automatically cycles through all `.kdl` files found in your animations folder.
* **Smart Notifications**: Sends a desktop notification using `notify-send` with the name of the newly activated animation.
* **Notification Replacement**: Uses a fixed ID (`-r 101`) to replace the previous notification, preventing screen clutter.
* **Safety Checks**: Verifies the directory exists and contains valid files before attempting to switch.

## 🛠️ Installation

1. **Create the directory**:
   Ensure your animation files are stored in the expected location:
   ```bash
   mkdir -p ~/.config/niri/animations
