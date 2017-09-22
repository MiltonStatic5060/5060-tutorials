# The Basics
An `OpMode` is the blueprint that defines the robot's commands.

Two types of Op modes:
- Autonomous - Phase where robot runs on preset commands. Only uses sensor data and cannot be controlled by players
- Telecommunication (TeleOp) - Phase where up to 2 players control robot by game controllers

----------------------

Every `OpMode` has two parts:
- Initialization - Like "starting a car". Activates motors and servos.
- Loop - Like "running the car". Commands and instructions run in a loop.  Usually the program keeps checking `if` statements to run a command. (if "button a pressed" then "move forward")

----------------------

