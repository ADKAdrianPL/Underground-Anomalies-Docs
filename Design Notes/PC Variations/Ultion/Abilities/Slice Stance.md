### A less basic offence.

Holding down the button uses up energy at a constant rate to slow down the character's perception of time and allow for rapid attacks unburdened by cooldown.

- Default Inputs: (Toggle, Hold)
    - Mouse and Keyboard: Right Mouse Button
    - Controller: Right Trigger
- Effect: (Duration: Varies + 0.2s | Cooldown: 0s)
    - The "Stance":
        1.  The owner is put into a state for the ability's duration, for as long as they have Energy, where:
            1.  Time is slowed down to 2.5%.
            2.  Movement inputs are used for looking around.
            3.  Looking inputs are used for aiming.
            4.  Energy is decreased by 5 points per second.
            5.  The [Slash](Slash.md) is replaced by the "Slice".
        2.  When the ability is ended
            1.  Time is sped back up.
            2.  Movement and Looking inputs are reassigned back to moving and looking respectively.
    - The "Slice":
        1.  An area in front of the character, rotated to match the aiming direction is defined.
        2.  Damage is applied to every enemy hit.
- Notes:
    - A player can press a button (and therefore Slice) ~5 times per second on average, ~6.5 times faster than one can [Slash](Slash.md), due to that ability's cooldown.<br>
Balancing the game around this ammount of damage per second could've been unfair to players that are not able to press a button repeatedly as fast as assumed, the attack button can be held down within the "Stance" to charge the "Slice" with the damage that would otherwise be dealt with rapid attacks to rectify that.
