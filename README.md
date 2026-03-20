Setting up the Niri animations script and adding Otter-WM buttom
======================================================================

Add the animations folder to ~/.config/niri/

Add the niri-anim-toggle.sh script to ~/.local/bin/

link one of the animations one time only so niri knows where to start
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
Button animation command: niri-anim-toggle
