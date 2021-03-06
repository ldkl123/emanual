### 1. Overview   
This page explains how to control upgraded walking(online walking).  
> Reference 1 : [Introduction to Humanoid Robotics]
> Reference 2 : [op3_online_walking_module]

### 2. Description
#### 2.1 How to
 - Preparation : Set the module and move to the tab
   1. Setting the module : Click `online_walking_module` button

   2. Select `Online Walking` tab of the gui demo program.

  ![](/assets/images/platform/op3/op3_online_walking_01.png)

 - Controlling walking of ROBOTIS-OP3
    1. Go to initial pose : click `Go to Initial Pose` button

    2. Balance On   

    3. Set the walking parameters    

    4. Send a walking command to `op3_manager`

  ![](/assets/images/platform/op3/op3_online_walking_02.png)

    > Walking parameters
    >  - DSP ratio : double support phase ratio
    >  - LIPM Height : linear inverted pendulum height
    >  - Foot Height Max : maximum value of foot height
    >  - ZMP Offset x : ZMP offset for x-direction
    >  - ZMP Offset y : ZMP offset for y-direction(The larger the value, the outer the zmp.)
    >  - Body Offset : desired body offset
    >  - Foot Distance : desired foot distance between left and right foot

### 3. Online walking using footstep planner
  > Reference : [Online walking using footstep planner]  

[&lt;&lt; Back](op3_user's_guide.md)

[Introduction to Humanoid Robotics]:http://www.springer.com/gp/book/9783642545351
[op3_online_walking_module]:op3_online_walking_module.md
[Online walking using footstep planner]:op3_how_to_control_upgraded_walking_using_footstep_planner.md
