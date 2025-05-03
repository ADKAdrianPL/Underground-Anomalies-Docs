### Moving up in the world.

The main method of navigating an obstacle filled world, second only to walking. Used to jump between platforms, around stationary hazards, and potentialy over some enemies.

- Default Inputs: (Toggle, Hold)
    - Mouse and Keyboard: Space bar
    - Controller: Left Shoulder
- Effect: (Duration: Varies | Cooldown: N/A)
    1.  The character Jumps.
    2.  The Ability is Ended when the input is let go of.
        1.  If the character hasn't reached the max jump height yet, upward momentum is stopped.
- Notes:
    - The player is allowed to stop ascending mid-jump to provide more precise control over the character.
    - The variable jump height functionality is only enabled after the player collects the [General Mobility](../Power-ups/GeneralMobility.md) power-up. Without it the jump only stops at max height, even if the button is released sooner.
