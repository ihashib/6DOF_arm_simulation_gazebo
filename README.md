# 6DOF_arm_simulation_gazebo          
Uses ROS Melodic on Kubuntu 18.04.                           
URDF based simulation.                                
Gazebo Version: 9.0.                            
RViz version: 1.13.15.                         
Qt version: 5.9.5.                    
OGRE version: 1.9.0.                                  

Commands:                         
To run rviz:         
"$rosrun mt_arm rviz.launch".                     
To run gazebo:                    
"$roslaunch gazebo_ros empty_world.launch"                
"$rosrun mt_arm gazebo.launch".

Using the joint state controller to control arm:
$rostopic pub -1 /mt_arm/joint1_position_controller/command std_msgs/Float64 "data: 0.0"

Debugging:
#1. After finishing RViz simulation and starting gazebo, make sure to make an empty world.
roslaunch gazebo_ros empty_world.launch
#2. When implementing the controllers for gazebo, make sure to install the controllers if it gives an error in ROS melodic.
$sudo apt-get install ros-melodi-joint-state-controller        
$sudo apt-get install ros-melodic-effort-controllers           
$sudo apt-get install ros-melodic-position-controllers          
