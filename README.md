## ESPELEOROBO'S MAIN REPOSITORY
This repository lists all EspeleoRobo's related repositories and wikis. 
-----------------------------------------------------------------------

-----------------------------------------------------------------------
### INSTALL PACKAGES ON EMBEDDED COMPUTER (ESPELEOROBO)

##### copy and paste into terminal to have necessary packages in workspace (ESPELEOROBO)
```
cd ~/catkin_ws/src/
git clone --recurse-submodules https://github.com/ITVRoC/espeleo.git
cd espeleo/
git submodule foreach --recursive git checkout master
```

#### FOR LOCOMOTION (essential to function)
* Clone and compile [kacanopen](https://github.com/ITVRoC/kacanopen.git) to control the motors.
* Clone and compile [espeleo_io](https://github.com/ITVRoC/espeleo_io) to control the IOs.
* Clone and compile [espeleo_locomotion](https://github.com/ITVRoC/espeleo_locomotion) to control espeleorobo.
 
#### FOR LOCALIZATION AND MAPPING
* Install the driver [xsens imu](https://github.com/ITVRoC/general-wiki/wiki/Rodar-IMU-XSens-no-ROS).
* Install the [ouster 16 lidar](https://github.com/ITVRoC/general-wiki/wiki/Rodar-o-LiDAR-OUSTER-16-no-ROS).
* Clone and compile [espeleo_planning](https://github.com/ITVRoC/espeleo_planning).

-----------------------------------------------------------------------
### INSTALL PACKAGES ON BASE COMPUTER (RUGGED)

#### FOR LOCOMOTION (essential to function)
* Clone and compile [espeleo_gui](https://github.com/ITVRoC/espeleo_gui) GUI Interface for ESPELEO.
* Clone and compile [espeleo_teleop](https://github.com/ITVRoC/espeleo_teleop)  to control the espeleo with joystick and keyboard.
* Clone and compile [espeleo_msg_srv](https://github.com/ITVRoC/espeleo_msg_srv.git) messages and services to espeleo.

#### FOR SIMULATION
* Espeleorobo [v-rep's models](https://github.com/ITVRoC/espeleo_vrep_simulation).
 
 
-----------------------------------------------------------------------
## Espeleorobo ROS Communication General Guide
 
This guide presents all nodes in EspeleoRobo, with its topics, messages and description.
One may find a graphical representation [here](https://docs.google.com/presentation/d/1Lrz-dAwWeXqzpGeWaSDRkczdpwMNBig6JlObKeRsX5Q/edit#slide=id.p).
 
#### kacanopen
Provides a ROS interface to EPOS CAN functionalities.
 
 *Subscribed Topics*
  TODO
  
 *Published Topics*
  TODO
  
#### Reseting motors
Provides solution to fault motors

[Wiki](https://github.com/ITVRoC/espeleo/wiki/Fault-motors)

#### espeleo_locomotion
Converts linear and angular velocities input to coordinated joints actions.
 
*Subscribed Topics*
 * `/cmd_vel` - `<geometry_msgs/Twist>` - Receives linear (in \[m/s\]) and angular (in \[rad/s\]) commands.
  
*Published Topics*
 TODO
