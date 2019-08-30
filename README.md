# ESPELEOROBO'S MAIN REPOSITORY

This repository lists all EspeleoRobo's related repositories and wikis. 

---------------------------------------------------------
## INSTALL ON ESPELEO 

Packages for EspeleoRobo's embedded computer.

### FOR LOCOMOTION

#### KACANOPEN to control the motors:
 - https://github.com/ITVRoC/kacanopen.git
 
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
 
 #### Espeleorobo V-REP's models:
 - https://github.com/ITVRoC/espeleo_vrep_simulation
 
 
 
 ------------------------------------------------------------------------
 # Espeleorobo ROS Communication General Guide
 
 This guide presents all nodes in EspeleoRobo, with its topics, messages and description.
 One may find a graphical representation [here](https://docs.google.com/presentation/d/1Lrz-dAwWeXqzpGeWaSDRkczdpwMNBig6JlObKeRsX5Q/edit#slide=id.p).
 
 ## kacanopen
 
 Provides a ROS interface to EPOS CAN functionalities.
 
  *Subscribed Topics*
   TODO
  
  *Published Topics*
   TODO
  
 ## espeleo_locomotion
 
 Converts linear and angular velocities input to coordinated joints actions.
 
 *Subscribed Topics*
  * `/cmd_vel` - `<geometry_msgs/Twist>` - Receives linear (in \[m/s\]) and angular (in \[rad/s\]) commands.
  
 *Published Topics*
  TODO
