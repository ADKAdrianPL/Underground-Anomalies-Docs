### Defence and resource generation.

Enter a stationary state, in which damage recieved from the front is turned into Energy.

- Obtained from the [Ability Giving Power-up](../../../Enviroment/Enviromental%20Features/Helpful/Power-ups/Ability%20Giving.md) in the [Sword Intro Level](../../../Enviroment/Levels/Sword%20Intro.md).
- Default Inputs (Toggle, Hold):
    - Mouse and Keyboard: "R" Key
    - Controller: Right Face Button
- Effect: (Duration: 0.5s | Cooldown: 1.0s)
    1.  A state is enabled, in which:
        1.  Movement and Looking inputs are disabled.
        2.  The character's gravity and velocity are set to zero.
        3.  The character enters the "Parry" state.
    2.  When damage is recieved while within the "Parry" state:
        - If it's from the front, the Parry is a Success:
            1.  The damage is added to the character's Energy.
            2.  The assailant is notified that it got parried.\*
            3.  The ability either ends or continues.
                - If the player is still holding the player button, the duration is extended by 0.5s.\**
                - If the player has let go of the button by this time, the ability is ended.
        - If its a failure:
            1.  The Parry is cancelled.
            2.  The PointDamage is applied as normal.
    3.  If no damage is received, the parry ends after 0.5s.
    4.  When the parry ends, or is cancelled:
        1.  The character returns the "Default" state.
        2.  Movement and Looking inputs are enabled.
        3.  The character's gravity is reverted to the value it was at the start of the Parry.
- Notes:
    - This is the only ability that generates Energy, as well as being the primary method of avoiding damage; it is designed to be central to the gameplay loop (at least within combat).
    - \*Some enemies are pushed up and away from the character when they're Parried.
    - \**This functionality exists to account for rapid enemy attacks, by allowing the player defend against all of them by holding the button down, instead of being forced to press the button equaly rapidly. This is most notably used in the fight against the [final boss]().
