# Husky - UR3 manipulator with AR marker Stockroom
 
## Overview
The Husky UR3 mobile manipulation tutorial will show you how to operate a mobile manipulation robot using Gazebo, RViz, MoveIt, and the UR3 arm. 

In this package, the Gazebo simulation enviroment based on the [stockroom world](https://github.com/Jpub/ROS/tree/master/stockroom_bot), also you can subscribe pose of the [ar_track_alvar](http://wiki.ros.org/ar_track_alvar).


**Author:**   
- [Hyeonjun Park](https://www.linkedin.com/in/hyeonjun-park-41bb59125), koreaphj91@gmail.com**  


**Affiliation: [Human-Robot Interaction LAB](https://khu-hri.weebly.com), Kyung Hee Unviersity, South Korea**

## This pakage for ROS Melodic version

## Installation
- Before do this, please backup important files.

### Dependencies
---
* This pacakge is based on the [husky_ur3_manipulator](https://github.com/MrLacquer/husky_ur3_manipluator) 'melodic' branch.  
Therefore, please do it after intallation of the huksy_ur3_manipulator.
---


- For subscribe ar markers,
[ar_track_alvar](http://wiki.ros.org/ar_track_alvar)
```
$ sudo apt-get install ros-melodic-ar-track-alvar
```

- For stockroom gazebo world.  
[stockroom world](https://github.com/Jpub/ROS/tree/master/stockroom_bot)
```
$ cd ~/Downloads && git clone https://github.com/Jpub/ROS.git
$ cd ROS
$ cp -r stockroom_bot ~/catkin_ws/src

$ gedit ~/.bashrc
   export GAZEBO_MODEL_PATH=${HOME}/catkin_ws/src/stockroom_bot/models

$ cd ~/catkin_ws && catkin_make
$ rospack profile && rosstack profile
```

## How to start?

```
$ cd ~/catkin_ws/src && git clone https://github.com/MrLacquer/husky-ur3-stockroom.git
$ cd ~/catkin_ws && catkin_make
$ rospack profile && rosstack profile

- Bring up Gazebo and the Husky UR3 manipulator, 
$ roslaunch husky_ur3_stockroom husky_ur3_stookroom.launch 


- Bring Up MoveIt & RViz
$ roslaunch husky_ur3_test_moveit_config husky_ur3_planning_execution.launch
$ roslaunch husky_ur3_stockroom husky_ur3_amcl_stockroom.launch 
$ roslaunch husky_ur3_stockroom husky_ur3_stockroom_rviz.launch 


- Contorlling the UR3 manipulator (more detail [ur3-moveit-test](https://github.com/MrLacquer/ur3-moveit-test.git))
$ rosrun husky_ur3_stockroom husky_ur3_stockroom_control.py
```

## Note


## Description


## Demo
### Launch the Stockroom Gazebo and Moveit!
[[SLAM Video Link]<img width="1000" src="https://user-images.githubusercontent.com/4105524/81662895-2a4f1180-9479-11ea-938a-7d1bd5d1709d.png"  alt="Screenshot" title="Screenshot">]()

