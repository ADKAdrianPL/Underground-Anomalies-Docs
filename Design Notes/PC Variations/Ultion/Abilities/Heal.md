### Fixing combat mistakes.

A vulnerable state of lowered mobility, in which energy is exchanged for health over time.

- Default Inputs (Toggle, Hold):
    - Mouse and Keyboard: "F" Key
    - Controller: Up Face Button
- Effect: (Duration: Varies + 0.75s | Cooldown: 1.0s)
    1.  The character's speed is lowered from 550 to 200.
        1.  Healing is constantly done:
            1.  The character's Health and Energy are increased and decreased respectively, at a rate of 10 points per second.
            2.  The ability ends if the character still has Energy and missing Health, otherwise the healing is allowed to continue.
        3.  When the ability ends, or is cancelled, the character's speed is reverted to 550.
- Notes:
    - Letting go of the input or running out of energy doesn't end the ability immediately. There is a 0.75s delay in which Health is no longer gained, but the character is still slowed and unable to use other abilities.<br>This is to make Healing unusable in the middle of a fight, unless a sizable window of opportunity is carved out by the player. Without these limitations this ability would be powerful enough to trivialize combat.
