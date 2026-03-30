Setting up the Niri animations script and Otter-WM buttom
======================================================================

Add the animations folder to ~/.config/niri/

Add the niri-anim-toggle.sh script to ~/.local/bin/

link one of the animations one time only so the script has a place to start
---------------------------------------------------------------------
ln -s ~/.config/niri/animations/pop-drop.kdl ~/.config/niri/animations/current_animation.kdl

Make the script executable
--------------------------
sudo chmod +x ~/.local/bin/niri-anim-toggle.sh

Edit your niri config.kdl, remove the animation section and add in its place
-----------------------------------------------------------------------------
include "animations/current_animation.kdl"

Add a button in otter-shell
----------------------------
Button animation command: niri-anim-toggle.sh

WARNING:
--------
I made this script with the help of a clanker (gemini), this was just for a personal project.

Credits for the animations
--------------------------
https://github.com/jhsu  
ditcher-glitch

https://github.com/jgarza9788
Blur
Glitch (01)
smoke
energize_b 

https://github.com/XansiVA
bloom.kdl
burn-ashes.kdl
burn-multicolor.kdl
burn.kdl
fold-window.kdl
glitch.kdl
pixelate.kdl
pop-drop.kdl
ribbons.kdl
roll-drop.kdl
swipe-window.kdl
unravel.kdl
