### A situational burst of lateral mobility.

- Default Inputs: (Instant)
    
    - Mouse and Keyboard: Left Shift
        
    - Controller: Left Trigger
        
- Effect: (Duration: 0.225s | Cooldown: 1.5s)
    
    1.  A RootMotionConstantForce is applied to the Owner
    2.  If the Owner'sCharacterMovement reads as falling, AirCharges is decremented.
    3.  After 0.225s the applying of RootMotionConstantForce is ended, thus ending the ability
- Notes:
    
    - Due to the possibility that higher mobility would encourage players dodging attacks more than parrying them, dashing should only ever have one charge.
    - Should only recharge after landing from the air, the only acception could be bouncing off of an enemy with the [Slash](../../../../../Underground%20Anomalies/Design%20Notes/PC%20Variations/Ultion/Abilities/Slash.md).
    - (Distance / Time) gives strength, though if using a math node they might need to be named something else, like Reach and Time (although it's pointless to use a math node here, since the calculation here is just one operation)
- Bugs:
    
    - Isn't interrupted properly by the [Knockback](../../../../../Underground%20Anomalies/Design%20Notes/PC%20Variations/Ultion/Abilities/Knockback.md) applied at taking PointDamage.