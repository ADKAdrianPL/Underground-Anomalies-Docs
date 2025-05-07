### A flashy offence.

Holding down the button uses up energy at a constant rate to slow down the character's perception of time and allow for rapid attacks unburdened by cooldown.

- Default Inputs: (Toggle, Hold)
    - Mouse and Keyboard: Right Mouse Button
    - Controller: Right Trigger
- Effect: (Duration: Varies + 0.2s | Cooldown: 0s)
    - The "Stance":
        1.  The owner is, for the ability's duration, put into a state where:
            1.  The Owner's InputResponse is set to "SliceStance"
            2.  GlobalTimeDilation is set to 0.025
            3.  The Owner'sPlayerControler's mouse cursor is shown
            4.  Every frame, a SliceStanceTick is ran, in which:
                1.  It is checked whether the Owner still has energy, if not, the ability is canceled
                2.  Otherwise, energy is decreased by \[(WorldDeltaSeconds / GlobalTimeDilation) \* (-DrainRate)\]
        2.  When the ability is ended
            1.  GlobalTimeDilation is set to 1.0
            2.  The Owner's InputResponse is set to "Default"
            3.  The Owner'sPlayerControler's input mode is set to game only, and its mouse cursor is hidden
    - The "Slice":
        1.  An area in front of the character, rotated to match the ___ is defined.
        2.  Damage is applied to every enemy hit.
- Notes:
    - A player can click the LMB ~5 times per second on average. compare to Slash, also if you can't click fast you can charge.
