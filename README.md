# Warman-Robot
Robot's function:
The robot drives forward for a duration of time then stops. The extending arm is released and the robot turns to each tower and unloads the required number of payloads.

Robot Components:
- Drivetrain:
  6WD. uses L298N H bridge. left/right wheels grouped to share common signal pins (tank steering). only needs to drive forward/backward
- Extending Arm: 
  is held back by a solenoid latch. Once the latch is given a HIGH signal, the arm releases
- Rotating base: 
  controlled by a stepper. initially faces forward for calibration. points to each tower, based on the angles we measure
- Storage device: 
  ejects payloads using a stepper. it rotates every 20 steps to release a payload. the number of payloads it ejects is inputted for each tower

Given the nature of the challenge (mechanical focus), no sensors are necessary. Therefore all the inputs will be hardcoded into our main loop.
