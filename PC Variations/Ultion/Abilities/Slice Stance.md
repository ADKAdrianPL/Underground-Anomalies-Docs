### The main way of dealing sizable ammounts of damage.

- Default Inputs: (Toggle, Hold)
    
    - Mouse and Keyboard: Right Mouse Button
        
    - Controller: Right Trigger
        
- Effect: (Duration: Varies + 0.2s | Cooldown: N/A)
    
    - The stance
        
        1.  The owner is, for the ability's duration, put into a state where:
            
            1.  The Owner's InputResponse is set to "SliceStance"
            2.  GlobalTimeDilation is set to 0.025
            3.  The Owner'sPlayerControler's mouse cursor is shown
            4.  Every frame, a SliceStanceTick is ran, in which:
                1.  It is checked whether the Owner still has energy, if not, the ability is canceled
                2.  Otherwise, energy is decreased by \[(WorldDeltaSeconds / GlobalTimeDilation) \* (-DrainRate)\]
        2.  When the ability is ended
            
            1.  GlobalTimeDilation is set to 1.0
            2.  The Owner's InputResponse is set to "Default"
            3.  The Owner'sPlayerControler's input mode is set to game only, and its mouse cursor is hidden
    - A Slice is the mid-stance replacement of the [Slash](../../../../../Underground%20Anomalies/Design%20Notes/PC%20Variations/Ultion/Abilities/Slash.md) in which:
        
        1.  A MultiBoxTraceForObjects is executed
        2.  Damage is applied to every Actor hit, once per activation
        3.  A Message to "be sliced" is sent to every Actor hit, once per activation, via BPI_Ability_Extras
- Notes:
    
    - A player can, on average, click the LMB ~5 times per second.  
        Assuming default settings (10 dmg & a drain rate of 5 EPS ), the above translates to 50 dmg per second, or 10 dmg per energy point.  
        For the sake of balance, rapid slashing cannot deal significantly more damage than charging (more than 100 dmg per 10 energy).
    - While the time dilation doesn't interfere with things that are supposed to happen in "world time", it may disturb things in "player time".  
        The fix for this is to multiply the "time" value by "GlobalTimeDilation"
    - add the ability to cancel out of a failed parry at the cost of 20 energy?
- Bugs:
    
    - ~~Despite the fact that the behaviors for the "IA_Look" and "IA_Move" events are being defined within "CH_Player_Ultion" the behaviors defined within "CH_Player_Base" are still being used, and there's no way to override them, like any other event.~~  
        The only thing solution i can think of is to negate the Base's behavior.
        
    - Slicing a SlicableActor works for the first time and then works less and less when slicing the halves repeatedly. Maybe check the how to slice an actor video that was originally used as the basis for the slicing functionality: if there's any setting of the SlicableActor that was missed
        
    - check if slicing multiple different SlicableActors works
        
    - Being within slice stance seems to make the game lag after some number of activatons