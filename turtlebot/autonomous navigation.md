 ```
 sudo apt update
```
```
sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-joy \
  ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc \
  ros-noetic-rgbd-launch ros-noetic-rosserial-arduino \
  ros-noetic-rosserial-python ros-noetic-rosserial-client \
  ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server \
  ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro \
  ros-noetic-compressed-image-transport ros-noetic-rqt* ros-noetic-rviz \
  ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers
```
```
sudo apt install ros-noetic-dynamixel-sdk
```
```
sudo apt install ros-noetic-turtlebot3-msgs
```
```
sudo apt install ros-noetic-turtlebot3
```
```
git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
```
```
export TURTLEBOT3_MODEL=burger
```
```
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
```
export TURTLEBOT3_MODEL=burger
```
```
 roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```
```
export TURTLEBOT3_MODEL=burger
```
```
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
```
rosrun map_server map_saver -f ~/map
```
```
export TURTLEBOT3_MODEL=burger
```
```
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
```
export TURTLEBOT3_MODEL=burger
```
```
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```
```
export TURTLEBOT3_MODEL=burger
```
```
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```



