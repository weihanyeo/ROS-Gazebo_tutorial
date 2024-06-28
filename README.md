# URDF Model for Gazebo Integrated with ROS

This repository contains a URDF (Unified Robot Description Format) model for a robot, designed to work with Gazebo and integrated with ROS (Robot Operating System) and a video tutorial.

## Branches

This repository is organized into several branches, each serving a specific purpose:

1. **base**: Creates a simple URDF model
2. **base_sensors**: Adds sensors to the robot
3. **navigation**: Enables autonomous navigation (updated for [ROS Melodic Morenia](http://wiki.ros.org/melodic))

Please checkout the appropriate branch for your needs.

## Tutorial

For a step-by-step guide on how to use this repository, please watch our tutorial video:

[MyBot Tutorial Video](https://t.ly/Prcyw)

![simulation](https://github.com/weihanyeo/ROS-Gazebo_tutorial/assets/36888332/09e68fa7-50c1-40e0-adf7-791ec4ea7bd9)


## Software Versions
- Ubuntu: [18.04](https://ubuntu.com/tutorials/install-ubuntu-desktop-1804#1-overview) 
- ROS Version: [Melodic](https://wiki.ros.org/melodic/Installation/Ubuntu) 
- Gazebo Version: [11.0.0](https://classic.gazebosim.org)

Based on https://github.com/richardw05/mybot_ws.git

## Terminal Commands:

- ./run_gazebo - launch gazebo world with mybot robot
- ./run_cmd - give linear and angular velocity to robot for circular motion
- ./run_rviz - visualization of robot with sensors in rviz

Grab willow_garage.pgm (107 MB) from https://drive.google.com/open?id=19qgc33GMiKADq-p_aDTKzgeXyQ7PxEfF for learned willow garage map.

## Requirements:
```
sudo apt-get install ros-kinetic-gazebo-ros

sudo apt-get install ros-kinetic-turtlebot ros-kinetic-turtlebot-apps ros-kinetic-turtlebot-
interactions ros-kinetic-turtlebot-simulator ros-kinetic-kobuki-ftdi ros-kinetic-ar-track-
alvar-msgs
```
## Notes:
- Changes to CMakeLists may be required before catkin_make
- Above recorded simulation is speed up 10 times

## Usage: 
### Terminal 1 (Gazebo): 
```
roslaunch mybot_gazebo mybot_world.launch
```
### Terminal 2 (Map Building):
```
roslaunch mybot_navigation amcl_demo.launch
```
### Terminal 3 (Rviz):
```
roslaunch mybot_description mybot_rviz_amcl.launch
```
- Use 2D Nav Goal in Rviz to Navigate

## Navigation Tutorial

[Guide](https://github.com/weihanyeo/ROS-Gazebo_tutorial/blob/main/src/mybot_navigation/README.md)

## Contact

If you have any questions or issues, please open an issue in this repository or contact me at [yeowh@hotmail.sg](yeowh@hotmail.sg)
