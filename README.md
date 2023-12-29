## What's in this repo
This repository contains sensor-ros packages for SCOUT mobile robot.

## sensors
* LiDAR
    * Velodyne VLP16
* Camera
    * Intel RealSense D435i

## Prerequisities
1. Install the ROS distribution, ROS Noetic on Ubuntu 20.04.<br/>
https://wiki.ros.org/noetic/Installation/Ubuntu
2. All ros packages are for ROS Noetic ver.
3. Using the terminal, register your personal LiDAR IP on your host PC. <br/>
https://wiki.ros.org/velodyne/Tutorials/Getting%20Started%20with%20the%20Velodyne%20VLP16


## Installations
* LiDAR
```
sudo apt-get install ros-noetic-velodyne
sudo apt-get install libpcap-dev
```
* Camera
```
sudo apt-get install ros-noetic-realsense2-camera
sudo apt-get install ros-noetic-imu-tools
```
## Usage Instructions
To start the LiDAR node in ROS:
```
roslaunch velodyne_pointcloud VLP16_points.launch
```
To start the camera node in ROS:
```
roslaunch realsense2_camera rs_camera.launch
```
