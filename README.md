# Dual-Universe-LUA-HUD

# Usage
Click on **flying_construct_MIN_HUD_paolo.conf** above. On the top right, right click the 'RAW' button and click Save Link As...

Save the file to *%ProgramData%\Dual Universe\Game\data\lua\autoconf\custom*, the filename does not matter (as long as it's still .conf)

In-game, right click your seat and go to *Advanced -> Update custom autoconf list*  - If you get a YAML error, you did not follow the above directions corretly.

Then *Advanced -> Run Custom Autoconfigure -> ButtonsHud - Dimencia and Archaegeo*

By default the HUD overwrites the in game flight Control Schemes.  You must right click the seat and set the control scheme to Keyboard.  Then look at the seat and choose Advanced-Edit LUA Parameters.  Mouse over each for a description, but the major one is userControlScheme.  You may set it to "Virtual Joystick" (which is the default), "Mouse", or "Keyboard".

This should set everything up and you're good to go

## Controls - MINHUD and Archeageo HUD
**Alt+1** and **Alt+2** (Option1 and Option2) **to scroll between target planets for Autopilot and display**.  This widget will not display if no planet is selected (ie you must press one of these hotkeys after entering the seat in order to show the widget)

**Alt+3 ** toggles the **HUD** off or back On.  Orbital display will still show if hud is off.

**Alt+4** to engage **Autopilot** for interplanetary travel, if you are in space and have a planet targeted with Alt+1/Alt+2.  Ensure you have a clear line of sight to the target.  This will align to the target, realign slightly to point 200km to the side of the target, accelerate, cut engines when at max, start braking when appropriate, and hopefully achieve a stable orbit around the target.

**Alt+5** to toggle **Turn & Burn Mode**, which changes all your braking readouts to assume you will be turning and burning.  Be sure to set *warmup* in the Parameters if you use this; the default warmup is assumed to be 32s.  Autopilot will also turn and burn for you (Auto-Braking will not).  Note that Turn & Burn Mode assumes your ship will be able to face the correct direction to burn before you must begin braking, and should be used with caution for short trips

**Alt+6** to toggle all **Normal Widgets**, does not include weapons, radar, or periscorpe

**Alt+7** to **Save variables in a databank** - To use:  Attach a databank to your ship in any location.  Rerun the HUD Autoconfig. Change any variables able to be saved (shown below) using Edit LUA Paremeters. Get in seat.  Hit ALT-7 to save.  These will now autoload anytime you get in seat.  To overwrite you must hit alt-7 to wipe the databank, then get out, rerun Autoconfig, then change the values with Edit LUA Parameters, get back in, and alt-7 to save the new values.  

**Alt+8** will toggle **Follow Mode** with a **Remote Controller**.  This makes your craft lift off and try to follow you wherever you go.

**Alt+9** to engage **Auto-Brake**.  This will simply engage the brake if you come within the max braking distance of the planet targeted with Alt+1 and Alt+2, and disengage it once it's gotten as close to an orbit as it can just by braking.  This is an alternative to auto-pilot if you don't want to give the autopilot control over where your ship is facing or thrusters

This feature will also load your values if you update the HUD autoconfigure to a new release or if you need to rerun it due to changes on your ship unless the list of saved variables has changed.

## Current Savable Variables
userControlScheme
AutopilotTargetOrbit
brakeToggle
apTickRate
turnAssist
warmup
MaxGameVelocity
freeLookToggle
PrimaryR, PrimaryG, PrimaryB
DeadZone
circleRad
MouseXSensitivity
MouseYSensitivity

## Customization
The following LUA parameters were added

*PrimaryR*, *PrimaryG*, *PrimaryB* - To set the primary color for the HUD

*warmup* - How long your engines take to warmup, or T50.  Defaults to 32.  For everything but freight engines, these values for space engines are: XS 0.25, S 1, M 4, L 16, XL 32.  If you're using freight engines, you should probably check https://hq.hyperion-corporation.de/ingame-engine-library

*circleRad* - to set the size of the altimeter circle in the middle of the screen, setting it to 0 will remove the circle.


### Credits

Rezoix and his HUD - https://github.com/Rezoix/DU-hud

JayleBreak and his orbital maths/atlas - https://gitlab.com/JayleBreak/dualuniverse/-/tree/master/DUflightfiles/autoconf/custom

Archeageo and his work on the HUD