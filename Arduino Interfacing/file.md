Procedure 
1.	Connect arduino to the USB port. Though the arduino is connected to a USB port, it internally converts to a serial port.  
2.	check the arduino is connected by command ls /dev in terminal and ensure  ttyUSB0 is there 
3.Download arduino ide zip file and extract to home folder 
4.	Run the installation sudo ./install.sh 
5.	The ide will be installed and open the ide 
6.	From sketch>>libraries>>include library, select roserial Arduino library and make sure that the folder is inside the folder which contains other libraries 
7.	Run the following commands to make the arduino executable  sudo usermod -a -G dialout user sudo chmod a+rw /dev/ttyUSB0 
8.	From foles>>examples>> ROS Serial Arduino Library choose Hello world 
9.	To remove the bug in ros library go to ~/arduino-
1.8.19/libraries/Rosserial_Arduino_Library/src/ros$ msg.h  change #include <string.h> and memcpy() 
10.	Run the code from Arduino 
11.	In ROS workspace, start a new master 
12.	Run the command in the master "rosrun rosserial_python serial_node.py /dev/ttyUSB0" 
13.	To receive the message check rostopic echo /chatter 
 
```
#include <ros.h>
#include <std_msgs/Int32.h>
ros::NodeHandle nh;
std_msgs::Int32 str_msg;
ros::Publisher chatter("chatter", &str_msg);
#define echoPin 12 // attach pin D2 Arduino to pin Echo of HC-SR04
#define trigPin 9 //attach pin D3 Arduino to pin Trig of HC-SR04
// defines variables
long duration; // variable for the duration of sound wave travel
int distance; // variable for the distance measurement
void setup() {
pinMode(trigPin, OUTPUT); // Sets the trigPin as an OUTPUT
pinMode(echoPin, INPUT); // Sets the echoPin as an INPUT
Serial.begin(9600); // // Serial Communication is starting with 9600 of baudrate speed
Serial.println("Ultrasonic Sensor HC-SR04 Test"); // print some text in Serial Monitor
Serial.println("with Arduino UNO R3");
nh.initNode();
nh.advertise(chatter);
}
void loop() {
// Clears the trigPin condition
digitalWrite(trigPin, LOW);
delayMicroseconds(2);
// Sets the trigPin HIGH (ACTIVE) for 10 microseconds
digitalWrite(trigPin, HIGH);
delayMicroseconds(10);
digitalWrite(trigPin, LOW);
// Reads the echoPin, returns the sound wave travel time in microseconds
duration = pulseIn(echoPin, HIGH);
// Calculating the distance
distance = duration * 0.034 / 2; // Speed of sound wave divided by 2 (go and back)
// Displays the distance on the Serial Monitor
Serial.print("Distance: ");
Serial.print(distance);
Serial.println(" cm");
str_msg.data = distance;
chatter.publish( &str_msg );
nh.spinOnce();
delay(1000);
}
```
