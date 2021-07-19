# Turtlebot3_Navigation
**First i work on ROS Online so it's different with first task ,so the first one task its kinetic but this it's melodic**

**I will write the code you wrote**

 **first i  install TurtleBot3 Packages**

$ sudo apt-get install ros-melodic-dynamixel-sdk
$ sudo apt-get install ros-melodic-turtlebot3-msgs
$ sudo apt-get install ros-melodic-turtlebot3

**And then i choose the turtlebot3**

echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
echo "export TURTLEBOT3_MODEL=waffle_pi" >> ~/.bashrc

$ cd ~/catkin_ws/src/
$ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make

$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch


$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch


$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_gazebo turtlebot3_house.launch


$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch

**Run SLAM Node**
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

**Run Teleoperation Node**
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

**finally here i Save Map in the last step**
$ rosrun map_server map_saver -f ~/map
