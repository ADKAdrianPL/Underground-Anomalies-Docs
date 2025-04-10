### summary

- Default Inputs: (Instant/Toggle)  
    While "Instant" is relatively self-explanitory, "Toggle" is a bit counter-intuitive.  
    It doesn't necessarily mean that one press of the listed button activates the ability and another one is required to turn it off.  
    "Toggle" could also mean that pressing the button turns it on, and letting go of it turns it off. This is denoted by adding ", Hold" after "Toggle", otherwise assume that the previous behaviour is intended.
    
    - Mouse and Keyboard:
        
    - Controller:
        
- Effect: \[Duration: X.XXs or Varies | Cooldown: X.XXs\]  
    Duration is how long an ability stays active after activation.  
    Cooldown is how often an ability can be activated, independent from duration.
    
    - description
- Notes:
    
    - Make sure that if the owning actor is needed multiple times, "GetOwningActorFromActorInfo" is only used once, and its result is cashed, instead of the "getting" being done multiple times
    - Make sure that the ability is commited after initalization (or after all other checks are passed)
    - Abilities need to block themselves
    - Make sure that these abilities are instanced per actor, rather than per activation
- Bugs:
    
    - If there are none, delete this point instead of leaving it empty