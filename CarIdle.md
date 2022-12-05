# Contents

1. Door Management
2. Reset Direction
3. Reset Parameterflag, speed and door contact
4. Movement and landing

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
