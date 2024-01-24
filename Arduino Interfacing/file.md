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
 

