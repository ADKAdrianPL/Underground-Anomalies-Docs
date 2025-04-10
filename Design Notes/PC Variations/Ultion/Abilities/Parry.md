### The most important ability in [this character's](../../../../../Underground%20Anomalies/Design%20Notes/PC%20Variations/Ultion/Summary.md) arsenal, the combat's entire gameplay loop revolves around it.

- Default Inputs (Toggle, Hold):
    
    - Mouse and Keyboard: "R" Key
        
    - Controller: Right Face Button
        
- Effect: (Duration: 0.5s | Cooldown: 1.0s)
    
    1.  A state is enabled, in which:
        1.  A message is sent to the OwnerCharacter, for it to change its DamageResponse to "Parry".
            - Movement and Looking input is also disabled.
        2.  The OwnerCharacter's GravityScale and Velocity are both zero'd out.
    2.  If PointDamage is taken while the OwnerCharacter's DamageResponse is set to "Parry":
        - If the UnitDirection(From:Camera; To:Assailant) is equal to the Camera's ForwardVector with 0.6 error tolerance, the Parry is a Success.
            1.  The Damage value is added to the character's Energy.
                
            2.  The ParryAbility is sent a message, that it was successful
                
                - If the player is still holding the player button, the duration is reset
                - If the player has let go of the button by this time, the ability is ended
            3.  The assailant is sent a message, that it got parried.
                
        - If its a failure:
            1.  The Parry is cancelled.
            2.  The PointDamage is applied as normal.
        - If nothing happens, the parry ends after 0.5s.
    3.  When the parry ends, or is cancelled
        1.  A message is sent to the OwnerCharacter, for it to change its DamageResponse to "Default".
            - Movement and Looking input is also enabled.
        2.  The OwnerCharacter's GravityScale is reverted to the OriginalGravityScale (set at Initialization).
- Notes:
    
    - The Player shouldn't just need to Parry, they should want to Parry.
    - The first 0.1s of the parry could also reflect the damage, unlike the remaining duration. This better timed parry would be referred to as a "Counter"
- Bugs:
    
    - ~~Successful parries still damage you due to AnyDamage running along side PointDamage. (there is a sloppy workaround within CH_Player_Ultion's "SuccessfulParry" Graph)~~  
        This just magically went away after changing cast nodes to interfaces