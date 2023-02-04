# Harden
Implement "Harden" feature from Mortal Shell into Skyrim

This code implements a freeze/unfreeze function using the SetSuspended function. The function takes a single argument, isSuspended, which determines whether the player should be frozen (isSuspended = true) or unfrozen (isSuspended = false).

When the player is frozen, their movement speed is set to 0 using the CallFunction("SetMovementSpeedMult", 0) line. The player's position, pitch, yaw, and roll are stored in the freezeX, freezeY, freezeZ, freezePitch, freezeYaw, and freezeRoll variables.

When the player is unfrozen, their movement speed is set back to normal using the CallFunction("SetMovementSpeedMult", 1) line. The player's position, pitch, yaw, and roll are set back to their stored values using the SetPlayerPos, SetPlayerPitch, SetPlayerYaw, and SetPlayerRoll functions.

The hotkey function, FreezePlayer, is bound to the f key using the ScriptEffect.AddKeyBinding line. When the hotkey is pressed, the function toggles the freeze/unfreeze state by calling the SetSuspended function with the current freeze state.

This mod should work as expected in SKSE, allowing you to freeze and unfreeze the player using the f key. 
