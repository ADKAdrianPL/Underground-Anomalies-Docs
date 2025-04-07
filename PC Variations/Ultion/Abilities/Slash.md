### The only way to deal damage without spenting recources.

- Default Inputs: (Instant)
    
    - Mouse and Keyboard: Left Mouse Button
        
    - Controller: Right Shoulder
        
- Effect: (Duration: 0.15s | Cooldown: 0.75s)
    
    1.  Every frame, a SlashTick is ran, in which:
        1.  A MultiBoxTraceForObjects is executed
        2.  Damage is applied to every Actor hit & pushback is applied to the PlayerCharacter, once per activation
        3.  The SwordOwnerHitReaction CollapsedGraph is run, in which:
            1.  It is checked whether or not the "Z" Value of the OwningActor'sCamera's ForwardVector is not greater than or equal to "0.5" and whether the TraceReturnValue is true.  
                In effect: If the player isn't looking up, and hit something.
            2.  If so, then the OwningCharacter's Jump (not to be confused with the ability "[Jump](../../../../../Underground%20Anomalies/Design%20Notes/PC%20Variations/Ultion/Abilities/Jump.md)") is ended.
            3.  The OwningCharacter is then Launched in the opposite of the rough direction its camera is pointed at.
    2.  After the amount of time defined in the Duration, the ability is ended.
- Notes:
    
    - The input for this ability is hijacked by [Slice Stance](../../../../../Underground%20Anomalies/Design%20Notes/PC%20Variations/Ultion/Abilities/Slice%20Stance.md).
    - Could give a fraction of the damage dealt as energy, as long as it doesn't step on the toes of the [Parry](../../../../../Underground%20Anomalies/Design%20Notes/PC%20Variations/Ultion/Abilities/Parry.md).
    - Sword-bouncing could "recharge" the character's double jump.
- Bugs:
    
    - ~~The VarHeight function of the jump can cancel the upward momentum from a sword-bounce~~  
        Solved