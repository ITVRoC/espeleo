# ESPELEOROBO'S MAIN REPOSITORY

This repository lists all EspeleoRobo's related repositories and wikis. 


---------------------------------------------------------
## INSTALL ON ESPELEO 

Packages for EspeleoRobo's embedded computer.

### FOR LOCOMOTION

#### PCAN drivers to use CAN:
 - https://github.com/ITVRoC/espeleo/wiki/PCAN-driver-installation

#### ROS_EPOSMCD to control the motors:
 - https://github.com/ITVRoC/ros_eposmcd
 
#### ESPELEO_IO to control the IOs:
 - https://github.com/ITVRoC/espeleo_io
 
#### ESPELEO_TELEOP to control the espeleo with joystick and keyboard:
 - https://github.com/ITVRoC/espeleo_teleop
 
#### ESPELEO_LOCOMOTION package 
 - https://github.com/ITVRoC/espeleo_locomotion
 
### FOR LOCALIZATION AND MAPPING

#### Install the XSENS IMU driver:
 - https://github.com/ITVRoC/general-wiki/wiki/Rodar-IMU-XSens-no-ROS
 
#### Install the Ouster 16 Lidar package on ROS:
 - https://github.com/ITVRoC/general-wiki/wiki/Rodar-o-LiDAR-OUSTER-16-no-ROS
 
#### Espeleo_planning
- https://github.com/ITVRoC/espeleo_planning
 

 ## INSTALL ON BASE COMPUTER
 
 Packages for base computer.
 
 #### GUI Interface for ESPELEO
 
 - https://github.com/ITVRoC/espeleo_gui
 

 ## FOR SIMULATION
 
 Packages for simulating EspeleoRobo.
 
 #### EspeleoRobo V-REP's models:
 - https://github.com/ITVRoC/espeleo_vrep_simulation
 
 
 
 ------------------------------------------------------------------------
 # EspeleoRobo ROS Communication General Guide
 
 This guide presents all nodes in EspeleoRobo, with its topics, messages and description.
 One may find a graphical representation [here](https://docs.google.com/presentation/d/1Lrz-dAwWeXqzpGeWaSDRkczdpwMNBig6JlObKeRsX5Q/edit#slide=id.p).
 
 ## motor_manager
 
 Provides a ROS interface to EPOS CAN functionalities.
 
  *Subscribed Topics*
  * `/ros_eposmcd/position_movement_absolute` - `<ros_eposmcd_msgs/MovementArray>` - set joints absolute position in \[radians\].
  * `/ros_eposmcd/position_movement_relative` - `<ros_eposmcd_msgs/MovementArray>` - set joints relative position with respect to the actual position, in \[radians\].
  * `/ros_eposmcd/velocity_movement` - `<ros_eposmcd_msgs/MovementArray>` - set joints angular velocity in \[radians/second\].
  
 *Published Topics*
  * `/ros_eposmcd/joints_positions` -  `<ros_eposmcd_msgs/EspeleoJoints>` - joints position in \[radians\].
  

 ## espeleo_locomotion
 
 Converts linear and angular velocities input to coordinated joints actions.
 
 *Subscribed Topics*
  * `/cmd_vel` - `<geometry_msgs/Twist>` - Receives linear (in \[m/s\]) and angular (in \[rad/s\]) commands.
  
 *Published Topics*
  * `/ros_eposmcd/position_movement_absolute` - `<ros_eposmcd_msgs/MovementArray>` - set joints absolute position in \[radians\].
  * `/ros_eposmcd/position_movement_relative` - `<ros_eposmcd_msgs/MovementArray>` - set joints relative position with respect to the actual position, in \[radians\].
  * `/ros_eposmcd/velocity_movement` - `<ros_eposmcd_msgs/MovementArray>` - set joints angular velocity in \[radians/second\].

 
 
 
 
 
 
 
 
 
