### 1. Overview
This chapter explains installation and configuration of Robot Operating System(ROS) for ROBOTIS-OP3. Also, common ROS Packages and developed ROS Packages will be introduced.  



### 2. [What is ROS?]
<a href="http://www.ros.org/about-ros">  ![](/assets/images/platform/op3/ros_image.png) </a>


### 3. How to install ROS
 - version : Kinetic  
 - Installation(Desktop-Full)  
   > Reference : [ROS Installation - WIKI]
     - For Linux Mint user  
     - If you want to install ROS in Linux mint, you should type ```sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list'``` instead of ```sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'``` in the step of [```Setup your sources.list```]


### 4. SetUp
#### 4.1 ROS Environment Setting
> Reference : [http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment]

#### 4.2 ROS Network Setup
> Reference : [ROS Network Setup]  

#### 4.3 Example Setting
  1. Open the bash file with an editor to apply configuration.  
     ```
     $ xed ~/.bashrc
     ```

  2. Append below contents at the end of the `.bashrc` file.  
     ```bash    
     # Set ROS Kinetic
     source /opt/ros/kinetic/setup.bash
     source ~/catkin_ws/devel/setup.bash

     ##### Set ROS Network ####
     # ROS Master(localhost)
     export ROS_MASTER_URI=http://10.41.0.1:11311

     # local ROS IP
     export ROS_IP=10.41.0.1
     ```

     > Reference : In order to operate ROS in a network with multiple PCs, addresses of the ROS_MASTER_URI and the ROS_IP have to be replaced with the `core` PC's IP address and the remote PC's IP address respectively.  
     > Reference : If Hotspot is configured, use "10.42.0.1". Otherwise, use "localhost" instead of IP address.
       - ROS_MASTER_URI=http://localhost:11311
       - ROS_IP=localhost

  3. Use below command to apply modified configuration or open a new terminal window to reload configuration.  
     ```
     $ source ~/.bashrc
     ```

### 5. ROBOTIS ROS Packages for ROBOTIS-OP3  
 1. [DynamixelSDK] : SDK for Dynamixel  
 2. [ROBOTIS-Framerowk] : The packages to use ROS (Robot Operating System) for robots assembled with ROBOTIS products.  
 3. [ROBOTIS-Framerowk-msgs] : Messages used in the ROBOTIS-Framework.  
 4. [ROBOTIS-Math] : Basic calculation related to transformation and trajectory functions.  
 5. [ROBOTIS-OP3] : ROS Packages running in the ROBOTIS-OP3.
 6. [ROBOTIS-OP3-Common]
 7. [ROBOTIS-OP3-Demo]
 8. [ROBOTIS-OP3-msgs]  
 9. [ROBOTIS-OP3-Tools]  
 10. [ROBOTIS-Utility]


### 6. Additional ROS Package
 1. face_detection  
    - This ROS Package detects faces.  
    - Link : [https://github.com/ROBOTIS-GIT/face_detection]
    - Message  
       - Name : `FaceCoord`  
       - Type : [std_msgs/Int32MultiArray]
       - Data : [fps, faces num, image width, image height, face id, tracking count, x, y, face_width, face_height, ...]  

 2. robot_upstart  
    - This ROS Package is used to automatically execute ROS on startup.  
    - Link : [http://wiki.ros.org/robot_upstart]
    - [How to setup auto start]

 3. usb_cam  
    - USB Camera  
    - Link : [http://wiki.ros.org/usb_cam]
    - Additional Installation : The following package must be manually installed in order to modify camera parameters.  
      ```
      $ sudo apt install v4l-utils
      ```  

[&lt;&lt; Back](op3_user's_guide.md)

[What is ROS?]:http://www.ros.org/about-ros/
[ROS Installation - WIKI]:http://wiki.ros.org/kinetic/Installation/Ubuntu  
[```Setup your sources.list```]:http://wiki.ros.org/kinetic/Installation/Ubuntu#Installation.2BAC8-Ubuntu.2BAC8-Sources.Setup_your_sources.list)
[http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment]:http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment
[ROS Network Setup]:http://wiki.ros.org/ROS/NetworkSetup

[DynamixelSDK]:https://github.com/ROBOTIS-GIT/DynamixelSDK/wiki
[ROBOTIS-Framerowk]:https://github.com/ROBOTIS-GIT/ROBOTIS-Documents/wiki/ROBOTIS-Framework-Documents
[ROBOTIS-Framerowk-msgs]:https://github.com/ROBOTIS-GIT/ROBOTIS-Documents/wiki/ROBOTIS-Framework-Documents
[ROBOTIS-Math]:https://github.com/ROBOTIS-GIT/ROBOTIS-Documents/wiki/robotis_math
[ROBOTIS-OP3]:robotis_op3.md
[ROBOTIS-OP3-Common]:robotis_op3_common.md
[ROBOTIS-OP3-Demo]:robotis_op3_demo.md
[ROBOTIS-OP3-msgs]: robotis_op3_msgs.md
[ROBOTIS-OP3-Tools]:robotis_op3_tools.md
[ROBOTIS-Utility]:
[https://github.com/ROBOTIS-GIT/face_detection]:https://github.com/ROBOTIS-GIT/face_detection
[std_msgs/Int32MultiArray]: /docs/en/popup/std_msgs_Int32MultiArray_msg/
[http://wiki.ros.org/robot_upstart]:http://wiki.ros.org/robot_upstart  
[http://wiki.ros.org/usb_cam]:http://wiki.ros.org/usb_cam  

[How to setup auto start]:OP3_How_to_kill_the_demo_program#31_start_demo_program_on_start.md
