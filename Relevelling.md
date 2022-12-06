# Contents

1. Timer Increment
2. Bridging
3. Releveling Status

## Timer Increment
This part includes incrementation of the timer and display of message.

- Display shows “Relevelling”.
- Releveling timer incremented by timer10msDiff

## Bridging
This part includes door bridging.

- If door A is not closed or door B is not closed,
  - Bridge the door(will be explained).
- If door A is closed and door B is closed,
  - Do not bridge the door(will be explained).

## Releveling Status
This part includes 2 part to update status of releveling,

1. Doorzone Check
2. Timer Check

### Doorzone Check
This part includes conditions to check if elevator is in doorzone.

- If value of oCarIsInDoorZone is TRUE and carIsOnLevelWithDeviation is TRUE,
  - Elevator Speed will be reset.
  - Releveling timer will be reset.
  - statusReleveling set to sucessfulReleveling.
  - carManagement set to carIdle.
- If signal 141 is FALSE and signal 142 is FALSE,
  - Elevator Speed will be reset.
  - Releveling timer will be reset.
  - statusReleveling set to errorReleveling.
  - carManagement set to carIdle.

### Timer Check
This part includes conditions of releveling timer.

- If timerReLeveling exceeds 20 seconds,
  - Elevator Speed will be reset.
  - Releveling timer will be reset.
  - statusReleveling set to failedReleveling.
  - carManagement set to carIdle.
- If timerReLeveling exceeds 5 seconds and oCarIsInDoorZone is FALSE,
  - Elevator Speed will be reset.
  - Releveling timer will be reset.
  - statusReleveling set to failedReleveling.
  - carManagement set to carIdle.
- If timerReleveling is less than and equal to 5 seconds or timerReleveling is bigger than 5 seconds, timerReleveling is less than 20 seconds and oCarIsInDoorZone is TRUE,
  - statusReleveling set to processingReleveling.
  - If signal 141 is FALSE and signal 142 is TRUE,
    - Elevator Speed set to relevellingSpeedDown.
  - If signal 141 is TRUE and signal 142 is FALSE,
    - Elevator Speed set to relevellingSpeedUp.





    


