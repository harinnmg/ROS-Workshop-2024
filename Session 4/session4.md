RVIZ code
```
Panels:
  - Class: rviz/Displays
    Help Height: 78
    Name: Displays
    Property Tree Widget:
      Expanded:
        - /Global Options1
        - /Status1
        - /RobotModel1
        - /TF1
      Splitter Ratio: 0.5
    Tree Height: 465
  - Class: rviz/Selection
    Name: Selection
  - Class: rviz/Tool Properties
    Expanded:
      - /2D Pose Estimate1
      - /2D Nav Goal1
      - /Publish Point1
    Name: Tool Properties
    Splitter Ratio: 0.5886790156364441
  - Class: rviz/Views
    Expanded:
      - /Current View1
    Name: Views
    Splitter Ratio: 0.5
  - Class: rviz/Time
    Name: Time
    SyncMode: 0
    SyncSource: ""
Preferences:Panels:
  - Class: rviz/Displays
    Help Height: 78
    Name: Displays
    Property Tree Widget:
      Expanded:
        - /Global Options1
        - /Status1
        - /RobotModel1
        - /TF1
      Splitter Ratio: 0.5
    Tree Height: 465
  - Class: rviz/Selection
    Name: Selection
  - Class: rviz/Tool Properties
    Expanded:
      - /2D Pose Estimate1
      - /2D Nav Goal1
      - /Publish Point1
    Name: Tool Properties
    Splitter Ratio: 0.5886790156364441
  - Class: rviz/Views
    Expanded:
      - /Current View1
    Name: Views
    Splitter Ratio: 0.5
  - Class: rviz/Time
    Name: Time
    SyncMode: 0
    SyncSource: ""
Preferences:
  PromptSaveOnExit: true
Toolbars:
  toolButtonStyle: 2
Visualization Manager:
  Class: ""
  Displays:
    - Alpha: 0.5
      Cell Size: 1
      Class: rviz/Grid
      Color: 160; 160; 164
      Enabled: true
      Line Style:
        Line Width: 0.029999999329447746
        Value: Lines
      Name: Grid
      Normal Cell Count: 0
      Offset:
        X: 0
        Y: 0
        Z: 0
      Plane: XY
      Plane Cell Count: 10
      Reference Frame: <Fixed Frame>
      Value: true
    - Alpha: 0.5
      Class: rviz/RobotModel
      Collision Enabled: false
      Enabled: true
      Links:
        All Links Enabled: true
        Expand Joint Details: false
        Expand Link Details: false
        Expand Tree: false
        Link Tree Style: Links in Alphabetic Order
        base_link:
          Alpha: 1
          Show Axes: false
          Show Trail: false
          Value: true
        right_leg:
          Alpha: 1
          Show Axes: false
          Show Trail: false
          Value: true
      Name: RobotModel
      Robot Description: robot_description
      TF Prefix: ""
      Update Interval: 0
      Value: true
      Visual Enabled: true
    - Class: rviz/TF
      Enabled: true
      Frame Timeout: 15
      Frames:
        All Enabled: true
        base_link:
          Value: true
        right_leg:
          Value: true
      Marker Alpha: 1
      Marker Scale: 0.5
      Name: TF
      Show Arrows: true
      Show Axes: true
      Show Names: true
      Tree:
        base_link:
          right_leg:
            {}
      Update Interval: 0
      Value: true
  Enabled: true
  Global Options:
    Background Color: 48; 48; 48
    Default Light: true
    Fixed Frame: base_link
    Frame Rate: 30
  Name: root
  Tools:
    - Class: rviz/Interact
      Hide Inactive Objects: true
    - Class: rviz/MoveCamera
    - Class: rviz/Select
    - Class: rviz/FocusCamera
    - Class: rviz/Measure
    - Class: rviz/SetInitialPose
      Theta std deviation: 0.2617993950843811
      Topic: /initialpose
      X std deviation: 0.5
      Y std deviation: 0.5
    - Class: rviz/SetGoal
      Topic: /move_base_simple/goal
    - Class: rviz/PublishPoint
      Single click: true
      Topic: /clicked_point
  Value: true
  Views:
    Current:
      Class: rviz/Orbit
      Distance: 0.9804548025131226
      Enable Stereo Rendering:
        Stereo Eye Separation: 0.05999999865889549
        Stereo Focal Distance: 1
        Swap Stereo Eyes: false
        Value: false
      Field of View: 0.7853981852531433
      Focal Point:
        X: 0
        Y: 0
        Z: 0
      Focal Shape Fixed Size: true
      Focal Shape Size: 0.05000000074505806
      Invert Z Axis: false
      Name: Current View
      Near Clip Distance: 0.009999999776482582
      Pitch: 0.7003970146179199
      Target Frame: <Fixed Frame>
      Yaw: 0.5235819816589355
    Saved: ~
Window Geometry:
  Displays:
    collapsed: false
  Height: 768
  Hide Left Dock: false
  Hide Right Dock: false
  QMainWindow State: 000000ff00000000fd0000000400000000000001560000025cfc0200000008fb0000001200530065006c0065006300740069006f006e00000001e10000009b0000005c00fffffffb0000001e0054006f006f006c002000500072006f007000650072007400690065007302000001ed000001df00000185000000a3fb000000120056006900650077007300200054006f006f02000001df000002110000018500000122fb000000200054006f006f006c002000500072006f0070006500720074006900650073003203000002880000011d000002210000017afb000000100044006900730070006c006100790073010000003d0000025c000000c900fffffffb0000002000730065006c0065006300740069006f006e00200062007500660066006500720200000138000000aa0000023a00000294fb00000014005700690064006500530074006500720065006f02000000e6000000d2000003ee0000030bfb0000000c004b0069006e0065006300740200000186000001060000030c00000261000000010000010f0000025cfc0200000003fb0000001e0054006f006f006c002000500072006f00700065007200740069006500730100000041000000780000000000000000fb0000000a00560069006500770073010000003d0000025c000000a400fffffffb0000001200530065006c0065006300740069006f006e010000025a000000b200000000000000000000000200000490000000a9fc0100000001fb0000000a00560069006500770073030000004e00000080000002e10000019700000003000004c000000044fc0100000002fb0000000800540069006d00650100000000000004c0000003bc00fffffffb0000000800540069006d006501000000000000045000000000000000000000024f0000025c00000004000000040000000800000008fc0000000100000002000000010000000a0054006f006f006c00730100000000ffffffff0000000000000000
  Selection:
    collapsed: false
  Time:
    collapsed: false
  Tool Properties:
    collapsed: false
  Views:
    collapsed: false
  Width: 1216
  X: 17
  Y: 27
  PromptSaveOnExit: true
Toolbars:
  toolButtonStyle: 2
Visualization Manager:
  Class: ""
  Displays:
    - Alpha: 0.5
      Cell Size: 1
      Class: rviz/Grid
      Color: 160; 160; 164
      Enabled: true
      Line Style:
        Line Width: 0.029999999329447746
        Value: Lines
      Name: Grid
      Normal Cell Count: 0
      Offset:
        X: 0
        Y: 0
        Z: 0
      Plane: XY
      Plane Cell Count: 10
      Reference Frame: <Fixed Frame>
      Value: true
    - Alpha: 0.5
      Class: rviz/RobotModel
      Collision Enabled: false
      Enabled: true
      Links:
        All Links Enabled: true
        Expand Joint Details: false
        Expand Link Details: false
        Expand Tree: false
        Link Tree Style: Links in Alphabetic Order
        base_link:
          Alpha: 1
          Show Axes: false
          Show Trail: false
          Value: true
        right_leg:
          Alpha: 1
          Show Axes: false
          Show Trail: false
          Value: true
      Name: RobotModel
      Robot Description: robot_description
      TF Prefix: ""
      Update Interval: 0
      Value: true
      Visual Enabled: true
    - Class: rviz/TF
      Enabled: true
      Frame Timeout: 15
      Frames:
        All Enabled: true
        base_link:
          Value: true
        right_leg:
          Value: true
      Marker Alpha: 1
      Marker Scale: 0.5
      Name: TF
      Show Arrows: true
      Show Axes: true
      Show Names: true
      Tree:
        base_link:
          right_leg:
            {}
      Update Interval: 0
      Value: true
  Enabled: true
  Global Options:
    Background Color: 48; 48; 48
    Default Light: true
    Fixed Frame: base_link
    Frame Rate: 30
  Name: root
  Tools:
    - Class: rviz/Interact
      Hide Inactive Objects: true
    - Class: rviz/MoveCamera
    - Class: rviz/Select
    - Class: rviz/FocusCamera
    - Class: rviz/Measure
    - Class: rviz/SetInitialPose
      Theta std deviation: 0.2617993950843811
      Topic: /initialpose
      X std deviation: 0.5
      Y std deviation: 0.5
    - Class: rviz/SetGoal
      Topic: /move_base_simple/goal
    - Class: rviz/PublishPoint
      Single click: true
      Topic: /clicked_point
  Value: true
  Views:
    Current:
      Class: rviz/Orbit
      Distance: 0.9804548025131226
      Enable Stereo Rendering:
        Stereo Eye Separation: 0.05999999865889549
        Stereo Focal Distance: 1
        Swap Stereo Eyes: false
        Value: false
      Field of View: 0.7853981852531433
      Focal Point:
        X: 0
        Y: 0
        Z: 0
      Focal Shape Fixed Size: true
      Focal Shape Size: 0.05000000074505806
      Invert Z Axis: false
      Name: Current View
      Near Clip Distance: 0.009999999776482582
      Pitch: 0.7003970146179199
      Target Frame: <Fixed Frame>
      Yaw: 0.5235819816589355
    Saved: ~
Window Geometry:
  Displays:
    collapsed: false
  Height: 768
  Hide Left Dock: false
  Hide Right Dock: false
  QMainWindow State: 000000ff00000000fd0000000400000000000001560000025cfc0200000008fb0000001200530065006c0065006300740069006f006e00000001e10000009b0000005c00fffffffb0000001e0054006f006f006c002000500072006f007000650072007400690065007302000001ed000001df00000185000000a3fb000000120056006900650077007300200054006f006f02000001df000002110000018500000122fb000000200054006f006f006c002000500072006f0070006500720074006900650073003203000002880000011d000002210000017afb000000100044006900730070006c006100790073010000003d0000025c000000c900fffffffb0000002000730065006c0065006300740069006f006e00200062007500660066006500720200000138000000aa0000023a00000294fb00000014005700690064006500530074006500720065006f02000000e6000000d2000003ee0000030bfb0000000c004b0069006e0065006300740200000186000001060000030c00000261000000010000010f0000025cfc0200000003fb0000001e0054006f006f006c002000500072006f00700065007200740069006500730100000041000000780000000000000000fb0000000a00560069006500770073010000003d0000025c000000a400fffffffb0000001200530065006c0065006300740069006f006e010000025a000000b200000000000000000000000200000490000000a9fc0100000001fb0000000a00560069006500770073030000004e00000080000002e10000019700000003000004c000000044fc0100000002fb0000000800540069006d00650100000000000004c0000003bc00fffffffb0000000800540069006d006501000000000000045000000000000000000000024f0000025c00000004000000040000000800000008fc0000000100000002000000010000000a0054006f006f006c00730100000000ffffffff0000000000000000
  Selection:
    collapsed: false
  Time:
    collapsed: false
  Tool Properties:
    collapsed: false
  Views:
    collapsed: false
  Width: 1216
  X: 17
  Y: 27
  ```
  
  Launch file
  
  ```
  <launch>

  <arg name="model" default="$(find urdftest)/urdf/test.urdf"/>
  <arg name="gui" default="true" />
  <arg name="rvizconfig" default="$(find urdftest)/rviz/urdf.rviz" />

  <param name="robot_description" command="$(find xacro)/xacro $(arg model)" />

  <node if="$(arg gui)" name="joint_state_publisher" pkg="joint_state_publisher_gui" type="joint_state_publisher_gui" />
  <node unless="$(arg gui)" name="joint_state_publisher" pkg="joint_state_publisher" type="joint_state_publisher" />
  <node name="robot_state_publisher" pkg="robot_state_publisher" type="robot_state_publisher" />
  <node name="rviz" pkg="rviz" type="rviz" args="-d $(arg rvizconfig)" required="true" />

</launch>
```


Urdf code

```
<?xml version="1.0"?>
<robot name="multipleshapes">
  <link name="base_link">
    <visual>
      <geometry>
        <cylinder length="0.6" radius="0.2"/>
      </geometry>
    </visual>
  </link>

  <link name="right_leg">
    <visual>
      <geometry>
        <box size="0.6 0.1 0.2"/>
      </geometry>
    </visual>
  </link>

  <joint name="base_to_right_leg" type="fixed">
    <parent link="base_link"/>
    <child link="right_leg"/>
  </joint>

</robot>
```
# Familiarization of Gazebo
## Theory
Gazebo is an open robotics simulator, where one can design and simulate robots. A robot will be associated with different predefined structures, sensors, actuators etc. So as seen in example 5, after adding basic shapes, we can add the capabilities in the form of plugins. 
plugin is a chunk of code that is compiled as a shared library and inserted into the simulation. The plugin has direct access to all the functionality of Gazebo through the standard C++ classes.


## Procedure
1. Create a new package inside your workspace src, and create three folders inside; urdf,launch and world.
2. Inside urdf folder, create a text file with .urdf extension and copy the following code.

Urdf file

```
<?xml version="1.0"?>
<robot name="myfirst">
<link name="base_link">
<inertial>
<mass value="5"/>
<origin rpy="0 0 0" xyz="0 0 0"/>
<inertia ixx="0" ixy="0" ixz="0" iyy="0.1" iyz="0" izz="0"/>
</inertial>
<collision>
<geometry>
<cylinder length="0.5" radius="0.5"/>
</geometry>
</collision>
<visual>
<geometry>
<cylinder length="0.5" radius="0.5"/>
</geometry>
</visual>
</link>

</robot>
```
3. Inside the launch folder, create a text file with extension .launch, copy the following code, replace <package_name> with your package name and <urdf_name> with the urdf name.
Launch file

```
<?xml version="1.0"?>
<launch>
<param name="robot_description" command="cat $(find test3)/urdf/test.urdf" />
<arg name="rvizconfig" default="$(find test3)/rviz/test.rviz" />
<arg name = "x" default = "0"/>
<arg name = "y" default = "0"/>
<arg name = "z" default = "0"/>
<arg name="gui" default="true" />
<node name="spawn_urdf" pkg="gazebo_ros" type="spawn_model" output="screen"
args="-urdf -param robot_description -model my_first -x $(arg x) -y $(arg y) -z $(arg z)"/>

  <include file="$(find gazebo_ros)/launch/empty_world.launch">

    <arg name="use_sim_time" value="true"/>
    <arg name="debug" value="false"/>
    <arg name="gui" value="true" />
    <arg name="world_name" value="true"/>
  </include>
  <node if="$(arg gui)" name="joint_state_publisher" pkg="joint_state_publisher_gui" type="joint_state_publisher_gui" />
<node unless="$(arg gui)" name="joint_state_publisher" pkg="joint_state_publisher" type="joint_state_publisher" />
<node name="robot_state_publisher" pkg="robot_state_publisher" type="robot_state_publisher" />
<node name="rviz" pkg="rviz" type="rviz" args="-d $(arg rvizconfig)" required="true" />
</launch>
```
4. Go to workspace and catkin_make
5. Apply the command ```source devel/setup.bash```
6. Run the command ```roslaunch <package_name> <launch_code with extension>``` replace  <package_name> with your package name and <launch_code with extension> with your launch file name with .launch extension. You will see the cylinder is spawned in Gazebo.

## Adding Joints in Gazebo
```
<?xml version="1.0"?>
<robot name="myfirst">
<link name="base_link">
<inertial>
<mass value="5"/>
<origin rpy="0 0 0" xyz="0 0 0"/>
<inertia ixx="0" ixy="0" ixz="0" iyy="0.1" iyz="0" izz="0"/>
</inertial>
<collision>
<geometry>
<cylinder length="0.5" radius="0.5"/>
</geometry>
</collision>
<visual>
<geometry>
<cylinder length="0.5" radius="0.5"/>
</geometry>
</visual>
</link>
<link name="right_leg">
<inertial>
<mass value="5"/>
<origin rpy="0 0 0" xyz="0 0 0"/>
<inertia ixx="0" ixy="0" ixz="0" iyy="0.1" iyz="0" izz="0"/>
</inertial>
<collision>
<geometry>
<box size="0.6 0.1 0.2"/>
</geometry>
</collision>
    <visual>
      <geometry>
       <box size="0.6 0.1 0.2"/>
      </geometry>
    </visual>
  </link>
   <joint name="base_to_right_leg" type="continuous">
    <parent link="base_link"/>
    <child link="right_leg"/>
     <origin
      xyz="0 0 0.35"
      rpy="0 0 0" />

    <axis
      xyz="0 0 1" />
    <limit
      effort="1"
      velocity="1" />
  </joint>


</robot>
```
## Adding Camera
```
<link name="camera_link">
    <collision>
      <origin xyz="0 0 0" rpy="0 0 0"/>
      <geometry>
    <box size="0.1 0.1 0.1"/>
      </geometry>
    </collision>

    <visual>
      <origin xyz="0 0 0" rpy="0 0 0"/>
      <geometry>
    <box size="0.1 0.1 0.1"/>
      </geometry>
      <material name="red"/>
    </visual>

    <inertial>
      <mass value="1e-5" />
      <origin xyz="0 0 0" rpy="0 0 0"/>
      <inertia ixx="1e-6" ixy="0" ixz="0" iyy="1e-6" iyz="0" izz="1e-6" />
    </inertial>
  </link>
   <joint name="right_leg" type="fixed">
    <axis xyz="0 0 1" />
    <origin xyz="0 0 0.15" rpy="0 0 0"/>
    <parent link="right_leg"/>
    <child link="camera_link"/>
  </joint>
    <!-- camera -->
 <gazebo reference="camera_link">
    <sensor type="camera" name="camera1">
      <update_rate>30.0</update_rate>
      <camera name="head">
        <horizontal_fov>1.3962634</horizontal_fov>
        <image>
          <width>800</width>
          <height>800</height>
          <format>R8G8B8</format>
        </image>
        <clip>
          <near>0.02</near>
          <far>300</far>
        </clip>
        <noise>
          <type>gaussian</type>
          <!-- Noise is sampled independently per pixel on each frame.
               That pixel's noise value is added to each of its color
               channels, which at that point lie in the range [0,1]. -->
          <mean>0.0</mean>
          <stddev>0.007</stddev>
        </noise>
      </camera>
      <plugin name="camera_controller" filename="libgazebo_ros_camera.so">
       <frame_name>camera_link_optical</frame_name>
        <alwaysOn>true</alwaysOn>
        <updateRate>0.0</updateRate>
        <cameraName>camera1</cameraName>
        <imageTopicName>image_raw</imageTopicName>
        <cameraInfoTopicName>camera_info</cameraInfoTopicName>
        
        <hackBaseline>0.07</hackBaseline>
        <distortionK1>0.0</distortionK1>
        <distortionK2>0.0</distortionK2>
        <distortionK3>0.0</distortionK3>
        <distortionT1>0.0</distortionT1>
        <distortionT2>0.0</distortionT2>
      </plugin>
    </sensor>
  </gazebo>
```

#  Create a custom world

1. Close all the terminals and open Gazebo
```gazebo```
2. Go to eidt>>bulding editor and create shapes your own. Save the shape and exit building editor
3. Save the world from file>>save to the location 'world' folder inside your package
4. Go to the launch folder inside the package and edit the code, replace <package_nmae> and <world_nmae> with yours

```
<?xml version="1.0"?>
<launch>
<param name="robot_description" command="cat $(find
<package_name>)/urdf/<urdf_name>" />
<arg name = "x" default = "0"/>
<arg name = "y" default = "0"/>
<arg name = "z" default = "0"/>
 <!-- World File -->
  <arg name="world_file" default="$(find package name)/world/world name"/>
<node name="spawn_urdf" pkg="gazebo_ros" type="spawn_model" output="screen"
args="-urdf -param robot_description -model my_first -x $(arg x) -y $(arg y) -z $(arg z)"/>

  <include file="$(find gazebo_ros)/launch/empty_world.launch">
    <arg name="use_sim_time" value="true"/>
    <arg name="debug" value="false"/>
    <arg name="gui" value="true" />
    <arg name="world_name" value="$(arg world_file)"/>
  </include>

</launch>
```
5. Do the procedure for roslaunch as we done previously 

# With Control
```
<?xml version="1.0"?>
<robot name="myfirst">
<link name="base_link">
<inertial>
<mass value="5"/>
<origin rpy="0 0 0" xyz="0 0 0"/>
<inertia ixx="0" ixy="0" ixz="0" iyy="0.1" iyz="0" izz="0"/>
</inertial>
<collision>
<geometry>
<cylinder length="0.5" radius="0.5"/>
</geometry>
</collision>
<visual>
<geometry>
<cylinder length="0.5" radius="0.5"/>
</geometry>
</visual>
</link>
<link name="right_leg1">
<inertial>
<mass value="5"/>
<origin rpy="0 0 0" xyz="0 0 0"/>
<inertia ixx="0.5" ixy="0" ixz="0" iyy="0.1" iyz="0" izz="0.2"/>
</inertial>
<collision>
<geometry>
<box size="0.6 0.1 0.2"/>
</geometry>
</collision>
    <visual>
      <geometry>
       <box size="0.6 0.1 0.2"/>
      </geometry>
    </visual>
  </link>
   <joint name="base_to_right_leg" type="continuous">
    <parent link="base_link"/>
    <child link="right_leg1"/>
     <origin
      xyz="0 0 0.45"
      rpy="0 0 0" />

    <axis
      xyz="0 0 1" />
    <limit
      effort="1"
      velocity="1" />
  </joint>

<link name="camera_link">
    <collision>
      <origin xyz="0 0 0" rpy="0 0 0"/>
      <geometry>
    <box size="0.1 0.1 0.1"/>
      </geometry>
    </collision>

    <visual>
      <origin xyz="0 0 0" rpy="0 0 0"/>
      <geometry>
    <box size="0.1 0.1 0.1"/>
      </geometry>
      <material name="red"/>
    </visual>

    <inertial>
      <mass value="1e-5" />
      <origin xyz="0 0 0" rpy="0 0 0"/>
      <inertia ixx="1e-6" ixy="0" ixz="0" iyy="1e-6" iyz="0" izz="1e-6" />
    </inertial>
  </link>
   <joint name="right_leg" type="fixed">
    <axis xyz="0 0 1" />
    <origin xyz="0 0 0.55" rpy="0 0 0"/>
    <parent link="right_leg1"/>
    <child link="camera_link"/>
  </joint>
    <!-- camera -->
 <gazebo reference="camera_link">
    <sensor type="camera" name="camera1">
      <update_rate>30.0</update_rate>
      <camera name="head">
        <horizontal_fov>1.3962634</horizontal_fov>
        <image>
          <width>800</width>
          <height>800</height>
          <format>R8G8B8</format>
        </image>
        <clip>
          <near>0.02</near>
          <far>300</far>
        </clip>
        <noise>
          <type>gaussian</type>
          <!-- Noise is sampled independently per pixel on each frame.
               That pixel's noise value is added to each of its color
               channels, which at that point lie in the range [0,1]. -->
          <mean>0.0</mean>
          <stddev>0.007</stddev>
        </noise>
      </camera>
      <plugin name="camera_controller" filename="libgazebo_ros_camera.so">
       <frame_name>camera_link_optical</frame_name>
        <alwaysOn>true</alwaysOn>
        <updateRate>0.0</updateRate>
        <cameraName>camera1</cameraName>
        <imageTopicName>image_raw</imageTopicName>
        <cameraInfoTopicName>camera_info</cameraInfoTopicName>
        
        <hackBaseline>0.07</hackBaseline>
        <distortionK1>0.0</distortionK1>
        <distortionK2>0.0</distortionK2>
        <distortionK3>0.0</distortionK3>
        <distortionT1>0.0</distortionT1>
        <distortionT2>0.0</distortionT2>
      </plugin>
    </sensor>
  </gazebo>
  <gazebo>

<plugin name="gazebo_ros_control" filename="libgazebo_ros_control.so">
<robotNamespace>/myfirst</robotNamespace>
<robotSimType>gazebo_ros_control/DefaultRobotHWSim</robotSimType>
</plugin>
</gazebo> 

   <transmission name="tran1">
   <type>transmission_interface/SimpleTransmission</type>
  <joint name="base_to_right_leg">
    <hardwareInterface>hardware_interface/EffortJointInterface</hardwareInterface>
  </joint>
  <actuator name="Rev1_actr">
    <hardwareInterface>hardware_interface/EffortJointInterface</hardwareInterface>
    <mechanicalReduction>1</mechanicalReduction>
  </actuator>
</transmission>

  
<gazebo>
    <plugin name="joint_state_publisher" filename="libgazebo_ros_joint_state_publisher.so">
        <robotNamespace>myfirst</robotNamespace>
        <jointName>base_to_right_leg</jointName>
        <updateRate>100</updateRate>
    </plugin>
  </gazebo> 
</robot>
```

