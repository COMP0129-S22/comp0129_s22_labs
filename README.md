# UCL-CS COMP0129-S22 Labs

Author: Dimitrios Kanoulas (d.kanoulas@ucl.ac.uk), Luke Beddow, Denis Hadjivelichkov

Description: This package implements lab code for COMP0129-S22

## Clone and Build
```bash
> git clone https://github.com/COMP0129-S22/comp0129_s22_labs.git
> cd comp0129_s22_labs/
> catkin config --extend /opt/ros/${ROS_DISTRO} --cmake-args -DCMAKE_BUILD_TYPE=Release
> catkin build
> source devel/setup.bash
```

## Style Lab


## MoveIt! Lab

```bash
> sudo apt install ros-melodic-moveit
> curl -sSL http://get.gazebosim.org | sh
> sudo apt-get install ros-melodic-gazebo-ros-pkgs ros-melodic-gazebo-ros-control
```

Copy the entire ‘moveit_tutorial’ folder into the main workspace, i.e., comp0129_s22_robot/src

```bash
> cd ~/comp0129_s22_robot
> catkin config --extend /opt/ros/${ROS_DISTRO} --cmake-args -DCMAKE_BUILD_TYPE=Release
> catkin build
> source devel/setup.bash
> roslaunch moveit_tutorial tutorial.launch 
```

```bash
> rosservice call /moveit_tutorial/set_gripper "finger_distance: 0.08"
> rosservice call /moveit_tutorial/set_arm 
```

## PCL Lab

### Pre-requirements
```bash
> sudo apt-get install ros-melodic-moveit-resources
> sudo apt-get install ros-melodic-octomap*
> sudo apt-get install libpcl-dev
> sudo apt-get install ros-melodic-pcl-ros 
```

## Add the Open Gazebo Models Database
Use git to get a bunch of open source gazebo models from the Open Source Robotics Foundation (OSRF) 

```
> cd
> git clone https://github.com/osrf/gazebo_models.git
```
Add Models path to the bashrc
```
> echo 'export GAZEBO_MODEL_PATH=~/gazebo_ws/gazebo_models:${GAZEBO_MODEL_PATH}' >> ~/.bashrc
source ~/.bashrc
```

### Build and Try
```bash
> cd ~/comp0129_s22_lab
> catkin config --extend /opt/ros/${ROS_DISTRO} --cmake-args -DCMAKE_BUILD_TYPE=Release
> catkin build
> source devel/setup.bash
> roslaunch pcl_tutorial pcl_tutorial.launch  
```
