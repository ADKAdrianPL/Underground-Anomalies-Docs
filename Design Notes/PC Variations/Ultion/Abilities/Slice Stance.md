### A less basic offence.

Holding down the button uses up energy at a constant rate to slow down the character's perception of time and allow for rapid attacks unburdened by cooldown.

- Default Inputs: (Toggle, Hold)
    - Mouse and Keyboard: Right Mouse Button
    - Controller: Right Trigger
- Effect: (Duration: Varies + 0.2s | Cooldown: 0s)
    - The "Stance":
        1.  The owner is put into a state for the ability's duration, for as long as they have Energy, where:
            1.  Time is slowed to 2.5%.
            2.  Movement inputs are used for looking around.
            3.  Looking inputs are used for aiming.
            4.  Energy is decreased by 5 per second.
        2.  When the ability is ended
            1.  GlobalTimeDilation is set to 1.0
            2.  The Owner's InputResponse is set to "Default"
            3.  The Owner'sPlayerControler's input mode is set to game only, and its mouse cursor is hidden
    - The "Slice":
        1.  An area in front of the character, rotated to match the ___ is defined.
        2.  Damage is applied to every enemy hit.
- Notes:
    - A player can click the LMB ~5 times per second on average. compare to Slash, also if you can't click fast you can charge.
