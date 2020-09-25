# Dual-Universe-LUA-HUD

# Usage
Click on **flying_construct_MIN_HUD_paolo.conf** above. On the top right, right click the 'RAW' button and click Save Link As...

Save the file to *%ProgramData%\Dual Universe\Game\data\lua\autoconf\custom*, the filename does not matter (as long as it's still .conf)

In-game, right click your seat and go to *Advanced -> Update custom autoconf list*  - If you get a YAML error, you did not follow the above directions corretly.

Then *Advanced -> Run Custom Autoconfigure -> ButtonsHud - Dimencia and Archaegeo*

By default the HUD overwrites the in game flight Control Schemes.  You must right click the seat and set the control scheme to Keyboard.  Then look at the seat and choose Advanced-Edit LUA Parameters.  Mouse over each for a description, but the major one is userControlScheme.  You may set it to "Virtual Joystick" (which is the default), "Mouse", or "Keyboard".

This should set everything up and you're good to go

### Credits

Rezoix and his HUD - https://github.com/Rezoix/DU-hud

JayleBreak and his orbital maths/atlas - https://gitlab.com/JayleBreak/dualuniverse/-/tree/master/DUflightfiles/autoconf/custom

Archeageo and his work on the HUD