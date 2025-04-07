### Technically "getting Knockback-ed", a reaction to receiving PointDamage from colliding with an enemy, or attack.

- Effect: (Duration: 0.8s | Cooldown: N/A, but functionaly the 1.25 Timer duration within the CH\_PlayerCharacter\_Base's "ApplyInvincibility" Event)
    1.  A state is applied during which:
        1.  Input is disabled to the OwnerCharacter's PlayerController
        2.  The FallingLateralFriction of the OwningCharacter's MovementComponent is set to 0.
    2.  The ability's OwnerCharacter is Launched(XYZ Override) away from the assailant, and up.  
        (using the equasion \[sqrt(((2 \* (0 - GravityZ)) \* Strenght)) = Vector(X, Y, 1) multiplier\] with Strength being set to 100)
    3.  After 0.8s:
        1.  Input is enabled to the OwnerCharacter's PlayerController
        2.  The FallingLateralFriction of the OwningCharacter's MovementComponent is set to the OriginalFallingLateralFriction (set at Initialization).
        3.  The Ability is ended.
- Notes:
    - Not to be confused with [Slash](../../../../../Underground%20Anomalies/Design%20Notes/PC%20Variations/Ultion/Abilities/Slash.md) Pushback (assuming such a thing will be implemented).
    - Maybe instead of a SetAssailant BPI Event, there should be a GetAssailant BPI Function?