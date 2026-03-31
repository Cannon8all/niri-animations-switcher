Niri Animation Toggle

A bash script that cycles through Niri window manager animations with a single command. Perfect for quick visual switching without restarting.
Features

    Cycle through animations – Press a button to switch to the next animation in your collection
    Loop seamlessly – Automatically wraps back to the first animation after the last one
    Desktop notifications – Get instant feedback on which animation is now active
    Symlink-based – Uses a single symlink that Niri reads, so no config editing needed per switch

Prerequisites

    Niri window manager installed
    notify-send (usually included with most Linux distributions)
    Animation .kdl files in ~/.config/niri/animations/

Installation
1. Create the script

Save the script as ~/.local/bin/niri-anim-toggle.sh
2. Make it executable
bash

chmod +x ~/.local/bin/niri-anim-toggle.sh

3. Create the initial symlink
bash

ln -s ~/.config/niri/animations/pop-drop.kdl ~/.config/niri/animations/current_animation.kdl

(Replace pop-drop.kdl with your preferred starting animation)
4. Update Niri configuration

Open ~/.config/niri/config.kdl and replace your animations { ... } section with:
kdl

include "animations/current_animation.kdl"

5. Bind to a hotkey (optional)

Add to your Niri config:
kdl

binds {
    Mod+Shift+A { spawn "niri-anim-toggle.sh"; }
}

Or integrate with Otter-Shell or another launcher using the command: niri-anim-toggle.sh
How it works

    Scans ~/.config/niri/animations/ for all .kdl files
    Identifies the currently active animation via the current_animation.kdl symlink
    Updates the symlink to point to the next animation in alphabetical order
    Sends a desktop notification showing the new animation name
    Loops back to the first animation after the last one

Requirements for Niri to apply changes

You may need to log out and back in or restart Niri for animation changes to take effect, depending on your Niri version.
