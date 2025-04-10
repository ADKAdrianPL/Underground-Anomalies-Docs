### The main mode of upward movement.

- Default Inputs: (Toggle, Hold)
    
    - Mouse and Keyboard: Space bar
        
    - Controller: Left Shoulder
        
- Effect: (Duration: Varies | Cooldown: N/A)
    
    1.  The AbilityLevel is checked for being greater than one;  
        If it is, the Owner is set to float by dividing its TerminalVelocity by 20.
    2.  The OwningCharacter Jumps.
    3.  The Ability is Ended when the input is let go of.
        1.  The TerminalVelocity is set to the OriginalTerminalVelocity (set at Initialization).
        2.  The OwningCharacter stops Jumping.
        3.  If conditions are meet (the Ability is not being Cancelled, the Owner is going up & not moving on the ground, the AbilityLevel is above 0), upward momentum is cancelled
- Notes:
    
    - Be careful not to make the max jump height too high.