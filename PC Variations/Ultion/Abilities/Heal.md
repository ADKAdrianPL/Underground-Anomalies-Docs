### The only way to recover a meaningful ammount of health in a timely manner.

- Default Inputs (Toggle, Hold):
    
    - Mouse and Keyboard: "F" Key
        
    - Controller: Up Face Button
        
- Effect: (Duration: Varies + 0.75s | Cooldown: Duration + 1.0s)
    
    1.  A state is enabled, in which:
        1.  The OwnerCharacter's MaxWalkSpeed is set to 200.
        2.  Every frame, a HealingTick is ran, in which:
            1.  The Owner's Health and Energy are increased and decreased respectively,  
                by \[WorldDeltaSeconds \* 10\] for a rate of 10 points per second.
            2.  If the Owner still has Energy and missing Health, the healing is allowed to continue, otherwise the ability is ended.
        3.  When the ability ends, or is cancelled, the MaxWalkSpeed is reverted to the OriginalMaxWalkSpeed (set at Initialization).
- Notes:
    
    - The Rate of the stat's change in PointsPerSecond could easily be made variable,  
        by replacing \[WorldDeltaSeconds \* 10\] with \[WorldDeltaSeconds \* Rate(10 by default)\], though you would have to remember to negate the Rate for decreasing the Energy.