# Turtlesim

The Turtlesim is a simple robot simulator used for familiarizing the concept of ros. A detailed description can be found at http://wiki.ros.org/turtlesim

The turtlesim can be started by running the roscore

```
roscore
```
In a new terminal, type
```
rosrun turtlesim turtlesim_node
```
It will open up a simulator. The turtlesim is a node. A node in ROS is a collection of topics, sevices, parameter servers etc.

To know about it, type

```
rosnode list
```
To know more
```
rosnode info /turtlesim
```

To know which all topics are published, we check
  ```
  rostopic list
  ```
Move a turtle using key board
```
rosrun turtlesim turtle_teleop_key
```

  We can check the published topic, using following command (example)
  ```
  rostopic echo /turtle1/pose
  ```
  
  We can publish to a publisher using following command (edit)
  ```
  rostopic pub /turtle1/cmd_vel geometry_msgs/Twist "linear:
  x: 0.0
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.0" 

```
We can also done using a python or c++ code, python code is attached for reference

Now we can use a launch file from a package to open turtlesim and motion code simultaneously

```
<?xml version="1.0" encoding="UTF-8"?>
<launch>
  <node name="one" pkg="turtlesim" type="turtlesim_node" />
  <node name="topic_publisher" pkg="<package_name>" type="move.py" />
 </launch>
 
 ```
 
# Drawing controlled shapes

```
#!/usr/bin/env python3
import rospy
from geometry_msgs.msg import Twist
PI = 3.1415926535897

def rotate():
    #Starts a new node
    rospy.init_node('robot_cleaner', anonymous=True)
    velocity_publisher = rospy.Publisher('/turtle1/cmd_vel', Twist, queue_size=10)
    vel_msg = Twist()

    # Receiveing the user's input
    print("Let's rotate your robot")
    speed = 30
    angle = 170
    

    #Converting from angles to radians
    angular_speed = speed*2*PI/360
    relative_angle = angle*2*PI/360

    #We wont use linear components
    vel_msg.linear.x=0.5
    vel_msg.linear.y=0
    vel_msg.linear.z=0
    vel_msg.angular.x = 0
    vel_msg.angular.y = 0

    # Checking if our movement is CW or CCW
    
    vel_msg.angular.z = angular_speed
    # Setting the current time for distance calculus
    t0 = rospy.Time.now().to_sec()
    current_angle = 0

    while(current_angle < relative_angle):
        velocity_publisher.publish(vel_msg)
        t1 = rospy.Time.now().to_sec()
        current_angle = angular_speed*(t1-t0)


    #Forcing our robot to stop
    vel_msg.angular.z = 0
    velocity_publisher.publish(vel_msg)
    rospy.spin()

if __name__ == '__main__':
    try:
        # Testing our function
        rotate()
    except rospy.ROSInterruptException:
        pass
  ```





