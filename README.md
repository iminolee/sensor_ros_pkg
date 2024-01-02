## What's in this repo
This repository contains sensor-ros packages for SCOUT mobile robot.

## Sensors
* LiDAR
    * Ouster
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
sudo apt install -y         \
    ros-noetic_-pcl-ros     \
    libpcap-dev             \
    build-essential         \
    libeigen3-dev           \
    libjsoncpp-dev          \
    libspdlog-dev           \
    libcurl4-openssl-dev    \
    cmake
```
* Camera
```
sudo apt-get install ros-noetic-realsense2-camera
sudo apt-get install ros-noetic-imu-tools   # optional
```
## Usage Instructions
To start the LiDAR node in ROS:
```
# Velodyne VLP16
roslaunch velodyne_pointcloud VLP16_points.launch

# Ouster
roslaunch ouster_ros driver.launch      \
    sensor_hostname:=<sensor host name> \
    metadata:=<json file name>             # optional

```
To start the camera node in ROS:
```
roslaunch realsense2_camera rs_camera.launch
```
