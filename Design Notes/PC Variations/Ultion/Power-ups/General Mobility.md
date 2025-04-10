- Visual Representation
    
    - Switching from a normal crash pod space suit to what appears to be a standard High Mobility Exploration and Combat Suit
- Effects
    
    - Increments [Jump](../../../../../Underground%20Anomalies/Design%20Notes/PC%20Variations/Ultion/Abilities/Jump.md) Level
        
    - Changes Character Movement Values
        
        | Movement Variable | Original Value | Target Value |
        | --- | --- | --- |
        | Gravity Scale | 1.0 | 2.0 |
        | Jump Height | 90.0 | 430.0 |
        | Max Walk Speed | 350 | 550 |
        | Max Acceleration | 2048.0 | 7168.0 |
        | Air Control | 0.05 | 1.0 |
        | Ground Friction | 8.0 | 10.0 |
        | Falling Lateral Friction | 0.0 | 7.5 |
        
- Notes
    
    - (sqrt(((2 \* (0 - GravityZ)) \* JumpHeight))) = JumpZVelocity aka. "max jump height".
    - JumpHeight at 90 is achieved at 420 JumpZVelocity
    - maybe the speed and jump height increases should be one power-up, while the air control used for more precise jumps could be introduced later? maybe even at the half way point