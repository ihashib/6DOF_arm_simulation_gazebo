# 6DOF_arm_simulation_gazebo
Uses ROS Melodic on Kubuntu 18.04
URDF based simulation
Gazebo Version: 9.0
RViz version: 1.13.15
Qt version: 5.9.5
OGRE version: 1.9.0

Commands:
$rosrun mt_arm rviz.launch
$roslaunch gazebo_ros empty_world.launch
$rosrun mt_arm gazebo.launch

Debugging:

#1. After finishing RViz simulation and starting gazebo, make sure to make an empty world.
roslaunch gazebo_ros empty_world.launch
#2. When implementing the controllers for gazebo, make sure to install the controllers if it gives an error in ROS melodic.
sudo apt-get install ros-indigo-joint-state-controller : This will install joint_state_controller package
sudo apt-get install ros-indigo-effort-controllers : This will install Effort controller
sudo apt-get install ros-indigo-position-controllers : This will install position controllers
