# Contents

1. Door Management 
2. Reset Direction, Parameter Flag, Speed and Door Contact
3. Movement and landing

## Door Management
This part reset the doors.

- If psuRequestDoorA is openTheDoor,
	- If DoorA_Open is TRUE
		- Door A will be idle state
- If psuRequestDoorA is not openTheDoor,
	- Door A will be idle state

- If psuRequestDoorB is openTheDoor,
	- If DoorB_Open is TRUE
		- Door B will be idle state
- If psuRequestDoorB is not openTheDoor,
	- Door B will be idle state

## Reset Direction, Parameter Flag, Speed and Door Contact
This part reset values of direction indication.

- Inspection up will be reset
- Inspection down will be reset
- Moving up will be reset
- Moving down will be reset
