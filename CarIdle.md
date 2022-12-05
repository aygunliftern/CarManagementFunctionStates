# Contents

1. Door Management 
2. Reset Direction, Parameter Flag, Speed and Door Contact
3. Movement and Landing

## Door Management
This part reset the doors.

- If psuRequestDoorA is openTheDoor,
	- If DoorA_Open is TRUE,
		- Door A will be idle state.
- If psuRequestDoorA is not openTheDoor,
	- Door A will be idle state.

- If psuRequestDoorB is openTheDoor,
	- If DoorB_Open is TRUE,
		- Door B will be idle state.
- If psuRequestDoorB is not openTheDoor,
	- Door B will be idle state.

## Reset Direction, Parameter Flag, Speed and Door Contact
This part reset values of direction indication.

- Inspection up will be reset.
- Inspection down will be reset.
- Moving up will be reset.
- Moving down will be reset.

- If actionflag_gotoparametertarget is TRUE
	- actionflag_gotoparametertarget is FALSE

- Elevator Speed will be reset.

- Bridge door contact values will be reset (NOT ACTIVE).

## Movement and Landing
This part manages releveling and movement while elevator is idling.

- If targetFloor is FALSE,
	- Reset value of motion move up and down.
	- Car lights set to FALSE.
	- Parking function will be called.
	- If car is in doorzone and door A is closed or open and door B is closed or open and releveling function is ENABLE,
		- If signal 141 is ON and signal 142 is OFF or signal 141 OFF and signal 142 is ON,
			- Releveling timer will be reset.
			- carManagement set to reLeveling
- If targetFloor is not FALSE,
	- Car lights set to TRUE.
	- Set value of motion move up and down.
	- If carCurrentFloor is not targetFloor,
		- carManagement is set to requestCloseDoor.
- If psuRequestDoorA is openTheDoor or psuRequestDoorB is openTheDoor,
	- Display shows "Passenger Loading/Unloading".
