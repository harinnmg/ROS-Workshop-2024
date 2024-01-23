# Python for ROS 
[Python codes.pdf](https://github.com/harinnmg/ROS-Workshop-2024/files/13959332/Python.codes.pdf)

# CPP for ROS

## Hello world program in CPP
1. Create a folder 'mycpp'
2. gedit hello.cpp
3. Type the following and save
```
#include <iostream>
using namespace std;
int main() {
    cout << "Hello, World!" << endl;
    return 0;
}
```
Executing C++ files
```
g++ hello.cpp
./a.out
```

Giving a name to executable

```
g++ hello.cpp -o hello
./hello
```
### Executing cpp using cmake

In the same folder 'mycpp' create a file called 'CMakeLists.txt' and add following

```
cmake_minimum_required(VERSION 3.0)

project(mycpp)

add_executable(hello main.cpp)
```
This will make an executable hello
Now follow the commands

```
mkdir build
cd build
cmake ..
make
```
after compilation, run
```
./hello
```
# Introduction to ROS
You can find the basics at

https://wiki.ros.org/

# ROS File System
![Picture1](https://github.com/harinnmg/ROS-Workshop-2024/assets/64157740/c177a78a-0670-471f-a9f8-8e8d9b4421ca)

# ROS Workspace

 ```
 
 >> cd catkin_ws
 >> catkin_make
 ```
 
# Creating ROS Package
```
>> cd catkin_ws/src
>> catkin_create_pkg <package_name> rospy roscpp
>>catkin_make
```
Now create a new text file inside the package and copy the following code to it. Name it as "talker.py"
# Publisher code

```
#!/usr/bin/env python
import rospy
from std_msgs.msg import String
def publishMethod():
 pub=rospy.Publisher('talker',String,queue_size=10)
 rospy.init_node('publish_node',anonymous=True)
 rate=rospy.Rate(10)
 while not rospy.is_shutdown():
 
  publishstring= "hi"
  rospy.loginfo('data is being sent')
  pub.publish(publishstring)
  rate.sleep()

if __name__ == '__main__':
    try:
        publishMethod()
    except rospy.ROSInterruptException:
        pass

 ```
 
# Subscriber code

Open a new text file inside the package and name "subcriber.py"

```
#!/usr/bin/env python
import rospy
from std_msgs.msg import String

def callback(data):
    rospy.loginfo(rospy.get_caller_id() + "I heard %s", data.data)
    
def listener():

   
    rospy.init_node('listener', anonymous=True)

    rospy.Subscriber("talker", String, callback)

    
    rospy.spin()

if __name__ == '__main__':
    listener()
    
```
* After completion of this, do the following commands
```
chmod a+rw talker.py
chmod a+rw subsciber.py
```
# Running a ROS Master
Next is to run a ros master in a terminal in the directory catkin_ws
```
roscore
```
# Communication between nodes
Open a new terminal and type following commands
```
source devel/setup.bash
rosrun <package_name> talker.py
```
Open another terminal and type following commands
```
source devel/setup.bash
rosrun <package_name> subscriber.py
```
# Publishing through terminal
```
>>rostopic pub /topic_name std_msgs/String hello
```
# Publisher code in c++
```
#include "ros/ros.h"
#include "std_msgs/String.h"

#include <sstream>


int main(int argc, char **argv)
{
 
  ros::init(argc, argv, "talker");

 
  ros::NodeHandle n;

 
  ros::Publisher chatter_pub = n.advertise<std_msgs::String>("chatter", 1000);

  ros::Rate loop_rate(10);


  int count = 0;
  while (ros::ok())
  {
   
    std_msgs::String msg;

    std::stringstream ss;
    ss << "hello world " << count;
    msg.data = ss.str();

    ROS_INFO("%s", msg.data.c_str());


    chatter_pub.publish(msg);

    ros::spinOnce();

    loop_rate.sleep();
    ++count;
  }


  return 0;
}
```
# Subscriber Node in C++
In the SRC of 
```
#include "ros/ros.h"
#include "std_msgs/String.h"


void chatterCallback(const std_msgs::String::ConstPtr& msg)
{
  ROS_INFO("I heard: [%s]", msg->data.c_str());
}

int main(int argc, char **argv)
{
 
  ros::init(argc, argv, "listener");


  ros::NodeHandle n;


  ros::Subscriber sub = n.subscribe("chatter", 1000, chatterCallback);


  ros::spin();

  return 0;
}
```
Then add following lines in cMakeLists.txt inside src
```
 
 add_executable(talker src/talker.cpp)
add_dependencies(talker ${${PROJECT_NAME}_EXPORTED_TARGETS} ${catkin_EXPORTED_TARGETS})
 target_link_libraries(talker
 ${catkin_LIBRARIES}
 )
 
add_executable(listner src/listner.cpp)
add_dependencies(listner ${${PROJECT_NAME}_EXPORTED_TARGETS} ${catkin_EXPORTED_TARGETS})
 target_link_libraries(listner
 ${catkin_LIBRARIES}
 )

 ```
# Custom Message in ROS

```
#!/usr/bin/env python3

import rospy
from simple.msg import hello

rospy.init_node('topic_publisher')
pub = rospy.Publisher('/abc', hello, queue_size=1)
rate = rospy.Rate(2)
move = hello() # defining the way we can allocate the values
move.x = 1 # allocating the values in x direction - linear
move.y = 0 # allocating the values in z direction - angular

while not rospy.is_shutdown(): 
  pub.publish(move)
  rate.sleep()
```
In CMakeLists.txt, do the following editing  
  ```
  find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  message_generation # add this line
)
```

Also add
```
add_message_files(
  FILES
  MyCustomMessage.msg # add your message file(s) here
)

generate_messages(
  DEPENDENCIES
  std_msgs
)
```
In package.xml, do the following edit
```
<build_depend>message_generation</build_depend>
<exec_depend>message_runtime</exec_depend>
```

# Custom Service
In the package create a new folder 'srv' and gedit a file 'hai.srv'
```
int32 request_data
---
int32 response_data
```
Edit CMakeLists.txt with following
```
add_service_files(
  FILES
  CustomService.srv
)
```
Write the service code as follows
```
#!/usr/bin/env python3

import rospy
from simple.srv import hai

def handle_custom_service(req):
    rospy.loginfo("Received request with data: %d", req.request_data)
    # Perform some computation or action based on the request
    response = req.request_data * 2
    rospy.loginfo("Sending response with data: %d", response)
    return response

def custom_service_server():
    rospy.init_node('custom_service_server')
    service = rospy.Service('custom_service', hai, handle_custom_service)
    rospy.loginfo("Custom service server is ready.")
    rospy.spin()

if __name__ == '__main__':
    custom_service_server()
```


